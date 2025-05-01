# Configure clock tolerance for My Account and Cons
- For the **Console**,

    ```yaml
    [console]
    idp_configs.clockTolerance = <value_in_seconds>
    ```

- For the **My Account** portal,

    ```yaml
    [myaccount]
    idp_configs.clockTolerance = <value_in_seconds>
    ```

!!! note "Important"
    
    It is strongly recommended to synchronize the clocks of the servers or virtual machines (VM) running {{product_name}} with a Network Time Protocol (NTP) server. Time discrepancies across servers can cause issues with authentication, token validation, session expiration, and other time-sensitive operations.
