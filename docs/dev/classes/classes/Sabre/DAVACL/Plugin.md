***

# Plugin

SabreDAV ACL Plugin.

This plugin provides functionality to enforce ACL permissions.
ACL is defined in RFC3744.

In addition it also provides support for the {DAV:}current-user-principal
property, defined in RFC5397 and the {DAV:}expand-property report, as
defined in RFC3253.

* Full name: `\Sabre\DAVACL\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../DAV/ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`R_PARENT`|public| |1|
|`R_RECURSIVE`|public| |2|
|`R_RECURSIVEPARENTS`|public| |3|

## Properties


### server

Reference to server object.

```php
protected \Sabre\DAV\Server $server
```






***

### principalCollectionSet

List of urls containing principal collections.

```php
public array $principalCollectionSet
```

Modify this if your principals are located elsewhere.




***

### hideNodesFromListings

By default nodes that are inaccessible by the user, can still be seen
in directory listings (PROPFIND on parent with Depth: 1).

```php
public bool $hideNodesFromListings
```

In certain cases it's desirable to hide inaccessible nodes. Setting this
to true will cause these nodes to be hidden from directory listings.




***

### principalSearchPropertySet

This list of properties are the properties a client can search on using
the {DAV:}principal-property-search report.

```php
public array $principalSearchPropertySet
```

The keys are the property names, values are descriptions.




***

### adminPrincipals

Any principal uri's added here, will automatically be added to the list
of ACL's. They will effectively receive {DAV:}all privileges, as a
protected privilege.

```php
public array $adminPrincipals
```






***

### allowUnauthenticatedAccess

The ACL plugin allows privileges to be assigned to users that are not
logged in. To facilitate that, it modifies the auth plugin's behavior
to only require login when a privileged operation was denied.

```php
public bool $allowUnauthenticatedAccess
```

Unauthenticated access can be considered a security concern, so it's
possible to turn this feature off to harden the server's security.




***

### defaultAcl

The default ACL rules.

```php
protected array $defaultAcl
```

These rules are used for nodes that don't implement IACL. These default
set of rules allow anyone to do anything, as long as they are
authenticated.




***

### principalMembershipCache

This array holds a cache for all the principals that are associated with
a single principal.

```php
protected array $principalMembershipCache
```






***

## Methods


### getFeatures

Returns a list of features added by this plugin.

```php
public getFeatures(): array
```

This list is used in the response of a HTTP OPTIONS request.










***

### getMethods

Returns a list of available methods for a given url.

```php
public getMethods(string $uri): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using Sabre\DAV\Server::getPlugin










***

### getSupportedReportSet

Returns a list of reports this plugin supports.

```php
public getSupportedReportSet(string $uri): array
```

This will be used in the {DAV:}supported-report-set property.
Note that you still need to subscribe to the 'report' event to actually
implement them






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### checkPrivileges

Checks if the current user has the specified privilege(s).

```php
public checkPrivileges(string $uri, array|string $privileges, int $recursion = self::R_PARENT, bool $throwExceptions = true): bool
```

You can specify a single privilege, or a list of privileges.
This method will throw an exception if the privilege is not available
and return true otherwise.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$privileges` | **array&#124;string** |  |
| `$recursion` | **int** |  |
| `$throwExceptions` | **bool** | if set to false, this method won&#039;t throw exceptions |




**Throws:**

- [`NeedPrivileges`](./Exception/NeedPrivileges.md)

- [`NotAuthenticated`](../DAV/Exception/NotAuthenticated.md)



***

### getCurrentUserPrincipal

Returns the standard users' principal.

```php
public getCurrentUserPrincipal(): string|null
```

This is one authoritative principal url for the current user.
This method will return null if the user wasn't logged in.










***

### getCurrentUserPrincipals

Returns a list of principals that's associated to the current
user, either directly or through group membership.

```php
public getCurrentUserPrincipals(): array
```












***

### setDefaultAcl

Sets the default ACL rules.

```php
public setDefaultAcl(array $acl): mixed
```

These rules are used for all nodes that don't implement the IACL interface.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$acl` | **array** |  |





***

### getDefaultAcl

Returns the default ACL rules.

```php
public getDefaultAcl(): array
```

These rules are used for all nodes that don't implement the IACL interface.










***

### getPrincipalMembership

Returns all the principal groups the specified principal is a member of.

```php
public getPrincipalMembership(string $mainPrincipal): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mainPrincipal` | **string** |  |





***

### principalMatchesPrincipal

Find out of a principal equals another principal.

```php
public principalMatchesPrincipal(string $checkPrincipal, string $currentPrincipal = null): bool
```

This is a quick way to find out whether a principal URI is part of a
group, or any subgroups.

The first argument is the principal URI you want to check against. For
example the principal group, and the second argument is the principal of
which you want to find out of it is the same as the first principal, or
in a member of the first principal's group or subgroups.

So the arguments are not interchangeable. If principal A is in group B,
passing 'B', 'A' will yield true, but 'A', 'B' is false.

If the second argument is not passed, we will use the current user
principal.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$checkPrincipal` | **string** |  |
| `$currentPrincipal` | **string** |  |





***

### getSupportedPrivilegeSet

Returns a tree of supported privileges for a resource.

```php
public getSupportedPrivilegeSet(string|\Sabre\DAV\INode $node): array
```

The returned array structure should be in this form:

[
   [
      'privilege' => '{DAV:}read',
      'abstract'  => false,
      'aggregates' => []
   ]
]

Privileges can be nested using "aggregates". Doing so means that
if you assign someone the aggregating privilege, all the
sub-privileges will automatically be granted.

Marking a privilege as abstract means that the privilege cannot be
directly assigned, but must be assigned via the parent privilege.

So a more complex version might look like this:

[
   [
      'privilege' => '{DAV:}read',
      'abstract'  => false,
      'aggregates' => [
         [
             'privilege'  => '{DAV:}read-acl',
             'abstract'   => false,
             'aggregates' => [],
         ]
      ]
   ]
]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **string&#124;\Sabre\DAV\INode** |  |





***

### getFlatPrivilegeSet

Returns the supported privilege set as a flat list.

```php
final public getFlatPrivilegeSet(string|\Sabre\DAV\INode $node): array
```

This is much easier to parse.

The returned list will be index by privilege name.
The value is a struct containing the following properties:
  - aggregates
  - abstract
  - concrete



* This method is **final**.


**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **string&#124;\Sabre\DAV\INode** |  |





***

### getAcl

Returns the full ACL list.

```php
public getAcl(string|\Sabre\DAV\INode $node): array
```

Either a uri or a INode may be passed.

null will be returned if the node doesn't support ACLs.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **string&#124;\Sabre\DAV\INode** |  |





***

### getCurrentUserPrivilegeSet

Returns a list of privileges the current user has
on a particular node.

```php
public getCurrentUserPrivilegeSet(string|\Sabre\DAV\INode $node): array
```

Either a uri or a DAV\INode may be passed.

null will be returned if the node doesn't support ACLs.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **string&#124;\Sabre\DAV\INode** |  |





***

### getPrincipalByUri

Returns a principal based on its uri.

```php
public getPrincipalByUri(string $uri): string|null
```

Returns null if the principal could not be found.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### principalSearch

Principal property search.

```php
public principalSearch(array $searchProperties, array $requestedProperties, string $collectionUri = null, string $test = &#039;allof&#039;): array
```

This method can search for principals matching certain values in
properties.

This method will return a list of properties for the matched properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$searchProperties` | **array** | The properties to search on. This is a<br />key-value list. The keys are property<br />names, and the values the strings to<br />match them on. |
| `$requestedProperties` | **array** | this is the list of properties to<br />return for every match |
| `$collectionUri` | **string** | the principal collection to search on.<br />If this is ommitted, the standard<br />principal collection-set will be used |
| `$test` | **string** | &quot;allof&quot; to use AND to search the<br />properties. &#039;anyof&#039; for OR. |


**Return Value:**

This method returns an array structure similar to
Sabre\DAV\Server::getPropertiesForPath. Returned
properties are index by a HTTP status code.




***

### initialize

Sets up the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This method is automatically called by the server class.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### beforeMethod

Triggered before any method is handled.

```php
public beforeMethod(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### beforeBind

Triggered before a new node is created.

```php
public beforeBind(string $uri): mixed
```

This allows us to check permissions for any operation that creates a
new node, such as PUT, MKCOL, MKCALENDAR, LOCK, COPY and MOVE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### beforeUnbind

Triggered before a node is deleted.

```php
public beforeUnbind(string $uri): mixed
```

This allows us to check permissions for any operation that will delete
an existing node.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### beforeUnlock

Triggered before a node is unlocked.

```php
public beforeUnlock(string $uri, \Sabre\DAV\Locks\LockInfo $lock): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$lock` | **\Sabre\DAV\Locks\LockInfo** |  |





***

### propFind

Triggered before properties are looked up in specific nodes.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### propPatch

This method intercepts PROPPATCH methods and make sure the
group-member-set is updated correctly.

```php
public propPatch(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### report

This method handles HTTP REPORT requests.

```php
public report(string $reportName, mixed $report, mixed $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reportName` | **string** |  |
| `$report` | **mixed** |  |
| `$path` | **mixed** |  |





***

### httpAcl

This method is responsible for handling the 'ACL' event.

```php
public httpAcl(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### principalMatchReport

The principal-match report is defined in RFC3744, section 9.3.

```php
protected principalMatchReport(string $path, \Sabre\DAVACL\Xml\Request\PrincipalMatchReport $report): mixed
```

This report allows a client to figure out based on the current user,
or a principal URL, the principal URL and principal URLs of groups that
principal belongs to.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$report` | **\Sabre\DAVACL\Xml\Request\PrincipalMatchReport** |  |





***

### expandPropertyReport

The expand-property report is defined in RFC3253 section 3.8.

```php
protected expandPropertyReport(string $path, \Sabre\DAVACL\Xml\Request\ExpandPropertyReport $report): mixed
```

This report is very similar to a standard PROPFIND. The difference is
that it has the additional ability to look at properties containing a
{DAV:}href element, follow that property and grab additional elements
there.

Other rfc's, such as ACL rely on this report, so it made sense to put
it in this plugin.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$report` | **\Sabre\DAVACL\Xml\Request\ExpandPropertyReport** |  |





***

### expandProperties

This method expands all the properties and returns
a list with property values.

```php
protected expandProperties(array $path, array $requestedProperties, int $depth): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **array** |  |
| `$requestedProperties` | **array** | the list of required properties |
| `$depth` | **int** |  |





***

### principalSearchPropertySetReport

principalSearchPropertySetReport.

```php
protected principalSearchPropertySetReport(string $path, \Sabre\DAVACL\Xml\Request\PrincipalSearchPropertySetReport $report): mixed
```

This method responsible for handing the
{DAV:}principal-search-property-set report. This report returns a list
of properties the client may search on, using the
{DAV:}principal-property-search report.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$report` | **\Sabre\DAVACL\Xml\Request\PrincipalSearchPropertySetReport** |  |





***

### principalPropertySearchReport

principalPropertySearchReport.

```php
protected principalPropertySearchReport(string $path, \Sabre\DAVACL\Xml\Request\PrincipalPropertySearchReport $report): mixed
```

This method is responsible for handing the
{DAV:}principal-property-search report. This report can be used for
clients to search for groups of principals, based on the value of one
or more properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$report` | **\Sabre\DAVACL\Xml\Request\PrincipalPropertySearchReport** |  |





***

### aclPrincipalPropSetReport

aclPrincipalPropSet REPORT.

```php
protected aclPrincipalPropSetReport(string $path, \Sabre\DAVACL\Xml\Request\AclPrincipalPropSetReport $report): mixed
```

This method is responsible for handling the {DAV:}acl-principal-prop-set
REPORT, as defined in:

https://tools.ietf.org/html/rfc3744#section-9.2

This REPORT allows a user to quickly fetch information about all
principals specified in the access control list. Most commonly this
is used to for example generate a UI with ACL rules, allowing you
to show names for principals for every entry.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$report` | **\Sabre\DAVACL\Xml\Request\AclPrincipalPropSetReport** |  |





***

### htmlActionsPanel

This method is used to generate HTML output for the
DAV\Browser\Plugin. This allows us to generate an interface users
can use to create new calendars.

```php
public htmlActionsPanel(\Sabre\DAV\INode $node, string& $output): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |
| `$output` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


## Inherited methods


### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getFeatures

This method should return a list of server-features.

```php
public getFeatures(): array
```

This is for example 'versioning' and is added to the DAV: header
in an OPTIONS response.










***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $path): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### getSupportedReportSet

Returns a list of reports this plugin supports.

```php
public getSupportedReportSet(string $uri): array
```

This will be used in the {DAV:}supported-report-set property.
Note that you still need to subscribe to the 'report' event to actually
implement them






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


***
> Automatically generated on 2025-03-15
