---
layout: post
title: Appearance | WindowsForms | Syncfusion
description: appearance
platform: WindowsForms
control: MetroForm
documentation: ug
---

# Appearance

## Border thickness

MetroForm border can be customized using `BorderThickness` property.

{% tabs %}

{% highlight C# %}

this.BorderThickness = 10;

{% endhighlight %}

{% highlight VB %}

Me.BorderThickness = 10
 
{% endhighlight %}

{% endtabs %}

## Border color

`BorderColor` property is used to change the color of the border.

{% tabs %}

{% highlight C# %}

 this.BorderColor = System.Drawing.Color.FromArgb(((int)(((byte)(17)))), ((int)(((byte)(158)))), ((int)(((byte)(218)))));

{% endhighlight %}


{% highlight VB %}

 Me.BorderColor = System.Drawing.Color.FromArgb(((int)(((byte)(17)))), ((int)(((byte)(158)))), ((int)(((byte)(218)))))
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/Customization_img1.jpeg)

## Caption bar height

Caption bar height can be customized using `CaptionBarHeight` property.

{% tabs %}

{% highlight C# %}

this.CaptionBarHeight = 40;

{% endhighlight %}


{% highlight VB %}

Me.CaptionBarHeight = 40
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/Caption-Bar-Customization_img1.jpeg)

### Retain the caption bar height on maximized mode

By Default, the height of the caption bar will be reduced while form is in maximized state. To retain the height of caption bar, set `SfForm.CaptionBarHeightMode` property as `SameAlwaysOnMaximize`

{% tabs %}

{% highlight C# %}

this.CaptionBarHeightMode = Syncfusion.Windows.Forms.Enums.CaptionBarHeightMode.SameAlwaysOnMaximize;

{% endhighlight %}

{% highlight VB %}

Me.CaptionBarHeightMode = Syncfusion.Windows.Forms.Enums.CaptionBarHeightMode.SameAlwaysOnMaximize
 
{% endhighlight %}

{% endtabs %}

## Caption bar color

Caption bar color can be customized using `CaptionBarColor` property.

{% tabs %}

{% highlight C# %}

this.CaptionBarColor = Color.Pink;

{% endhighlight %}


{% highlight VB %}

Me.CaptionBarColor = Color.Pink
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/Caption-Bar-Customization_img2.jpeg)

## Caption alignment

MetroForm caption can be aligned vertically using `CaptionAlign` property.

* Left
* Center
* Right

{% tabs %}

{% highlight C# %}

this.CaptionAlign = System.Windows.Forms.HorizontalAlignment.Right;

{% endhighlight %}


{% highlight VB %}

Me.CaptionAlign = System.Windows.Forms.HorizontalAlignment.Right
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/CaptionAlign.png)

## Caption vertical alignment

MetroForm caption can be aligned vertically using `CaptionVerticalAlignment` property.

* Top
* Center
* Bottom

{% tabs %}

{% highlight C# %}

 this.CaptionVerticalAlignment = Syncfusion.Windows.Forms.VerticalAlignment.Top;

{% endhighlight %}


{% highlight VB %}

Me.CaptionVerticalAlignment = Syncfusion.Windows.Forms.VerticalAlignment.Top
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/CaptionVerticalAlignment.png)

## Icon alignment support

MetroForm supports Left, Right, and Center alignment for Icon.

{% tabs %}

{% highlight C# %}

this.IconAlign = System.Windows.Forms.HorizontalAlignment.Right;

{% endhighlight %}


{% highlight VB %}

 Me.IconAlign = System.Windows.Forms.HorizontalAlignment.Right
 
{% endhighlight %}

{% endtabs %}

![](Appearance_images/Icon Alignment.png)
 
