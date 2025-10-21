---
title: "Verifying Results with Exception Handling"
description: "Ensure accurate outcomes by mastering exception handling for result verification. Learn best practices for robust code."
---

Results of [FileAdapter](/reference/datagate/datagate-client/file-adapter.html) and [ AdgDataSet](adg-dataset-class.html) methods are provided via .NET exception handling. The standard exception object in DG is [dgException](/reference/datagate/datagate-common/dg-exception.html). DG uses **dgException** to transmit both error conditions and "normal" procedural conditions, such as "end-of-file". In the examples shown so far, tests for dgException have been omitted for clarity. In your own DG programs, you would use these checks to improve the reliability of your program. The DG reference documentation for access and other methods lists the common **dgException** objects thrown. 

Revising a previous example, the following code will check for certain conditions, such as end-of-file.

```cs

using System;
using System.Data;
using System.Windows.Forms;
using ASNA.DataGate.Client;
using ASNA.DataGate.Common;
namespace NetworkRecovery
{
    public class Form1 | System.Windows.Forms.Form     
    {     
        const string srcStr = "asna network database";
        private System.Windows.Forms.Button button1;
        private System.ComponentModel.Container components = null;
        public Form1()...     
        protected override void Dispose(bool disposing)...           
        #region Windows Form Designer generated code     
        ...Designer code omitted...
        #endregion

        [STAThread]
        static void Main()...     
      
        private void button1_Click(object sender, System.EventArgs e)
        {
            AdgConnection cx = new AdgConnection(srcStr);
            bool retry = false;
            Cursor origCursor = Cursor.Current;

            // enter the "retry" loop     
            do
            {
                try
                {
                    retry = false;
                    Cursor.Current = Cursors.WaitCursor; // hourglass     
                    cx.Open();                           // this will throw dgException if errors occur     
                }
                catch (dgException ex)
                {
                    string mbMsg = ex.Message;
                    // check for error indicating "service not running"     
                    if (ex.Error == dgErrorNumber.dgEiNORESPONSE)

                        mbMsg = "Cannot connect to " + srcStr + ". Is the service running?";
                    // check for error indicating "network down"     
                    else if (ex.Error == dgErrorNumber.dgEiCONNLOST || ex.Error == dgErrorNumber.dgEiHOSTNOTFND)
                        mbMsg = "Cannot connect to " + srcStr + ". Is the network available?";
                    DialogResult dr = MessageBox.Show(mbMsg, "Database Provider Unavailable",
                    MessageBoxButtons.RetryCancel, MessageBoxIcon.Hand, MessageBoxDefaultButton.Button1, 0);
                    if (dr == DialogResult.Retry)
                        retry = true;
                }
                finally
                {
                    Cursor.Current = origCursor;
                }
            } while (retry == true);

            // In this simple example, just check the connection state and quit     
            if (cx.State == ConnectionState.Open)
                MessageBox.Show("Connected!");
            Close();
        }
    }
}

```

The code in this simple example opens a keyed-access file, then enters a "<span>try-catch</span>" block, to perform read operations. The first [ReadSequential](/reference/datagate/datagate-client/file-adapter-readsequential.html) method reads the first record in the file. Next, [ ReadRandomKey](/reference/datagate/datagate-client/file-adapter-readrandomkey.html) is called to read the first record with a particular key. If the file has no records, <span>dgException</span> will be thrown from the <span>ReadSequential</span> method, and the value of the <span>dgException.Error</span> property will be dgEaEOF. In this case, the program will print the result "End of file." If the file has at least one record, but none with a CMCustNo value of 200000, then dgException will be thrown from <span>ReadRandomKey</span> with an Error value of dgEaNOTFND. 

Note that not all traditional "feedback" information regarding the last access performed is transmitted through dgException. Other properties of FileAdapter, such as [ ExactSeek](/reference/datagate/datagate-client/file-adapter.html#properties), [RRN](/reference/datagate/datagate-client/file-adapter.html#properties) and [ CurrentFormatIndex](/reference/datagate/datagate-client/file-adapter.html#properties) are provided for this purpose. 

For a general introduction to .NET exception handling, please see the <span>.NET Framework referenc</span>e. 
## See Also

[AdgDataSet Class](adg-dataset-class.html)<br />[Database File Records and 
						AdgDataSet](database-file-recordsand-adg-dataset.html)<br />[Efficient File Access](efficient-file-access.html)<br />[FileAdapter Class](/reference/datagate/datagate-client/file-adapter.html)<br />[Reading and Writing to Database 
						Files](readingand-writingto-database-files.html)<br />[Using the FileAdapter Class](usingthe-file-adapter-class.html)   

