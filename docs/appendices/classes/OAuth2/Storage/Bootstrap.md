
# Bootstrap





* Full name: `\OAuth2\Storage\Bootstrap`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DYNAMODB_PHP_VERSION`|public| |&#039;none&#039;|

## Properties


### instance



```php
protected static $instance
```



* This property is **static**.


***

### mysql



```php
private $mysql
```






***

### sqlite



```php
private $sqlite
```






***

### postgres



```php
private $postgres
```






***

### mongo



```php
private $mongo
```






***

### mongoDb



```php
private $mongoDb
```






***

### redis



```php
private $redis
```






***

### cassandra



```php
private $cassandra
```






***

### configDir



```php
private $configDir
```






***

### dynamodb



```php
private $dynamodb
```






***

### couchbase



```php
private $couchbase
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### getInstance



```php
public static getInstance(): mixed
```



* This method is **static**.








***

### getSqlitePdo



```php
public getSqlitePdo(): mixed
```












***

### getPostgresPdo



```php
public getPostgresPdo(): mixed
```












***

### getPostgresDriver



```php
public getPostgresDriver(): mixed
```












***

### getMemoryStorage



```php
public getMemoryStorage(): mixed
```












***

### getRedisStorage



```php
public getRedisStorage(): mixed
```












***

### testRedisConnection



```php
private testRedisConnection(\Predis\Client $redis): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$redis` | **\Predis\Client** |  |





***

### getMysqlPdo



```php
public getMysqlPdo(): mixed
```












***

### getMongo



```php
public getMongo(): mixed
```












***

### getMongoDb



```php
public getMongoDb(): mixed
```












***

### testMongoConnection



```php
private testMongoConnection(\MongoClient $mongo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mongo` | **\MongoClient** |  |





***

### testMongoDBConnection



```php
private testMongoDBConnection(\MongoDB\Client $mongo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mongo` | **\MongoDB\Client** |  |





***

### getCouchbase



```php
public getCouchbase(): mixed
```












***

### testCouchbaseConnection



```php
private testCouchbaseConnection(\Couchbase $couchbase): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$couchbase` | **\Couchbase** |  |





***

### getCassandraStorage



```php
public getCassandraStorage(): mixed
```












***

### testCassandraConnection



```php
private testCassandraConnection(\phpcassa\Connection\ConnectionPool $cassandra): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cassandra` | **\phpcassa\Connection\ConnectionPool** |  |





***

### removeCassandraDb



```php
private removeCassandraDb(): mixed
```












***

### createCassandraDb



```php
private createCassandraDb(\OAuth2\Storage\Cassandra $storage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\Cassandra** |  |





***

### createSqliteDb



```php
private createSqliteDb(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### removeSqliteDb



```php
private removeSqliteDb(): mixed
```












***

### createMysqlDb



```php
private createMysqlDb(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### removeMysqlDb



```php
private removeMysqlDb(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### createPostgresDb



```php
private createPostgresDb(): mixed
```












***

### populatePostgresDb



```php
private populatePostgresDb(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### removePostgresDb



```php
private removePostgresDb(): mixed
```












***

### runPdoSql



```php
public runPdoSql(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### getSqliteDir



```php
public getSqliteDir(): mixed
```












***

### getConfigDir



```php
public getConfigDir(): mixed
```












***

### createCouchbaseDB



```php
private createCouchbaseDB(\Couchbase $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db` | **\Couchbase** |  |





***

### clearCouchbase



```php
private clearCouchbase(\Couchbase $cb): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cb` | **\Couchbase** |  |





***

### createMongo



```php
private createMongo(\MongoDB $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db` | **\MongoDB** |  |





***

### removeMongo



```php
public removeMongo(\MongoDB $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db` | **\MongoDB** |  |





***

### createMongoDB



```php
private createMongoDB(\MongoDB\Database $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db` | **\MongoDB\Database** |  |





***

### removeMongoDB



```php
public removeMongoDB(\MongoDB\Database $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db` | **\MongoDB\Database** |  |





***

### createRedisDb



```php
private createRedisDb(\OAuth2\Storage\Redis $storage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\Redis** |  |





***

### getTestPublicKey



```php
public getTestPublicKey(): mixed
```












***

### getTestPrivateKey



```php
private getTestPrivateKey(): mixed
```












***

### getDynamoDbStorage



```php
public getDynamoDbStorage(): mixed
```












***

### getDynamoDbClient



```php
private getDynamoDbClient(): mixed
```












***

### deleteDynamoDb



```php
private deleteDynamoDb(\Aws\DynamoDb\DynamoDbClient $client, mixed $prefix = null, mixed $waitForDeletion = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client` | **\Aws\DynamoDb\DynamoDbClient** |  |
| `$prefix` | **mixed** |  |
| `$waitForDeletion` | **mixed** |  |





***

### createDynamoDb



```php
private createDynamoDb(\Aws\DynamoDb\DynamoDbClient $client, mixed $prefix = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client` | **\Aws\DynamoDb\DynamoDbClient** |  |
| `$prefix` | **mixed** |  |





***

### populateDynamoDb



```php
private populateDynamoDb(mixed $client, mixed $prefix = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client` | **mixed** |  |
| `$prefix` | **mixed** |  |





***

### getEnvVar



```php
private getEnvVar(mixed $var, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$default` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
