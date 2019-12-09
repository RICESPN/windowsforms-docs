---
layout: post
title: Themes-and-Visual-Styles | WindowsForms | Syncfusion
description: themes and visual styles
platform: WindowsForms
control: EditorsPackage
documentation: ug
---

# Themes and Visual Styles

This section discusses themes and visual styles settings of the NumericUpDownExt control.

## Themes

Themes define the look and feel of the NumericUpDownExt control. They can be set using the property given below.

<table>
<tr>
<th>
NumericUpDownExt Property</th><th>
Description</th></tr>
<tr>
<td>
ThemesEnabled</td><td>
Specifies whether XP Themes (visual styles) should be used for this control when available.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.numericUpDownExt1.ThemesEnabled = true;                          

{% endhighlight %}

{% highlight vb %}

Me.numericUpDownExt1.ThemesEnabled = True

{% endhighlight %}
{% endtabs %}

![](Themes-and-Visual-Styles_images/Themes-and-Visual-Styles_img1.png)

## Visual styles

Visual Styles enhance the appearance of the NumericUpDownExt control and can be set using the property given below.

<table>
<tr>
<th>
NumericUpDownExt Properties</th><th>
Description</th></tr>
<tr>
<td>
VisualStyle</td><td>
Specifies the visual style of the NumericUpDownExt control. It includes the options given below.Default andOffice2007.</td></tr>
<tr>
<td>
ColorScheme</td><td>
Gets / sets Office2007Theme for Office2007 style.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2007;
this.numericUpDownExt1.ColorScheme = Syncfusion.Windows.Forms.Office2007Theme.Blue;    

{% endhighlight %}

{% highlight vb %}

Me.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2007
Me.numericUpDownExt1.ColorScheme = Syncfusion.Windows.Forms.Office2007Theme.Blue

{% endhighlight %}
{% endtabs %}
    
![](Themes-and-Visual-Styles_images/Themes-and-Visual-Styles_img2.png)

![](Themes-and-Visual-Styles_images/Themes-and-Visual-Styles_img3.png)

When the ColorScheme property is set to 'Managed', the NumericUpDownExt control can be displayed using custom colors supported by the control.

This can be done programmatically as follows.

{% tabs %}
{% highlight c# %}

this.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2007;
this.numericUpDownExt1.ColorScheme = Syncfusion.Windows.Forms.Office2007Theme.Managed;
Office2007Colors.ApplyManagedColors(this, Color.Orange);

{% endhighlight %}

{% highlight vb %}

Me.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2007
Me.numericUpDownExt1.ColorScheme = Syncfusion.Windows.Forms.Office2007Theme.Managed;
Office2007Colors.ApplyManagedColors(Me, Color.Orange)

{% endhighlight %}
{% endtabs %}

![](Themes-and-Visual-Styles_images/Themes-and-Visual-Styles_img4.png)

## Office2016 theme

NumericUpDownExt control supports Office2016 Visual styles such as Office2016Colorful,Office2016White,Office2016Black and Office2016DarkGray.

//Sample code for setting "Office2016 Colorful" style for NumericUpDownExt

{% tabs %}
{% highlight c# %}

this.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2016Colorful;

{% endhighlight %}

{% highlight vb %}

Me.numericUpDownExt1.VisualStyle = Syncfusion.Windows.Forms.VisualStyle.Office2016Colorful;

{% endhighlight %}
{% endtabs %}

![](Appearance-Settings_images/Appearance-Settings_img4.png)

N> The ThemesEnabled property should be set to 'True' for the above settings to take effect.

A sample which demonstrates the ThemesEnabled property and Office 2007 Visual Styles of TextBoxExt control is available in the below sample installation path.

…\_My Documents\Syncfusion\EssentialStudio\Version Number\Windows\Tools.Windows\Samples\Advanced Editor Functions\ActionGroupingDemo_

