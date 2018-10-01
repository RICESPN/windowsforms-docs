---
layout: post
title: Border-Settings | WindowsForms | Syncfusion
description: border settings
platform: WindowsForms
control: StatusBarAdvPanel
documentation: ug
---

# Border Settings

This section illustrates the border settings available for the StatusBarAdvPanel control.

The border settings for the StatusBarAdvPanel control can be set through the properties listed below.

Property Table

<table>
<tr>
<th>
StatusBarAdvPanel Property</th><th>
Description</th></tr>
<tr>
<td>
Border3DStyle</td><td>
Indicates the style of the 3D border. The options included are as follows.RaisedOuter,SunkenOuter,RaisedInner,SunkenInner,Raised,Etched,Bump,Sunken,Adjust andFlat.</td></tr>
<tr>
<td>
BorderColor</td><td>
Indicates the color of the 2D border.</td></tr>
<tr>
<td>
BorderSingle</td><td>
Indicates the 2D border style. The options included are as follows.Dotted,Dashed,Solid,Inset,Outset andNone.</td></tr>
<tr>
<td>
BorderSides</td><td>
Indicates the border sides of the control. The options included are given below.Left,Top,Right,Bottom,Middle andAll.</td></tr>
<tr>
<td>
BorderStyle</td><td>
Indicates whether the panel should have a border. The options included are given below.FixedSingle,Fixed3D andNone.</td></tr>
</table>

N> The BorderColor and BorderSingle properties will have effect only when the BorderStyle property is set to 'FixedSingle'.

{% tabs %}
{% highlight c# %}

this.statusBarAdv1.Border3DStyle = System.Windows.Forms.Border3DStyle.RaisedInner;
this.statusBarAdv1.BorderColor = System.Drawing.Color.DarkRed;
this.statusBarAdv1.BorderSingle = System.Windows.Forms.ButtonBorderStyle.Dashed;
this.statusBarAdv1.BorderStyle = System.Windows.Forms.BorderStyle.FixedSingle;
this.statusBarAdv1.BorderSides = System.Windows.Forms.Border3DSide.All;

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdv1.Border3DStyle = System.Windows.Forms.Border3DStyle.RaisedInner
Me.statusBarAdv1.BorderColor = System.Drawing.Color.DarkRed
Me.statusBarAdv1.BorderSingle = System.Windows.Forms.ButtonBorderStyle.Dashed
Me.statusBarAdv1.BorderStyle = System.Windows.Forms.BorderStyle.FixedSingle
Me.statusBarAdv1.BorderSides = System.Windows.Forms.Border3DSide.All

{% endhighlight %}
{% endtabs %}

User can also set the other options available to the properties and monitor the difference in appearance.

![](Overview_images/Overview_img88.jpeg) 
