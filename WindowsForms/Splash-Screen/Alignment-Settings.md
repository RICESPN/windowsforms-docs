---
layout: post
title: Alignment-Settings | WindowsForms | Syncfusion
description: alignment settings
platform: WindowsForms
control: SplashControl
documentation: ug
---

# Alignment Settings

This section discusses the alignment settings available in SplashControl.

SplashControl provides options to customize the alignment of the splash image in the desktop. The property that is related to this feature is given below.

Property Table

<table>
<tr>
<th>
SplashControl Property</th><th>
Description</th></tr>
<tr>
<td>
DesktopAlignment</td><td>
Specifies the desktop alignment of the splash image. It includes the following options.SystemTray,Center,LeftTop,LeftBottom,RightTop,RightBottom andCustom.</td></tr>
</table>

This can be done through code using the code snippet below.

{% tabs %}
{% highlight c# %}

this.splashControl1.DesktopAlignment = Syncfusion.Windows.Forms.Tools.SplashAlignment.SystemTray;

{% endhighlight %}

{% highlight vb %}

Me.SplashControl1.DesktopAlignment = Syncfusion.Windows.Forms.Tools.SplashAlignment.SystemTray

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img38.jpeg) 


