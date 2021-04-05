---
layout: post
title: Ribbon-Form | WindowsForms | Syncfusion
description: A quick go through of RibbonForm which replaces the default form Title and Control box button to enable different Visual styles to the Ribbon
platform: WindowsForms
control: RibbonControlAdv 
documentation: ug
---

# Ribbon Form in Windows Forms

`RibbonForm` is an extension that replaces the default form to enable different Visual styles to the ribbon. This RibbonForm now gives similar look and feel of Microsoft office, to its controls.

## Appearance Settings

<table>
<tr>
<th>
Property</th><th>
Description</th></tr>
<tr>
<td>
Appearance</td><td>
Sets the appearance of the form. The values are,Normal andOffice2007 (Default)Office 2010</td></tr>
<tr>
<td>
ColorScheme</td><td>
Specifies the office color scheme of the Ribbon form. The color schemes are, Blue, Black, Silver and Managed (Default).</td></tr>
<tr>
<td>
EnableAeroTheme</td><td>
Specifies the Aero theme of the Ribbon form. </td></tr>
<tr>
<td>
Font</td><td>
Gets or sets the RibbonControlAdv Font.</td></tr>
</table>

{% tabs %}

{% highlight c# %}

//Specifies the appearance of the form
this.Appearance = AppearanceType.Office2007;

//Specifies the color scheme for the form
this.ColorScheme = ColorSchemeType.Blue;

//Specifies the Aero theme
this.EnableAeroTheme = true;

{% endhighlight %}

{% highlight vb %}

Me.Appearance = AppearanceType.Office2007

Me.ColorScheme = ColorSchemeType.Blue

Me.EnableAeroTheme = True

{% endhighlight %}

{% endtabs %}

`IsFormManager` property can be used to remove the form title bar and replace it with the RibbonControlAdv built-in system buttons.

*	Default Theme

![IsFormManager enabled](Ribbon_Form_Images/Ribbon-Form_img1.jpg)

*	Aero Theme

![Aero Theme enabled](Ribbon_Form_Images/Ribbon-Form_img2.jpg)


## Customization

The property which lets you set borders for the Office2007Style form is as follows.

<table>
<tr>
<th>
Property</th><th>
Description</th></tr>
<tr>
<td>
Borders</td><td>
Gets/sets the border values of an Office 2007 style form. Sets borders for Left, Top, Right and Bottom sides of the form.</td></tr>
</table>


{% highlight c# %}

this.Borders = new System.Windows.Forms.Padding(10);

{% endhighlight %}

{% highlight vbnet %}

Me.Borders = New System.Windows.Forms.Padding(10)

{% endhighlight %}


### Customizing the Top Left Edge

This TopLeftRadius property gets/sets the curved radius of the top left edge of the form. Default is 8.

{% highlight c# %}

this.TopLeftRadius = 20;

{% endhighlight %}

{% highlight vbnet %}

Me.TopLeftRadius = 20

{% endhighlight %}

## Adding user control to the title bar

The [`RibbonForm`](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.RibbonForm.html) allows to load any user control into the right side of the title bar by using the [`HeaderItem`](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.RibbonForm.html#Syncfusion_Windows_Forms_Tools_RibbonForm_HeaderItem) property.

The following code example illustrates how to add the header item in title bar of the RibbonForm.

{% tabs %}

{% highlight c# %}

this.button = new SfButton();
this.button.ForeColor = Color.White;
this.button.Font = Font = new System.Drawing.Font("Segoe UI Semibold", 9F);
this.button.Size = new System.Drawing.Size(75, 50);
this.button.Text = "Sign-In";
this.button.Style.BackColor = System.Drawing.Color.FromArgb(((int)(((byte)(42)))), ((int)(((byte)(120)))), ((int)(((byte)(212)))));
this.button.Style.HoverBackColor = System.Drawing.Color.FromArgb(((int)(((byte)(42)))), ((int)(((byte)(141)))), ((int)(((byte)(212)))));
this.button.Style.FocusedBackColor = System.Drawing.Color.FromArgb(((int)(((byte)(42)))), ((int)(((byte)(87)))), ((int)(((byte)(154)))));
this.button.Style.PressedBackColor = System.Drawing.Color.FromArgb(((int)(((byte)(42)))), ((int)(((byte)(87)))), ((int)(((byte)(154)))));
this.button.Style.PressedForeColor = Color.White;
this.button.Style.HoverForeColor = Color.White;
this.button.Style.FocusedForeColor = Color.White;

this.HeaderItem = button;

{% endhighlight %}

{% endtabs %}

![WindowsForms RibbonForm HeaderItem in Title Bar](Ribbon_Form_Images/WindowsForms-RibbonForm-HeaderItem-in-Title-Bar.jpg)

N>[View sample in GitHub](https://github.com/SyncfusionExamples/How-to-load-user-control-to-titlebar-of-RibbonForm)