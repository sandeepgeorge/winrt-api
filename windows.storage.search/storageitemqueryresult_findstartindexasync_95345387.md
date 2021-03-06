---
-api-id: M:Windows.Storage.Search.StorageItemQueryResult.FindStartIndexAsync(System.Object)
-api-type: winrt method
---

<!-- Method syntax
public Windows.Foundation.IAsyncOperation<uint> FindStartIndexAsync(System.Object value)
-->

# Windows.Storage.Search.StorageItemQueryResult.FindStartIndexAsync

## -description
Retrieves the index of the item from the query results that most closely matches the specified property value. The property that is matched is determined by the first [SortEntry](sortentry.md) of the [QueryOptions.SortOrder](queryoptions_sortorder.md) list.

## -parameters
### -param value
The property value to match when searching the query results. The property to that is used to match this value is the property in the first [SortEntry](sortentry.md) of the [QueryOptions.SortOrder](queryoptions_sortorder.md) list.

## -returns
When this method completes successfully it returns the index of the matched item in the query results.

## -remarks

## -examples
This example shows how to find the first item that has an album title that begins with an "R" in a set of query results that contains albums sorted by title.

```csharp

QueryOptions queryOptions = new QueryOptions();
queryOptions.FolderDepth = FolderDepth.Deep;
queryOptions.IndexerOption = IndexerOption.OnlyUseIndexer;
SortEntry album = new SortEntry();
album.AscendingOrder = true;
album.PropertyName = "System.Music.AlbumTitle";
queryOptions.SortOrder.Add(album);

StorageFolderQueryResult queryResult = musicFolder.CreateItemQueryWithOptions(queryOptions);
var firstIndex = await queryResult.FindStartIndexAsync("R");
```

```javascript
var queryOptions = new Windows.Storage.Search.QueryOptions();
queryOptions.folderDepth = Windows.Storage.Search.FolderDepth.deep;
queryOptions.indexerOption = Windows.Storage.Search.IndexerOptions.onlyUseIndexer;
queryOptions.sortOrder.append({
 ascendingOrder: true,
 propertyName: "System.Music.AlbumTitle"
});

var queryResult = Windows.Storage.KnownFolders.picturesLibrary.createFolderQueryWithOptions(queryOptions);
var firstIndex = queryResult.findStartIndexAsync("R");
```



## -see-also
