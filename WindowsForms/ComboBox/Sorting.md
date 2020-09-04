---
layout: post
title: Sorting behaviors | SfComboBox | WinForms | Syncfusion
description: This section explains about how the sorting of the drop-down items works in SfComboBox for Syncfusion Essential WindowsForms.
platform: windowsforms
control: SfComboBox
documentation: ug
---

# Sorting

The SfComboBox supports sorting the data either in ascending or descending order by using the [sfComboBox1.DropDownListView.View.SortDescriptors](https://help.syncfusion.com/cr/windowsforms/Syncfusion.DataSource.DataSource.html#Syncfusion_DataSource_DataSource_SortDescriptors) property. 

You can sort the data by creating the `SortDescriptor` with required name and direction and add it to the [SortDescriptors](https://help.syncfusion.com/cr/windowsforms/Syncfusion.DataSource.DataSource.html#Syncfusion_DataSource_DataSource_SortDescriptors) property.

`SortDescriptor` object holds the following three properties:

* `PropertyName`: Describes the name of the sorted property.
* `Direction`: Describes an object of type `ListSortDirection` that defines the sorting direction.
* `Comparer`: Describes the comparer to be applied when sorting the items.

{% tabs %}
{% highlight c# %}
sfComboBox1.DropDownListView.View.SortDescriptors.Add(new Syncfusion.DataSource.SortDescriptor() { PropertyName = "LongName", Direction = Syncfusion.DataSource.ListSortDirection.Descending });
{% endhighlight %}
{% highlight vb %}
sfComboBox1.DropDownListView.View.SortDescriptors.Add(New Syncfusion.DataSource.SortDescriptor() With {.PropertyName = "LongName", .Direction = Syncfusion.DataSource.ListSortDirection.Descending})
{% endhighlight %}
{% endtabs %}

![Sorted items of the drop-down](Sorting_images/Sorting_img1.png)
