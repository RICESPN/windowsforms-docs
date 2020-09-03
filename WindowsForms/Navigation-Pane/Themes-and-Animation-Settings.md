---
layout: post
title: Themes and Animation Settings | WindowsForms | Syncfusion
description: Themes and Animation Settings
platform: WindowsForms
control: GroupBar
documentation: ug
---
# Themes and animation settings

Themes define the look and feel of the whole GroupBar. It also changes the behavior of the GroupBar completely. Themes can be enabled by setting the [ThemesEnabled](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupBar.html#Syncfusion_Windows_Forms_Tools_GroupBar_ThemesEnabled) property of GroupBar to `true`.

{% tabs %}

{% highlight C# %}  

this.groupBar1.ThemesEnabled = true;

{% endhighlight %}


{% highlight VB %}

Me.groupBar1.ThemesEnabled = True

{% endhighlight %}

{% endtabs %}

![GroupBar theme enabled](Overview_images/Overview_img37.jpeg)

Themed look of Office 2007 Style GroupBar
{:.caption}

## Animation settings

Switching between the different GroupBar Items can be animated by setting the [AnimatedSelection](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupBar.html#Syncfusion_Windows_Forms_Tools_GroupBar_AnimatedSelection) property to `true`.

{% tabs %}

{% highlight C# %}

this.groupBar1.AnimatedSelection = true;

 {% endhighlight %}

 
 
{% highlight VB %}

Me.groupBar1.AnimatedSelection = true

{% endhighlight %}

{% endtabs %}

![GroupBar animation](Overview_images/Overview_img38.jpeg)
