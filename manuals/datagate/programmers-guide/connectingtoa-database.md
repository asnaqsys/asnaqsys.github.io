---
title: "Connecting to named Databases"
description: "Discover how to establish database connections using a name effectively. This guide covers essential techniques, tips, and best practices for developers."
---

The DataGate notions of "database source profile name" or "database name" (a registered client-side reference to a set of database connection parameters) and "database label" (the server-side identifier for database servers) are provided to help you identify and connect to a database.

The way to connect to a database is through the [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) object. DataGate provide the `AsnaConfig` class to assist in Resolving Names.

The following code fragment creates an AdgConnection object and connects to a database referred to by the name "My Local DB".

```cs 

    IDataGateConfig dgConfig;

    public void PrepareStore(params string[] configJsonFiles) 
    {
        ConfigurationBuilder builder = new ConfigurationBuilder();
        builder.AddJsonFile(AsnaConfigHelper.DefaultConfigFilePath);
        foreach (var configFile in configJsonFiles)
            builder.AddJsonFile(configFile);
        IAsnaConfig config = new AsnaConfig(builder.Build());
        dgConfig = config.DataGate;
    }

    private AdgConnection createAdgConnection(string dbName)
    {
        SourceProfile sourceProfile = dgConfig.ResolveSourceName(dbName);
        AdgConnection dbConnection = new AdgConnection(sourceProfile);
        return dbConnection;
    }


    public void start()
    {
        PrepareStore(AsnaConfigHelper.DefaultConfigFilePath, "./appsetting.json");
        . . . 
        AdgConnection dbConnection = createAdgConnection("My Local DB");
        dbConnection.Open();
        . . .
        . . .
        //Disconnects from the dataBase by closing the connection.
        dbConnection.Close();
    }

```


## See Also

[AdgConnection Class](/reference/datagate/datagate-client/adg-connection.html) <br />
[Disconnecting from a Database](disconnectingfroma-database.html)<br />


