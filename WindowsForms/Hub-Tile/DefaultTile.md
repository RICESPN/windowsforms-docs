---
layout: post
title: DefaultTile | WindowsForms | Syncfusion
description: defaulttile
platform: WindowsForms
control: HubTile
documentation: ug
---
# DefaultTile

This type provides notification through various transition effects.

## Key properties

* [Title](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~Title.html) - The title can be displayed at the top of the hub tile.
* [Footer](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~Footer.html) - The footer can be displayed at the bottom of the hub tile.
* [ImageSource](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~ImageSource.html) - An image can be displayed in the background of the hub tile.

The following code example shows the usage of the [Title](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~Title.html), [Footer](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~Footer.html), and [ImageSource](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~ImageSource.html) properties.

{% tabs %}

{% highlight C# %}  

this.HubTile1.Title.Text  = "This is the title area. Display your image here”;

this.HubTile1.Title.TextColor  = Color.White;

this.HubTile1.Footer.Text = "HubTile";

this.HubTile1.Footer.TextColor  = Color.White;

this.HubTile1.ImageSource  = this.ImageListAdv1.Images[0];

{% endhighlight %}

{% highlight VB %} 

Me.HubTile1.Title.Text = "This is the title area. Display your image here”

Me.HubTile1.Title.TextColor  = Color.White

Me.HubTile1.Footer.Text = "HubTile"

Me.HubTile1.Footer.TextColor  = Color.White

Me.HubTile1.ImageSource  = Me.ImageListAdv1.Images(0)

{% endhighlight %}

{% endtabs %}

 ![Default Tile](Concept-and-Features_images/Concept-and-Features_img1.png) 
 
 Default Tile
 {:.caption}
 
## Transition effects

In HubTile, image transition can be performed at specified intervals and in different directions just like the Windows 8 live tiles. They include the following transition effects.

* Bottom-to-Top
* Top-to-Bottom
* Left-to-Right
* Right-to-Left

HubTile image transition direction can be modified using the [SlideTransition](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~SlideTransition.html) property.


{% tabs %}

{% highlight C# %} 

this.HubTile1.TileType = HubTileType.DefaultTile;

this.HubTile1.TurnLiveTileOn = true;

this.HubTile1.SlideTransition = TransitionDirection.BottomToTop;

 {% endhighlight %}

 
{% highlight VB %} 

Me.HubTile1.TileType = HubTileType.DefaultTile

Me.HubTile1.TurnLiveTileOn = True

Me.HubTile1.SlideTransition = TransitionDirection.LeftToRight

{% endhighlight %}

{% endtabs %}

 ![Slide tansition](Concept-and-Features_images/Concept-and-Features_img2.png)
 


## Transition speed

In HubTile, image transition speed can be increased or decreased by using [ImageTransitionSpeed](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.HubTile~ImageTransitionSpeed.html) property.

{% tabs %}

{% highlight C# %} 

this.HubTile1.ImageTransitionSpeed = 3;

 {% endhighlight %}

{% highlight VB %} 

Me.HubTile1.ImageTransitionSpeed = 3

{% endhighlight %}

{% endtabs %}