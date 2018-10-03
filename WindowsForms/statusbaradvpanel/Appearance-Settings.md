---
layout: post
title: Appearance-Settings | WindowsForms | Syncfusion
description: appearance settings
platform: WindowsForms
control: StatusBarAdvPanel
documentation: ug
---

# Appearance Settings

The appearance of the StatusBarAdvPanel control can be enhanced using the properties given below.

## Background settings

The StatusBarAdvPanel control's background can be customized using the various options provided in the BackgroundColor property given below.

Property Table

<table>
<tr>
<th>
StatusBarAdvPanel Property</th><th>
Description</th></tr>
<tr>
<td>
BackgroundColor</td><td>
Gets / sets the background gradient and other styles.</td></tr>
<tr>
<td>
Style</td><td>
Specifies the brush style.{{ '_Solid,_' | markdownify }}{{ '_Pattern and_' | markdownify }}{{ '_Gradient._' | markdownify }}</td></tr>
<tr>
<td>
BackColor</td><td>
Specifies the back color of the control.</td></tr>
<tr>
<td>
ForeColor</td><td>
Specifies the fore color for any text or graphics in the control.</td></tr>
<tr>
<td>
PatternStyle</td><td>
Specifies the pattern style of the control.</td></tr>
<tr>
<td>
GradientBackground</td><td>
Indicates whether the background will be drawn with the gradient.</td></tr>
<tr>
<td>
GradientStyle</td><td>
Specifies the gradient style of the background.ForwardDiagonal,BackwardDiagonal,Horizontal,Vertical,PathRectangle andPathEllipse.</td></tr>
<tr>
<td>
GradientColors</td><td>
Specifies the gradient colors.The first entry in this list will be the same as the BackColor property, the last entry will be the same as the ForeColor property.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.statusBarAdvPanel1.BackgroundColor = new Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.PathRectangle, System.Drawing.Color.LavenderBlush, System.Drawing.Color.RosyBrown);

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdvPanel1.BackgroundColor = New Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.PathRectangle, System.Drawing.Color.LavenderBlush, System.Drawing.Color.RosyBrown)

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img83.jpeg) 

## Icon settings

Icons can be added to the StatusBarAdvPanels using the property given below.

Property Table

<table>
<tr>
<th>
StatusBarAdvPanel Property</th><th>
Description</th></tr>
<tr>
<td>
Icon</td><td>
Indicates the icon of the panel.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.Icon = ((System.Drawing.Icon)(resources.GetObject("$this.Icon")));

{% endhighlight %}

{% highlight vb %}

Me.Icon = DirectCast((resources.GetObject("$this.Icon")), System.Drawing.Icon)

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img84.jpeg) 
