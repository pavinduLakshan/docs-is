The elements in the above configuration are described below:

<table>
    <tr class="even">
        <td><strong>maxActive</strong></td>
        <td>This is the maximum number of active connections that can be allocated at the same time from this pool. Enter any negative value to denote an unlimited number of active connections.</td>
    </tr>
    <tr class="odd">
        <td><strong>maxWait</strong></td>
        <td>This is the maximum number of milliseconds that the pool will wait (when there are no available connections) for a connection to be returned before throwing an exception. You can enter zero or a negative value to wait indefinitely.</td>
    </tr>
    <tr class="even">
        <td><strong>minIdle</strong></td>
        <td>The minimum number of active connections that can remain idle in the pool without extra ones being created. Enter zero to create none.</td>
    </tr>
    <tr class="odd">
        <td><p><strong>testOnBorrow</strong></p></td>
        <td>This indicates whether objects will be validated before being borrowed from the pool. If the object fails to be 
        validated, it will be dropped from the pool and another attempt will be made to borrow another.</td>
    </tr>
    <tr class="even">
        <td><p><strong>defaultAutoCommit</strong></p></td>
        <td>Indicates whether to commit database changes automatically or not</td>
    </tr>
    <tr class="odd">
        <td><strong>validationInterval</strong></td>
        <td>This is the indication to avoid excess validation and only run validation after the specified frequency (time in milliseconds). If a connection is due for validation, but has been validated previously within this interval, it will not be validated again.</td>
    </tr>
    <tr class="even">
        <td><strong>defaultAutoCommit</strong></td>
        <td><div class="content-wrapper">
        <p>This property is <strong>not</strong> applicable to the carbon database in WSO2 Identity Server because auto committing is usually handled at the code level, i.e., the default auto commit configuration specified for the RDBMS driver will be effective instead of this property element. Typically, auto committing is enabled for RDBMS drivers by default.</p>
        <p>When auto committing is enabled, each SQL statement will be committed to the database as an individual transaction, as opposed to committing multiple statements as a single transaction.</p>
        </td>
    </tr>
</table>

!!! info 
    For more information on other parameters that can be defined in
    the `<IS_HOME>/repository/conf/deployment.toml` file, see [Tomcat JDBC Connection Pool](http://tomcat.apache.org/tomcat-9.0-doc/jdbc-pool.html#Tomcat_JDBC_Enhanced_Attributes).