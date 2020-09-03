---
layout: post
title: Appearance Settings | WindowsForms | Syncfusion
description: Appearance Settings
platform: WindowsForms
control: TileLayout 
documentation: ug
---

# Appearance settings

## SetParentFormFlat

This [SetParentFormFlat](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.TileLayout.html#Syncfusion_Windows_Forms_Tools_TileLayout_SetParentFormFlat) property gives flat look for the the parent Form.

{% tabs %}

{% highlight C# %}

//Enables flat look for parent form

this.tileLayout1.SetParentFormFlat = true;

{% endhighlight %}


{% highlight VB %}

'Enables flat look for parent form

Me.tileLayout1.SetParentFormFlat = True

 
{% endhighlight %}

{% endtabs %}

![Tile layout customization](Appearance_images/ParentFormFlat.png)


## ShowGroupTitle

Shows the Group Title while enabling this [ShowGroupTitle](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.TileLayout.html#Syncfusion_Windows_Forms_Tools_TileLayout_ShowGroupTitle) property.

{% tabs %}

{% highlight C# %}

//Shows the Group Title

this.tileLayout1.ShowGroupTitle = true;

{% endhighlight %}

{% highlight VB %}

'Shows the Group Title

 Me.tileLayout1.ShowGroupTitle = True
 
{% endhighlight %}

{% endtabs %}

![Tile layout group title](Appearance_images/LayoutTitle.png)


## IgnoreThemeBackground

[IgnoreThemeBackground](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.Renderers.RendererInfo.html#Syncfusion_Windows_Forms_Tools_Renderers_RendererInfo_IgnoreThemeBackground) indicates whether the control will ignore the theme's background color and draw the BackColor instead. BackColor of the [TileLayout](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.TileLayout.html) will only be applied if the [IgnoreThemeBackground](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.Renderers.RendererInfo.html#Syncfusion_Windows_Forms_Tools_Renderers_RendererInfo_IgnoreThemeBackground) property is set to `true`.


{% tabs %}

{% highlight C# %}

//To apply BackColor of the TileLayout

 this.tileLayout1.IgnoreThemeBackground = true;

{% endhighlight %}

{% highlight VB %}

‘To apply BackColor of the TileLayout

 Me.tileLayout1.IgnoreThemeBackground = true
 
{% endhighlight %}

{% endtabs %}

![TileLayout back color customization](Appearance_images/ThemedBackground.png)
