---
layout: post
title: Exporting in GridControl
description: how to save the contents of a grid in memory rather than a file system to export to another grid
platform: windowsforms
control: Grid
documentation: ug
---

# How to save the contents of a Grid in memory rather than a file system to export to another grid

You can save the contents of a grid in memory rather than writing to a file system. This can be done using SaveSoap or SaveBinary method of GridControl. The below code snippet illustrates how this can be done.

{% tabs %}
{% highlight c# %}

MemoryStream s = new MemoryStream();
gridControl1.Model.SaveSoap(s); 
s.Position = 0;
gridControl1.Model = GridModel.LoadSoap(s);
gridControl2.Model = GridModel.LoadSoap(s);
{% endhighlight  %}

{% highlight vb %}

Dim s As MemoryStream = New MemoryStream()
gridControl1.Model.SaveSoap(s) 
s.Position = 0
gridControl1.Model = GridModel.LoadSoap(s)
gridControl2.Model = GridModel.LoadSoap(s)
{% endhighlight %}
{% endtabs %}