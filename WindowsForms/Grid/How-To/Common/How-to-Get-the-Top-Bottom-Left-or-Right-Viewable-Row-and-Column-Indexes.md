---
layout: post
title: How-to-Get-the-Top-Bottom--Left-or-Right-Viewable-row-and-column-indexes | Windows Forms | Syncfusion
description: how to get the top, bottom / left, or right viewable row and column indexes
platform: windowsforms
control: Grid
documentation: ug
---

# How to get the top, bottom or left, or right viewable row and column indexes

Use the following variables to get the viewable row and column indexes.

{% tabs %}
{% highlight c# %}

//Top Row Index.
this.grid.TopRowIndex

//Left Column Index.
this.grid.LeftColIndex

//Bottom Row Index.
this.grid.ViewLayout.LastVisibleRow

//Right Column Index.
this.grid.ViewLayout.LastVisibleCol

{% endhighlight %}

{% highlight vb %}

'Top Row Index.
Me.grid.TopRowIndex

'Left Column Index.
Me.grid.LeftColIndex

'Bottom Row Index.
Me.grid.ViewLayout.LastVisibleRow

'Right Column Index.
Me.grid.ViewLayout.LastVisibleCol

{% endhighlight %}
{% endtabs %}
