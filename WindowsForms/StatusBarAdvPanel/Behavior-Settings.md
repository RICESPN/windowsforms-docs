---
layout: post
title: Behavior-Settings | WindowsForms | Syncfusion
description: behavior settings
platform: WindowsForms
control: StatusBarAdvPanel
documentation: ug
---

# Behavior Settings

## Panel types

The format of the data in the panel can be set using the property given below.

Property Table

<table>
<tr>
<th>
StatusBarAdvPanel Property</th><th>
Description</th></tr>
<tr>
<td>
PanelType</td><td>
Indicates the type of the panel.</td></tr>
</table>


The PanelType property can be used to display predefined text representing key states, date / time or culture information.

N> Users can also specify their own text to be displayed in the control by setting the PanelType property to 'Custom'. The text to be displayed is set using the Text property of the StatusBarAdvPanel.

{% tabs %}
{% highlight c# %}

this.statusBarAdvPanel1.PanelType = Syncfusion.Windows.Forms.Tools.StatusBarAdvPanelType.NumLockState;

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdvPanel1.PanelType = Syncfusion.Windows.Forms.Tools.StatusBarAdvPanelType.NumLockState

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img86.jpeg) 

## Panel size

The StatusBarAdvPanel can be automatically resized using the property given below.

Property Table

<table>
<tr>
<th>
StatusBarAdvPanel Property</th><th>
Description</th></tr>
<tr>
<td>
SizeToContent</td><td>
Indicates if the size of the panel will be automatically calculated by the size of it's contents.</td></tr>
<tr>
<td>
PreferredSize</td><td>
Gets / sets the preferred size of the panel in the FlowLayout.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.statusBarAdvPanel1.SizeToContent = true;
this.statusBarAdvPanel1.PreferredSize = new System.Drawing.Size(99, 21);

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdvPanel1.SizeToContent = True
Me.statusBarAdvPanel1.PreferredSize = New System.Drawing.Size(99, 21)

{% endhighlight %}
{% endtabs %}

A Sample which demonstrates the Panel Types of the StatusBarAdvPanel is available in the below sample installation path.

…\My Documents\Syncfusion\EssentialStudio\Version Number\Windows\Tools.Windows\Samples\Advanced Editor Functions\ActionGroupingDemo

