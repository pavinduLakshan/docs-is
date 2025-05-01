# Managing Permissions with APIs

The following section describes the [RemoteAuthorizationManager API](https://localhost:9443/services/RemoteAuthorizationManagerService?wsdl) and the operations that come with it.

## About permissions 

- A permission is an **authorization** to perform a specific **action** on a **resource**. For instance, a user role can have permission (authorization) to add and delete (actions) service providers (resource). 
- The following set of actions can be performed on a resource. 
    <table>
      <tr>
        <td>
          <ul>
            <li>get</li>
            <li>add</li>
            <li>delete</li>
            <li>edit</li>
            <li>login</li>
          </ul>
        </td>
        <td>
          <ul>
            <li>man_config</li>
            <li>man_lc_config</li>
            <li>man_sec</li>
            <li>up_serv</li>
            <li>man_serv</li>
            <li>man_media</li>
          </ul>
        </td>
        <td>
          <ul>
            <li>mon_sys</li>
            <li>del_id</li>
            <li>authorize</li>
            <li>inv_ser</li>
            <li>ui_execute</li>
          </ul>
        </td>
        <td>
          <ul>
            <li>subscribe</li>
            <li>publish</li>
            <li>consume</li>
            <li>change_permission</li>
            <li>browse</li>
          </ul>
        </td>
        <td>
          <ul>
            <li>sqs_send_message</li>
            <li>sqs_receive_message</li>
            <li>sqs_delete_message</li>
            <li>sqs_change_message_visibility</li>
            <li>sqs_get_queue_attributes</li>
          </ul>
        </td>
      </tr>
    </table>
  - Permissions can be assigned to user roles. 

The following operations are available in this API.

## API operations

### authorizeRole

<table>
  <tr>
    <th>Description</th>
    <td>This operation authorizes the given role to perform the specified action on the given resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName</code>: This is the name of the role, e.g. <code>role1</code>.</li>
        <li><code>resourceId</code>: This is the resource path, e.g., <code>/permission/admin/login</code>.</li>
        <li><code>action</code>: This is the name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:authorizeRole&gt;
 &lt;!­­--Optional:­­--&gt;
 &lt;ser:roleName&gt;role1&lt;/ser:roleName&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:authorizeRole&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Invalid data provided</li>
        <li>Error in connection rollback</li>
        <li>Error! DB error occurred while checking is existing system role for : <code>roleName</code> & tenant id : <code>tenantId</code></li>
        <li>Error! Error occurred while getting UI permission ID for resource id : <code>resourceId</code> & action : <code>action</code> </li>
        <li>Error! Error occurred while adding UI permission ID for resource id : <code>resourceId</code> & action : <code>action</code></li>
        <li>Error! Using sql : <code>sqlStmt</code></li>
        <li>Error! Error while authorizing role: roleName in permission tree for resource id: <code>resourceId</code> for action: <code>action</code></li>
        <li>Error! Error while denying role: roleName in permission tree for resource id: <code>resourceId</code> for action: <code>action</code></li>
      </ul>
    </td>
  </tr>
</table>

### clearAllRoleAuthorization

<table>
  <tr>
    <th>Description</th>
    <td>This operation clears all authorizations of the role.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName</code>: This is the name of the role, e.g., <code>role1</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
 &lt;soapenv:Header/&gt;
 &lt;soapenv:Body&gt;
  &lt;ser:clearAllRoleAuthorization&gt;
   &lt;!­­--Optional:­­--&gt;
   &lt;ser:roleName&gt;role1&lt;/ser:roleName>
  &lt;/ser:clearAllRoleAuthorization&gt;
 &lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error occurred while clearing role authorizations for role : <code>roleName</code></li>
      </ul>
    </td>
  </tr>
</table>

### clearResourceAuthorizations

<table>
  <tr>
    <th>Description</th>
    <td>This operation clears all the authorizations for the given resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>resourceId</code>: This is the resource path, e.g., <code>/permission/admin/login</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:clearResourceAuthorizations&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId&gt;
&lt;/ser:clearResourceAuthorizations&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error occurred while clearing resource authorizations for resource id : <code>resourceId</code></li>
      </ul>
    </td>
  </tr>
</table>

### clearRoleActionOnAllResources

<table>
  <tr>
    <th>Description</th>
    <td>This operation removes the authorization from the role to perform the specified action on all the resources.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>action</code>: This is the action name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:clearRoleActionOnAllResources&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:clearRoleActionOnAllResources&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error occurred while clearing role action on all resources for role : <code>roleName</code> & action : <code>action</code></li>
      </ul>
    </td>
  </tr>
</table>

### clearRoleAuthorization

<table>
  <tr>
    <th>Description</th>
    <td>This operation clears the authorization of the specified role to perform the given action on the resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName  </code>: This is the name of the role, e.g., <code>role1"</code>.</li>
        <li><code>resourceId</code>: This is the resource path e.g., <code>/permission/admin/login</code>.</li>
        <li><code>action</code>: This is the action name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:clearRoleAuthorization&gt;
 &lt;!­­--Optional:­­--&gt;
 &lt;ser:roleName&gt;role1&lt;/ser:roleName&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId>
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:clearRoleAuthorization&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error occurred while clearing role authorizations for role : <code>roleName</code> + & resource id : <code>resourceId</code> & action : <code>action</code></li>
      </ul>
    </td>
  </tr>
</table>

### denyRole

<table>
  <tr>
    <th>Description</th>
    <td>This operation removes the authorization of the role to perform the given action on the specified resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName  </code>: This is the name of the role, e.g., <code>role1</code>.</li>
        <li><code>resourceId</code>: This is the resource path, e.g., <code>/permission/admin/login</code>.</li>
        <li><code>action</code>: This is the action name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:denyRole&gt;
 &lt;!­­--Optional:­­--&gt;
 &lt;ser:roleName&gt;role1&lt;/ser:roleName&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:denyRole&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>No response on success</td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Invalid data provided</li>
      </ul>
    </td>
  </tr>
</table>

### getAllowedRolesForResource

<table>
  <tr>
    <th>Description</th>
    <td>This operation retrieves the list of authorized roles to perform the given action on the specified resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>resourceId</code>: This is the resource path, e.g., <code>/permission/admin/login</code>.</li>
        <li><code>action</code>: This is the action name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:getAllowedRolesForResource&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:getAllowedRolesForResource&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"&gt;
&lt;soapenv:Body&gt;
&lt;ns:getAllowedRolesForResourceResponse xmlns:ns="http://service.ws.um.carbon.wso2.org"
xmlns:ax2599="http://core.user.carbon.wso2.org/xsd"
xmlns:ax2600="http://api.user.carbon.wso2.org/xsd"&gt;
 &lt;ns:return&gt;admin&lt;/ns:return&gt;
 &lt;ns:return&gt;myrole&lt;/ns:return&gt;
&lt;/ns:getAllowedRolesForResourceResponse&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error loading authorizations. Please check the database. Error message is + <code>errorMessage</code></li>
        <li>Error! Error while authorizing role: <code>roleName</code> in permission tree for resource id: <code>resourceId</code> for action: <code>action</code></li>
        <li>Error! Error while denying role: <code>roleName</code> in permission tree for resource id: resourceId for action: <code>action</code></li>
      </ul>
    </td>
  </tr>
</table>

### getAllowedUIResourcesForUser

<table>
  <tr>
    <th>Description</th>
    <td>This operation retrieves the list of UI resources in the specified root patch for which the user has authorization.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>userName</code>: This is the username of the specific user, e.g., <code>admin</code>.</li>
        <li><code>permissionRootPath</code>: This is the permission root path.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:getAllowedUIResourcesForUser&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:userName&gt;admin&lt;/ser:userName&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:permissionRootPath&gt;/&lt;/ser:permissionRootPath&gt;
&lt;/ser:getAllowedUIResourcesForUser&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"&gt;
&lt;soapenv:Body&gt;
&lt;ns:getAllowedUIResourcesForUserResponse xmlns:ns="http://service.ws.um.carbon.wso2.org"
xmlns:ax2599="http://core.user.carbon.wso2.org/xsd"
xmlns:ax2600="http://api.user.carbon.wso2.org/xsd"&gt;
 &lt;ns:return&gt;/permission&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/admin/configure/&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/admin/login/&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/admin/manage/&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/admin/monitor/&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/protected/&lt;/ns:return&gt;
 &lt;ns:return&gt;/permission/testlogin/&lt;/ns:return&gt;
&lt;/ns:getAllowedRolesForResourceResponse&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Invalid Permission root path provided</li>
        <li>Error loading authorizations. Please check the database. Error message is <code>message</code></li>
      </ul>
    </td>
  </tr>
</table>

### getAllowedUIResourcesForRole

<table>
  <tr>
    <th>Description</th>
    <td>This function retrieves the list of UI resources in the specified root path for a given role. </td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName</code>: The name of the specific role, e.g., <code>admin</code>.</li>
        <li><code>permissionRootPath</code>: The permission root path.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
    <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ser="http://service.ws.um.carbon.wso2.org">
      &lt;soapenv:Header/&gt;
      &lt;soapenv:Body&gt;
          &lt;ser:getAllowedUIResourcesForRole&gt;
            &lt;ser:roleName&gt;admin&lt;/ser:roleName&gt;
            &lt;ser:permissionRootPath&gt;/&lt;/ser:permissionRootPath&gt;
          &lt;/ser:getAllowedUIResourcesForRole&gt;
      &lt;/soapenv:Body&gt;
    &lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>
  <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   &lt;soapenv:Body>
      &lt;ns:getAllowedUIResourcesForRoleResponse xmlns:ns="http://service.ws.um.carbon.wso2.org" xmlns:ax2716="http://core.user.carbon.wso2.org/xsd" xmlns:ax2717="http://api.user.carbon.wso2.org/xsd">
         &lt;ns:return&gt;/permission&lt;/ns:return&gt;
         &lt;ns:return&gt;/permission/admin/configure/security/usermgt&lt;/ns:return&gt;
         &lt;ns:return&gt;/permission/admin/login&lt;/ns:return&gt;
         &lt;ns:return&gt;/permission/admin/manage/identity/applicationmgt&lt;/ns:return&gt;
      &lt;/ns:getAllowedUIResourcesForRoleResponse&gt;
   &lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;
</code></pre>
    </td>
  </tr>
  </table>

### isRoleAuthorized

<table>
  <tr>
    <th>Description</th>
    <td>This operation checks whether the given role is authorized to perform the action on the specified resource.</td>
  </tr>
  <tr>
    <th>Input Parameters</th>
    <td>
      <ul>
        <li><code>roleName</code>: This is the name of the role, e.g., <code>role1</code>.</li>
        <li><code>resourceId</code>: This is the resource path, e.g., <code>/permission/admin/login</code>.</li>
        <li><code>action</code>: This is the action name of the action to be performed on the resource, e.g., <code>ui.execute</code>.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Request</th>
    <td>
      <div style="width: 100%; display: block; overflow: auto;">
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:ser="http://service.ws.um.carbon.wso2.org"&gt;
&lt;soapenv:Header/&gt;
&lt;soapenv:Body&gt;
&lt;ser:isRoleAuthorized&gt;
 &lt;!­­--Optional:­­--&gt;
 &lt;ser:roleName&gt;role1&lt;/ser:roleName&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:resourceId&gt;/permission/admin/login&lt;/ser:resourceId&gt;
 &lt;!--­­Optional:­­--&gt;
 &lt;ser:action&gt;ui.execute&lt;/ser:action&gt;
&lt;/ser:isRoleAuthorized&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </div>
    </td>
  </tr>
  <tr>
    <th>Response</th>
    <td>
      <pre><code>&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"&gt;
&lt;soapenv:Body&gt;
&lt;ns:isRoleAuthorized xmlns:ns="http://service.ws.um.carbon.wso2.org"&gt;
 &lt;ns:return&gt;false&lt;/ns:return&gt;
&lt;/ns:isRoleAuthorized&gt;
&lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;</code></pre>
    </td>
  </tr>
  <tr>
    <th>Error Codes</th>
    <td>
      <ul>
        <li>Error loading authorizations. Please check the database. Error message is + <code>errorMessage</code></li>
      </ul>
    </td>
  </tr>
</table>
