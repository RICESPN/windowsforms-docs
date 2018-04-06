---
layout: post
title: Common questions in Essential Grid
description: how to hide a row or column
platform: windowsforms
control: Grid
documentation: ug
---

# How to hide a row or column

You can hide rows and columns using grid.Model.Rows.Hidden collection and grid.Model.Cols.Hidden collection. You can hide or show a range of columns or rows using grid.Model.HideCols.SetRange or grid.Model.HideRows.SetRange.

{% tabs %}
{% highlight c# %}
//Hides row 2.
this.grid.Model.Rows.Hidden[2] = true; 

//Hides column 3.
this.grid.Model.Cols.Hidden[3] = true; 

//Hides cols 1-3.
this.grid.Model.HideCols.SetRange(1, 3, true); 

{% endhighlight %}

{% highlight vb %}

'Hides row 2. 
Me.grid.Model.Rows.Hidden(2) = True 

'Hides column 3.
Me.grid.Model.Cols.Hidden(3) = True 

'Hides cols 1-3.
Me.grid.Model.HideCols.SetRange(1, 3, True) 

{% endhighlight %}
{% endtabs %}
