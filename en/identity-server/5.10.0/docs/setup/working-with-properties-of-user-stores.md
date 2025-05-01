# Working with Properties of User Stores

The following table provides descriptions of the key properties you use
to configure primary user stores.

<table>
<thead>
<tr class="header">
<th><p>Property Id</p></th>
<th><p>Primary User Store Property</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>             MaxUserName<br>ListLength            </code></td>
<td><code>             max_user_name<br>_list_length        </code></td>
<td>Controls the number of users listed in the user store of a WSO2 product. This is useful when you have a large number of users and don't want to list them all. Setting this property to 0 displays all users.</td>
</tr>
<tr class="even">
<td><code>             Connection<br>URL            </code></td>
<td><code>             connection<br>_url           </code></td>
<td><p>Connection URL to the user store server. In the case of default LDAP in Carbon, the port is specified in the <code>              carbon.xml             </code> file, and a reference to that port is included in this configuration.</p></td>
</tr>
<tr class="odd">
<td><code>             Connection<br>Name            </code></td>
<td><code>             connection<br>_name           </code></td>
<td><p>The username used to connect to the database and perform various operations. This user does not have to be an administrator in the user store or have an administrator role in the WSO2 product that you are using, but this user MUST have permissions to read the user list and users' attributes and to perform search operations on the user store. The value you specify is used as the DN ( <code>              Distinguish Name             </code> ) attribute of the user. This property is mandatory.</p></td>
</tr>
<tr class="even">
<td><code>             Connection<br>Password            </code></td>
<td><code>             connection_<br>password           </code></td>
<td>Password for the <code>             ConnectionName            </code> user.</td>
</tr>
<tr class="odd">
<td><code>             Display<br>NameAttribute            </code></td>
<td><code>display_<br>name_attribute</code></td>             
<td>This is an optional property. The Display Name Attribute is the name by which users will be listed when you search for users in the management console (Go to <strong>Configuration -&gt; Users</strong> tab).</td>
</tr>
<tr class="even">
<td><code>             Password<br>HashMethod            </code></td>
<td><code>password_<br>hash_method</code></td>
<td>Password hash method to use when storing user entries in the user store.</td>
</tr>
<tr class="odd">
<td><code>             UserName<br>ListFilter            </code></td>
<td><code>              user_name_<br>list_filter </code></td>
<td><p>Filtering criteria for listing all the user entries in the user store. This query or filter is used when doing search operations on users. In this case, the search operation only provides the objects created from the specified class. This query is the same as listing out all the available users in the management console.</p></td>
</tr>
<tr class="even">
<td><code>             UserEntry<br>ObjectClass            </code></td>
<td><code>user_entry_<br>object_class</code></td>
<td>Object class used to construct user entries. By default, it is a custom object class defined with the name <code>             wso2Person            </code> .</td>
</tr>
<tr class="odd">
<td><code>             User<br>SearchBase            </code></td>
<td><code>user_<br>search_base</code></td>
<td><div class="content-wrapper">
<p>DN of the context or object under which the user entries are stored in the user store. In this case, it is the "users" container. When the user store searches for users, it will start from this location of the directory.</p>
<div>
<p>Different databases have different search bases.</p>
</div>
</div></td>
</tr>
<tr class="even">
<td><code>             UserName<br>SearchFilter            </code></td>
<td><code>user_name_<br>search_filter</code></td>
<td>Filtering criteria used to search for a particular user entry.</td>
</tr>
<tr class="odd">
<td><code>             UserName<br>Attribute            </code></td>
<td><code>user_name<br>_attribute</code></td>
<td><div class="content-wrapper">
<p>The attribute used for uniquely identifying a user entry. Users can be authenticated using their email address, UID, etc.</p>
<div>
<p>The name of the attribute is considered as the username.</p>
</div>
<p>For information on using email address to authenticate users, click <a href="(../../learn/using-email-address-as-the-username)">here</a> .</p>
</div></td>
</tr>
<tr class="odd">
<td><p><code>              PasswordJava<br>ScriptRegEx             </code></p></td>
<td><code>password_java_<br>script_regex</code></td>
<td>Policy that defines the password format.</td>
</tr>
<tr class="even">
<td><code>             UsernameJava<br>ScriptRegEx            </code></td>
<td><code>username_java_<br>script_regex</code></td>
<td>The regular expression used by the front-end components for username validation.</td>
</tr>
<tr class="odd">
<td><code>             Username<br>JavaRegEx            </code></td>
<td><code>username_<br>java_regex</code></td>
<td><div class="content-wrapper">
<p>A regular expression to validate usernames. By default, strings have a length of 5 to 30. Only non-empty characters are allowed. You can provide ranges of alphabets, numbers and also ranges of ASCII values in the RegEx properties.</p>
<div class="code panel pdl" style="border-width: 1px;">
<div class="codeContent panelContent pdl">
<div class="sourceCode" id="cb2" data-syntaxhighlighter-params="brush: xml; gutter: false; theme: Confluence" data-theme="Confluence" style="brush: xml; gutter: false; theme: Confluence"><pre class="sourceCode xml"><code class="sourceCode xml"><a class="sourceLine" id="cb2-1" title="1"><span class="kw">&lt;Property</span><span class="ot"> name=</span><span class="st">&quot;UsernameJavaRegEx&quot;</span><span class="kw">&gt;</span>[a-zA-Z0-9._\-|/]{3,30}$<span class="kw">&lt;/Property&gt;</span></a></code></pre></div>
</div>
</div>
</div></td>
</tr>
<tr class="odd">
<td><code>             ReadGroups            </code></td>
<td><code>read_groups</code></td>
<td>Specifies whether groups should be read from the user store. If this is disabled by setting it to <code>             false            </code>, none of the groups in the user store can be read, and the following group configurations are NOT mandatory: <code>             GroupSearchBase            </code>, <code>             GroupNameListFilter            </code>, or <code>             GroupNameAttribute            </code> .</td>
</tr>
<tr class="odd">
<td><code>             WriteGroups            </code></td>
<td><code>write_groups</code></td>
<td>Specifies whether groups should be written to user store.</td>
</tr>
<tr class="odd">
<td><code>             Group<br>SearchBase            </code></td>
<td><code>group_<br>search_base</code></td>
<td>DN of the context under which user entries are stored in the user store.</td>
</tr>
<tr class="odd">
<td><code>             GroupName<br>ListFilter            </code></td>
<td><code>group_name_<br>list_filter</code></td>
<td>Filtering criteria for listing all the group entries in the user store. Groups are created in LDAP using the " <code>             groupOfName            </code> " class. The group search operation only returns objects created from this class.</td>
</tr>
<tr class="even">
<td><code>             GroupEntry<br>ObjectClass            </code></td>
<td><code>group_entry_<br>object_class</code></td>
<td>Object class used to construct group entries.</td>
</tr>
<tr class="odd">
<td><code>             GroupName<br>SearchFilter            </code></td>
<td><code>group_name_<br>search_filter</code></td>
<td>Filtering criteria used to search for a particular group entry.</td>
</tr>
<tr class="even">
<td><code>             GroupName<br>Attribute            </code></td>
<td><code>group_name_<br>attribute</code></td>
<td>Attribute used for uniquely identifying a user entry. This attribute is to be treated as the group name.</td>
</tr>
<tr class="odd">
<td><code>             Membership<br>Attribute            </code></td>
<td><code>membership<br>_attribute</code></td>
<td>Attribute used to define members of groups.</td>
</tr>
<tr class="even">
<td><code>             Membership<br>AttributeRange            </code></td>
<td><code>membership_<br>attribute_range</code></td>
<td>Attribute used by Active Directories where they need limit membership attributes. The default value for this is 1500.</td>
</tr>
<tr class="odd">
<td><code>             UserRoles<br>CacheEnabled            </code></td>
<td><code>user_roles_<br>cache_enabled</code></td>
<td>This is to indicate whether to cache the role list of a user. By default this is set to <code>             true            </code> . Set it to <code>             false            </code> if the user roles are changed by external means and those changes should be instantly reflected in the Carbon instance.</td>
</tr>
<tr class="even">
<td><code>             UserDNPattern            </code></td>
<td><code>user_dn_pattern</code></td>
<td>(LDAP) The patten for the user's DN, which can be defined to improve the search. When there are many user entries in the LDAP user store, defining a <code>             UserDNPattern            </code> provides more impact on performances as the LDAP does not have to travel through the entire tree to find users.</td>
</tr>
<tr class="odd">
<td><code>             ReplaceEscape<br>Characters<br>AtUserLogin            </code></td>
<td><code>replace_escape_<br>characters_at_user_login</code></td>
<td>(LDAP) If the user name has special characters it replaces it to validate the user logging in. Only " <strong>\</strong> " and " <strong>\\</strong> " are identified as escape characters.</td>
</tr>
<tr class="odd">
<td><p><code>              Password<br>JavaRegEx             </code></p></td>
<td><code>password_<br>java_regex</code></td>
<td><p>(LDAP and JDBC) A regular expression to validate passwords. By default, strings having a length between 5 to 30 with non-empty characters are allowed.</p></td>
</tr>
<tr class="even">
<td><p><code>              PasswordJava<br>ScriptRegEx             </code></p></td>
<td><code>password_java<br>_script_regex</code></td>
<td>The regular expression used by the front-end components for password validation.</td>
</tr>
<tr class="odd">
<td><p><code>              Username<br>JavaRegEx             </code></p></td>
<td><code>username_<br>java_regex</code></td>
<td>A regular expression to validate usernames. By default, strings having a length 5 to 30 between with non-empty characters are allowed.</td>
</tr>
<tr class="even">
<td><code>             Username<br>JavaScript<br>RegEx            </code></td>
<td><code>username_java_<br>script_regex</code></td>
<td>The regular expression used by the front-end components for username validation.</td>
</tr>
<tr class="odd">
<td><p><code>              Rolename<br>JavaRegEx             </code></p></td>
<td><code>rolename_<br>java_regex</code></td>
<td>A regular expression to validate role names. By default, strings having a length between 5 to 30 with non-empty characters are allowed.</td>
</tr>
<tr class="odd">
<td><code>MultiTenant<br>Realm<br>ConfigBuilder</code></td>
<td><code>config<br>_builder</code></td>
<td>Tenant Manager specific realm config parameter. Can be used to build different types of realms for the tenant.</td>
</tr>
<tr class="odd">
<td><p><code>                             LDAPConnection<br>Timeout                           </code></p></td>
<td><code>ldap_connection<br>_timeout</code></td>
<td>If the connection to an LDAP is inactive for the length of time (in milliseconds) specified by this property, the connection will be terminated.</td>
</tr>
</tbody>
</table>
