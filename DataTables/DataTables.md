# Data Table Attributes
This article covers All about Nop Datatables
```csharp
var dataTable = new DataTablesModel
{
    Name = "Table name",
    UrlRead = new DataUrl { Url = "URL for data read (ajax)" },
    UrlDelete = new DataUrl { Url = "URL for delete action (ajax)" },
    UrlUpdate = new DataUrl { Url = "URL for update action (ajax)" },
    SearchButtonId = "Search button Id",
    Filters = new List<FilterParameter>(), // Populate with actual filters
    Data = null, // Data can be set here if not using ajax
    Processing = true,
    ServerSide = true,
    Paging = true,
    Info = true,
    RowIdBasedOnField = "field_name",
    RefreshButton = true,
    PagingType = "simple_numbers",
    Length = 10,
    LengthMenu = "[10, 25, 50, 100]",
    Dom = "<'row'<'col-md-12'tr>>" + // Example DOM structure
          "<'row'<'col-md-5'l><'col-md-7'p>>",
    Ordering = true,
    HeaderCallback = "headerCallbackFunctionName",
    DrawCallback = "drawCallbackFunctionName",
    FooterColumns = 0, // Set to the number of columns if a footer is needed
    FooterCallback = "footerCallbackFunctionName",
    IsChildTable = false, // Set to true if this is a child table
    ChildTable = null, // Set to a DataTablesModel if there is a child table
    PrimaryKeyColumn = "primary_key_column_name",
    BindColumnNameActionDelete = "bind_column_name_for_delete",
    ColumnCollection = new List<ColumnProperty>() // Populate with actual column properties
};

// Add to the view
return View(dataTable);
```

in your cshtml page:
```html
@model DataTablesModel

<!-- Table HTML structure -->
<table id="@Model.Name" class="display" style="width:100%">
    <!-- Table headers and footers would be generated here -->
</table>

<!-- DataTables initialization script -->
<script>
$(document).ready(function() {
    $('#@Model.Name').DataTable({
        // DataTables options would be set here using Model properties
    });
});
</script>

```
### All Attribute Explainations
1. **Name**: Table name.
2. **UrlRead**: URL for data read (ajax).
3. **UrlDelete**: URL for delete action (ajax).
4. **UrlUpdate**: URL for update action (ajax).
5. **SearchButtonId**: Search button Id.
6. **Filters**: Filters controls.
7. **Data**: Data for table (ajax, json, array).
8. **Processing**: Enable or disable the display of a 'processing' indicator when the table is being processed.
9. **ServerSide**: Feature control DataTables' server-side processing mode.
10. **Paging**: Enable or disable table pagination.
11. **Info**: Enable or disable information ("1 to n of n entries").
12. **RowIdBasedOnField**: If set, populate the row id based on the specified field.
13. **RefreshButton**: Enable or disable refresh button.
14. **PagingType**: Pagination button display options.
15. **Length**: Number of rows to display on a single page when using pagination.
16. **LengthMenu**: This parameter allows you to readily specify the entries in the length drop down select list that DataTables shows when pagination is enabled.
17. **Dom**: Indicates where particular features appear in the DOM.
18. **Ordering**: Feature control ordering (sorting) abilities in DataTables.
19. **HeaderCallback**: Custom render header function name(js).
20. **DrawCallback**: Custom render function name(js) that is called every time DataTables performs a draw.

21. **FooterColumns**: A number of columns to generate in a footer. Set 0 to disable footer.
22. **FooterCallback**: Custom render footer function name(js).
23. **IsChildTable**: Indicate of child table.
24. **ChildTable**: Child table.
25. **PrimaryKeyColumn**: Primary key column name for the parent table.
26. **BindColumnNameActionDelete**: Bind column name for the delete action. If this field is not specified, the default will be the alias "id" for the delete action.
27. **ColumnCollection**: Column collection.
28. **UrlRead**: URL for data read (ajax).
29. **UrlDelete**: URL for the delete action (ajax).
30. **UrlUpdate**: URL for the update action (ajax).
31. **SearchButtonId**: Search button Id.
32. **Filters**: Filters controls.
33. **Data**: Data for the table (ajax, json, array).
34. **Processing**: Enable or disable the display of a 'processing' indicator when the table is being processed.
35. **ServerSide**: Feature control DataTables' server-side processing mode.
36. **Paging**: Enable or disable table pagination.
37. **Info**: Enable or disable information ("1 to n of n entries").
38. **RowIdBasedOnField**: If set, populate the row id based on the specified field.
39. **RefreshButton**: Enable or disable the refresh button.
40. **PagingType**: Pagination button display options.
41. **Length**: Number of rows to display on a single page when using pagination.





