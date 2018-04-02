---
layout: post
title: How-to-access-a-particular-record-from-a-table | Windows Forms | Syncfusion
description: how to access a particular record from a table
platform: windowsforms
control: GridGrouping
documentation: ug
---

# How to Access a Particular Record from a Table

This can be done using the following code snippet.

{% tabs %}
{% highlight c# %}

//Uses the record Index to access a particular record from a table.
Record r=this.gridGroupingControl1.Table.Records[RecordIndex];

{% endhighlight %}

{% highlight vb %}

'Uses the record Index to access a particular record from a table.
Dim r As Record = Me.gridGroupingControl1.Table.Records(RecordIndex)

{% endhighlight %}
{% endtabs %}
