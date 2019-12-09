---
layout: post
title: How-to-get-the-row-position-of-AddNewRecord-in-Gri | Windows Forms | Syncfusion
description: how to get the row position of addnewrecord in gridgroupingcontrol
platform: windowsforms
control: GridGrouping
documentation: ug
---

# How to Get the Row Position of AddNewRecord in GridGroupingControl

You can get the row index of AddNewRecord using SourceListRecordChanged event handler. In the event handler, you can check e.Action property and get row position from FilteredRecordsCollection.

{% tabs %}
{% highlight c# %}

void gridGroupingControl1_SourceListRecordChanged(object sender, RecordChangedEventArgs e)
{
    if (e.Action == RecordChangedType.Added)
    {
        int offset = gridGroupingControl1.TableControl.GetMinimumTopRowIndex();
        int newRowIndex = e.TableListChangedEventArgs.Table.FilteredRecords.IndexOf(e.Record) + offset;
        Console.WriteLine(newRowIndex);
    }
}

{% endhighlight %}

{% highlight vb %}

Private Sub gridGroupingControl1_SourceListRecordChanged(ByVal sender As Object, ByVal e As RecordChangedEventArgs)
If e.Action = RecordChangedType.Added Then
Dim offset As Integer = gridGroupingControl1.TableControl.GetMinimumTopRowIndex()
Dim newRowIndex As Integer = e.TableListChangedEventArgs.Table.FilteredRecords.IndexOf(e.Record) + offset
Console.WriteLine(newRowIndex)
End If
End Sub

{% endhighlight %}
{% endtabs %}
