---
layout: post
title: Appearance-Settings | WindowsForms | Syncfusion
description: appearance settings
platform: WindowsForms
control: StatusBarAdv
documentation: ug
---

# Appearance Settings

You can enhance the appearance of the StatusBarAdv control by using the following properties.

## Style

StatusBarAdv supports Office2016 styles such as Office2016Colorful,Office2016White,Office2016Black and Office2016DarkGray.

//Sample code for setting "Office2016 Colorful" style for StatusBarAdv

{% tabs %}
{% highlight c# %}

this.statusBarAdv1.Style = Syncfusion.Windows.Forms.Tools.StatusbarStyle.Office2016White;

{% endhighlight  %}

{% highlight vb %}

Me.statusBarAdv1.Style = Syncfusion.Windows.Forms.Tools.StatusbarStyle.Office2016White;

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img117.png)

## Background settings

You can customize the StatusBarAdv control's background by using the various options provided in the BackgroundColor property as follows.

Property Table

<table>
<tr>
<th>
StatusBarAdv Property</th><th>
Description</th></tr>
<tr>
<td>
BackgroundColor</td><td>
Gets or sets the background gradient and other styles.</td></tr>
<tr>
<td>
Style</td><td>
Specifies the brush style.Solid,Pattern andGradient.</td></tr>
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
VerticalGradient</td><td>
Indicates whether the gradient is vertical.</td></tr>
<tr>
<td>
GradientColors</td><td>
Specifies the gradient colors.The first entry in this list is same as the BackColor property, the last entry is same as the ForeColor property.</td></tr>
<tr>
<td>
MetroColor</td><td>
Gets or sets the Metro color of the StatusBarAdv</td></tr>
<tr>
<td>
UseMetroColorAsBorder</td><td>
Gets or sets whether to set MetroColor as its Border color.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

//To set the Background color of the StatusBarAdv
this.statusBarAdv1.BackgroundColor = new Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.PathRectangle, Color.NavajoWhite, Color.IndianRed);

//To set the MetroColor in StatusBarAdv
this.statusBarAdv1.MetroColor = ColorTranslator.FromHtml("#16a5dc");

//To set the MetroColor as Border of the StatusBarAdv
this.statusBarAdv1.UseMetroColorAsBorder = true;

{% endhighlight %}

{% highlight vb %}

'To set the Background color of the StatusBarAdv
Me.statusBarAdv1.BackgroundColor = New Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.PathRectangle, Color.NavajoWhite, Color.IndianRed)

'To set the MetroColor in StatusBarAdv
Me.statusBarAdv1.MetroColor = ColorTranslator.FromHtml("#16a5dc")

'To set the MetroColor as Border of the StatusBarAdv
Me.statusBarAdv1.UseMetroColorAsBorder = True

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img64.jpeg) 

![](Overview_images/Overview_img65.png) 

## Sizing grip

A sizing grip can be displayed for the StatusBarAdv control using the property given below.

Property Table

<table>
<tr>
<th>
StatusBarAdv Property</th><th>
Description</th></tr>
<tr>
<td>
SizingGrip</td><td>
Indicates if the sizing grip is visible.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.statusBarAdv1.SizingGrip = true;

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdv1.SizingGrip = True

{% endhighlight %}
{% endtabs %}

SizingGrip property when set will display a grip at the bottom right of the control as displayed in the below image.

![](Overview_images/Overview_img66.jpeg) 
