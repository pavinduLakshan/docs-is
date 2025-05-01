# Default Ports of WSO2 Products

This page describes the default ports that are used for each WSO2 product when the port offset is 0. If you are running multiple WSO2 products on the same server, you must set the `offset` value in the `<IS_HOME>/repository/conf/deployment.toml` file to a different value for each product so that there are no port conflicts.

``` toml
[server]
offset = <PORT_OFFSET_VALUE>
```

For example, if you are running two WSO2 products on the same server, and you set the port offset to `1` in one product and `2` in the second product, the management console port will be changed from the default of `9443` to `9444` in the first product and to `9445` in the second product. See [here](#change-the-offset-for-default-ports) for more information on changing the offset.

## Common ports

The following ports are common to all WSO2 products that provide the given feature. Some features are bundled in the WSO2 Carbon platform itself and therefore are available in all WSO2 products by default.

## Console ports

WSO2 products that provide a WSO2 IS console use the following servlet transport ports:

- `9443` - HTTPS servlet transport (the default URL of the WSO2 IS console is `https://localhost:9443/console`)
- `9763` - HTTP servlet transport


<!-- TODO ## JMX monitoring ports

WSO2 Carbon platform uses TCP ports to monitor a running Carbon instance using a JMX client such as JConsole. By default, JMX is enabled in all products. To disable it, see [Disable JMX for the server]({{base_path}}/deploy/monitor/jmx-based-monitoring/#disable-jmx-for-the-server).

- `11111` - RMIRegistry port. Used to monitor Carbon remotely
- `9999` - RMIServer port. Used along with the RMIRegistry port when Carbon is monitored from a JMX client that is behind a firewall-->


## Clustering ports

To cluster any running Carbon instance, either one of the following ports must be opened.

- `45564` - Opened if the membership scheme is multicast
- `4000` - Opened if the membership scheme is wka

## Random ports

Certain ports are randomly opened during server startup. This is due to specific properties and configurations that become effective when the product is started. Note that the IDs of these random ports will change every time the server is started.

- A random TCP port will open at server startup because of the `-Dcom.sun.management.jmxremote` property set in the server startup script. This property is used for the JMX monitoring facility in JVM.
- A random UDP port is opened at server startup due to the log4j appender `Syslog Appender`, which is configured in the `<IS_HOME>/repository/conf/log4j2.properties` file.

    ``` xml
    # Uncomment the below lines to use the Syslog Appender
    #appender.syslog.type = Syslog
    #appender.syslog.name = Syslog
    #appender.syslog.host = localhost
    #appender.syslog.port = 514
    #appender.syslog.layout.type = PatternLayout
    #appender.syslog.layout.pattern = [%d] [%tenantId] %5p {% raw %}{%c}{% endraw %} - %mm%ex%n
    #appender.syslog.filter.threshold.type = ThresholdFilter
    #appender.syslog.filter.threshold.level = DEBUG
    ```

## WSO2 Identity Server ports

WSO2 IS also opens the following additional ports.

- `8000` - `KDCServerPort` : the port on which KDC (Kerberos Key Distribution Center) server runs
- `10500` - `ThriftEntitlementReceivePort`

## Change the offset for default ports

When you run multiple {{product_name}} instances, you need to change their default ports with a port offset. Port offset defines the number by which all ports defined in the runtime (such as for HTTP/HTTPS) will be changed. 

!!! note

    The default HTTP and HTTPS ports for {{product_name}} are 9763 and 9443 respectively.

For example, if the port offset is 1, the HTTP and HTTPS ports will change to 9764 and 9444 respectively. For each additional instance, you need to set the port offset with a unique value. The default port offset is 0.

There are two ways to set an offset to a port:

- Pass the port offset to the server during startup. The following command starts the server with the default port incremented by 3.

    ```
    ./wso2server.sh -DportOffset=3
    ```

- Set the `offset` value in the `<IS_HOME>/repository/conf/deployment.toml` file as follows:

    ``` toml
    [server]
    offset = <PORT_OFFSET_VALUE>
    ```

Usually, when you offset the port, all the ports are shifted by that offset automatically. The following table indicates the changes that occur when the offset value is modified.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>WSO2 Server instance</p></td>
<td><p>PortOffset</p></td>
<td><p>Sample Default Port Value</p></td>
</tr>
<tr class="even">
<td><p>WSO2 Product 1</p></td>
<td><p>0</p></td>
<td><p>9443</p></td>
</tr>
<tr class="odd">
<td><p>WSO2 Product 2</p></td>
<td><p>1</p></td>
<td><p>9444</p></td>
</tr>
<tr class="even">
<td><p>WSO2 Product 3</p></td>
<td><p>2</p></td>
<td><p>9445</p></td>
</tr>
<tr class="odd">
<td><p>WSO2 Product 4</p></td>
<td><p>3</p></td>
<td><p>9446</p></td>
</tr>
<tr class="even">
<td><p>WSO2 Product 5</p></td>
<td><p>4</p></td>
<td><p>9447</p></td>
</tr>
</tbody>
</table>
