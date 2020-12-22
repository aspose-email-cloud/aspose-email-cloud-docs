---
title: "Storage"
type: docs
url: /reference-storage-api/
weight: 1
---

This is a **storage operations controller**.



## GetDiscUsage

Get disc usage. 
Returns [**DiscUsage**](/email/reference-model-disc-usage/) model. Requires:

{{< expand-list title="request" >}}

GetDiscUsage method request. Type: [**GetDiscUsageRequest**](/email/reference-model-get-disc-usage-request/).

{{< tabs tabTotal="6" tabID="get_disc_usage_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new GetDiscUsageRequest
{ 
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
GetDiscUsageRequest request = Models.getDiscUsageRequest()
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.GetDiscUsageRequest(
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = GetDiscUsageRequest.new(
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.GetDiscUsageRequest()
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::GetDiscUsageRequest()
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="get_disc_usage_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.Storage.GetDiscUsageAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
DiscUsage result = api.cloudStorage().storage().getDiscUsage(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.storage.get_disc_usage(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.storage.get_disc_usage(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.storage.getDiscUsage(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->storage()->getDiscUsage($request);
```

{{< /tab >}}

{{< /tabs >}}
## GetFileVersions

Get file versions. 
Returns [**FileVersions**](/email/reference-model-file-versions/) model. Requires:

{{< expand-list title="request" >}}

GetFileVersions method request. Type: [**GetFileVersionsRequest**](/email/reference-model-get-file-versions-request/).

{{< tabs tabTotal="6" tabID="get_file_versions_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new GetFileVersionsRequest
{ 
    Path = "/storage/path/to/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
GetFileVersionsRequest request = Models.getFileVersionsRequest()
    .path("/storage/path/to/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.GetFileVersionsRequest(
    path='/storage/path/to/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = GetFileVersionsRequest.new(
    path: '/storage/path/to/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.GetFileVersionsRequest()
    .path('/storage/path/to/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::GetFileVersionsRequest()
    ->path('/storage/path/to/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="get_file_versions_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.Storage.GetFileVersionsAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
FileVersions result = api.cloudStorage().storage().getFileVersions(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.storage.get_file_versions(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.storage.get_file_versions(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.storage.getFileVersions(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->storage()->getFileVersions($request);
```

{{< /tab >}}

{{< /tabs >}}
## ObjectExists

Check if file or folder exists. 
Returns [**ObjectExist**](/email/reference-model-object-exist/) model. Requires:

{{< expand-list title="request" >}}

ObjectExists method request. Type: [**ObjectExistsRequest**](/email/reference-model-object-exists-request/).

{{< tabs tabTotal="6" tabID="object_exists_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new ObjectExistsRequest
{ 
    Path = "/storage/path/to/folder/or/file.ext",
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ObjectExistsRequest request = Models.objectExistsRequest()
    .path("/storage/path/to/folder/or/file.ext")
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.ObjectExistsRequest(
    path='/storage/path/to/folder/or/file.ext',
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = ObjectExistsRequest.new(
    path: '/storage/path/to/folder/or/file.ext',
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.ObjectExistsRequest()
    .path('/storage/path/to/folder/or/file.ext')
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::ObjectExistsRequest()
    ->path('/storage/path/to/folder/or/file.ext')
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="object_exists_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.Storage.ObjectExistsAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
ObjectExist result = api.cloudStorage().storage().objectExists(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.storage.object_exists(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.storage.object_exists(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.storage.objectExists(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->storage()->objectExists($request);
```

{{< /tab >}}

{{< /tabs >}}
## Exists

Check if storage exists. 
Returns [**StorageExist**](/email/reference-model-storage-exist/) model. Requires:

{{< expand-list title="request" >}}

Exists method request. Type: [**StorageExistsRequest**](/email/reference-model-storage-exists-request/).

{{< tabs tabTotal="6" tabID="storage_exists_2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var request = new StorageExistsRequest
{ 
    StorageName = "First Storage"
};
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageExistsRequest request = Models.storageExistsRequest()
    .storageName("First Storage")
    .build();
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
request = models.StorageExistsRequest(
    storage_name='First Storage')
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
request = StorageExistsRequest.new(
    storage_name: 'First Storage')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let request = Models.StorageExistsRequest()
    .storageName('First Storage')
    .build();
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$request = Models::StorageExistsRequest()
    ->storage_name('First Storage')
    ->build();
```

{{< /tab >}}

{{< /tabs >}}

{{< /expand-list >}}

{{< tabs tabTotal="6" tabID="storage_exists_1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Ruby" tabName5="Typescript" tabName6="PHP" >}}

{{< tab tabNum="1" >}}

```csharp
var result = await api.CloudStorage.Storage.ExistsAsync(request);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
StorageExist result = api.cloudStorage().storage().exists(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
result = api.cloud_storage.storage.exists(request)
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
result = api.cloud_storage.storage.exists(request)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
let result = await api.cloudStorage.storage.exists(request);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```php
$result = $api->cloudStorage()->storage()->exists($request);
```

{{< /tab >}}

{{< /tabs >}}

## More APIs

{{< list-of-articles-in-this-section >}}

