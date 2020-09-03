---
layout: post
title: Helpers in WinForms DataGrid control | Syncfusion
description: Learn about helpers such as get the actual row index irrespective of grouping and so on in Syncfusion WinForms DataGrid (SfDataGrid) control and more details.
platform: WindowsForms
control: SfDataGrid 
documentation: ug
---

# Helpers in Windows Forms DataGrid (SfDataGrid) 

## IndexResolver

SfDataGrid has [DataGridIndexResolver](https://help.syncfusion.com/cr/windowsforms/Syncfusion.WinForms.DataGrid.DataGridIndexResolver.html) static class present in [Syncfusion.WinForms.DataGrid](https://help.syncfusion.com/cr/windowsforms/Syncfusion.WinForms.DataGrid.html) namespace that has some extension methods used to Resolve from row or column index to record or visible column index and `vice versa`. 

## Example: You can find the record index from row index using ResolveToRecordIndex method.

`Prototype Table`

<table>
<tr>
<th>
ProtoType</th><th>
Description</th></tr>
<tr>
<td>
ResolveToRecordIndex(int rowIndex)</td><td>
Resolves Record index from the RowIndex. When RowIndex does not find any records it returns -1. RecordIndex denotes the index of Record in <code>SfDataGrid.View.Records</code></td></tr>
<tr>
<td>
ResolveToRowIndex(int recordIndex)</td><td>
Resolves RowIndex from the record index associated with <code>SfDataGrid.View.Records</code>. When record index is lesser than 0 it returns the -1.</td></tr>
<tr>
<td>
ResolveToRowIndex(object recordItem)</td><td>
Resolves row index from the record associated with <code>SfDataGrid.View.Records</code>. When the given record is not available in the collection it returns -1.</td></tr>
<tr>
<td>
ResolveStartIndexOfGroup(Group group)</td><td>
Resolves the start index of group in DataGrid associated with <code>SfDataGrid.View.TopLevelGroup</code>. When there is no group in DataGrid it returns -1.</td></tr>
<tr>
<td>
ResolveToGridVisibleColumnIndex(int visibleColumnIndex)</td><td>
Resolves the GridColumn index from the visible column index. It excludes the <code>RowHeader</code> and <code>IndentColumn</code>.</td></tr>
<tr>
<td>
ResolveStartIndexBasedOnPosition()</td><td>
Resolves the start index based on position. It includes the <code>stacked header</code> also. By default it returns 0.</td></tr>
<tr>
<td>
ResolveToScrollColumnIndex(int gridColumnIndex)</td><td>
Resolves column index from the Grid column index associated with <code>SfDataGrid.Columns</code>. It includes the <code>IndentColumn</code> and <code>RowHeader</code> also.</td></tr>
<tr>
<td>
ResolveToStartColumnIndex()</td><td>
Returns start column index of the VisibleColumn. </td></tr>
<tr>
<td>
GetDetailsViewDataGridRowIndex(DetailsViewDataGrid detailsViewDataGrid)</td><td>
Returns the RowIndex of DetailsViewGrid. You can pass the <code>DetailsViewDataGrid</code> as argument. When the DetailsView is not found it returns the -1.</td></tr>
<tr>
<td>
GetTableSummaryCount(VerticalPosition position)</td><td>
Returns the TableSummary count from <code>VerticalPosition.Position</code>. </td></tr>
<tr>
<td>
GetHeaderIndex()</td><td>
Returns the header row index.</td></tr>
<tr>
<td>
IsInDetailsViewIndex(int rowIndex)</td><td>
Decides whether the given row index is <code>DetailsView</code> index or not.</td></tr>
<tr>
<td>
IsAddNewIndex(int rowIndex)</td><td>
Decides whether the given row index is <code>AddNewRow</code> index or not.</td></tr>
<tr>
<td>
IsTableSummaryIndex(int rowIndex)</td><td>
Decides whether the given row index is <code>TableSummary</code> index or not.</td></tr>
<tr>
<td>
IsFilterRowIndex(int rowIndex)</td><td>
Decides whether the given row index is <code>FilterRow</code> index or not.</td></tr>
</table>


## Dispose

The method is associated with relinquishes memory and clears all references associated with SfDataGrid. When you call this method, it releases all the reference for SfDataGrid. So the memory it is occupying using the DataGrid is reclaimed. You have to call `SfDataGrid.Dispose` method to release the memory.

