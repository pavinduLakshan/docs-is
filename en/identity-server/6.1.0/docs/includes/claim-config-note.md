    The dialects configured in the `<IS_HOME>/repository/conf/claim-config.xml` file get applied only **when you start the product** for the first time or for any newly created tenants.
        
    With the first startup, dialects and claims are loaded from the file and persisted in the database. Any consecutive updates to the file will not be picked up.