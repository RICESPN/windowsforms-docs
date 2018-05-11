---
layout: post
title: How-to-add-Grid-Control-inside-the-SplitterControl | WindowsForms | Syncfusion
description: how to add grid control inside the splittercontrol
platform: WindowsForms
control: Splitter
documentation: ug
---

# How to add Grid control inside the SplitterControl

The SplitterControl can be embedded with Grid control and the following code example allows addition of a Grid inside the SplitterControl.

{% tabs %}

{% highlight C# %}



private Syncfusion.Windows.Forms.Grid.GridControl gridControl1;

this.gridControl1 = new Syncfusion.Windows.Forms.Grid.GridControl();

this.gridControl1.ColCount = 10;

this.gridControl1.RowCount = 100;

this.splitterControl1.Controls.Add(this.gridControl1);

{% endhighlight %}

{% highlight VB %}



Private WithEvents gridControl1 As GridControl

Me.gridControl1 = New Syncfusion.Windows.Forms.Grid.GridControl()

Me.gridControl1.ColCount = 10

Me.gridControl1.RowCount = 100

Me.splitterControl1.Controls.Add(Me.gridControl1)

{% endhighlight %}

{% endtabs %}