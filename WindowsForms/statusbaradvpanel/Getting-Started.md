---
layout: post
title: Getting Started with Windows Forms statusbaradvpanel | Syncfusion
description: Learn here about getting started with Syncfusion Windows Forms Status Bar (StatusBarAdvPanel) control and more details.
platform: WindowsForms
control: StatusBarAdvPanel
documentation: ug
---

# Getting Started in Windows Forms Status Bar (StatusBarAdvPanel)

This section will give a step by step procedure to design a StatusBarAdvPanel control through designer and also through programming approach.

## Through designer

To create a StatusBarAdvPanel control through designer,

* Drag-and-drop a StatusBarAdvPanel control from the toolbox onto the form.

  ![Create statusbaradvpanel Through Designer](Overview_images/Overview_img80.jpeg)

* Set the desired background in the properties window.
* Set the PanelType property for the control.
* You can set the StatusBarAdvPanel to have a custom border color by setting the value of the BorderColor property.
* Build and run the application.

  ![Run the Application](Overview_images/Overview_img81.jpeg) 
  
## Through code

To create a StatusBarAdvPanel programmatically,

* Open a new Visual C# or VB.NET application in Visual Studio .NET.
* Add the Syncfusion assemblies Shared.Base and Tool.Windows to your application.
* Declare the StatusBarAdvPanel control.

{% tabs %}
{% highlight c# %}

private Syncfusion.Windows.Forms.Tools.StatusBarAdvPanel statusBarAdvPanel1;

{% endhighlight %}

{% highlight vb %}

Private statusBarAdvPanel1 As Syncfusion.Windows.Forms.Tools.StatusBarAdvPanel

{% endhighlight %}
{% endtabs %}

* Initialize the control and add it to your form.

{% tabs %}
{% highlight c# %}

this.statusBarAdvPanel1 = new Syncfusion.Windows.Forms.Tools.StatusBarAdvPanel();
this.statusBarAdvPanel1.Location = new System.Drawing.Point(48, 128);
this.Controls.Add(this.statusBarAdvPanel1);

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdvPanel1 = New Syncfusion.Windows.Forms.Tools.StatusBarAdvPanel()
Me.statusBarAdvPanel1.Location = New System.Drawing.Point(48, 128)
Me.Controls.Add(Me.statusBarAdvPanel1)

{% endhighlight %}
{% endtabs %}

* Customize the control's look and feel using the properties given below.

{% tabs %}
{% highlight c# %}

this.statusBarAdvPanel1.BackgroundColor = new Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.BackwardDiagonal, System.Drawing.Color.PaleVioletRed, System.Drawing.Color.PeachPuff);
this.statusBarAdvPanel1.BorderColor = System.Drawing.Color.Black;
this.statusBarAdvPanel1.HAlign = Syncfusion.Windows.Forms.Tools.HorzFlowAlign.Left;
this.statusBarAdvPanel1.Location = new System.Drawing.Point(160, 184);
this.statusBarAdvPanel1.PanelType = Syncfusion.Windows.Forms.Tools.StatusBarAdvPanelType.LongDate;
this.statusBarAdvPanel1.Size = new System.Drawing.Size(216, 48);

{% endhighlight %}

{% highlight vb %}

Me.statusBarAdvPanel1.BackgroundColor = New Syncfusion.Drawing.BrushInfo(Syncfusion.Drawing.GradientStyle.BackwardDiagonal, System.Drawing.Color.PaleVioletRed, System.Drawing.Color.PeachPuff)
Me.statusBarAdvPanel1.BorderColor = System.Drawing.Color.Black
Me.statusBarAdvPanel1.HAlign = Syncfusion.Windows.Forms.Tools.HorzFlowAlign.Left
Me.statusBarAdvPanel1.Location = New System.Drawing.Point(160, 184)
Me.statusBarAdvPanel1.PanelType = Syncfusion.Windows.Forms.Tools.StatusBarAdvPanelType.LongDate
Me.statusBarAdvPanel1.Size = New System.Drawing.Size(216, 48)

{% endhighlight %}
{% endtabs %}

* Run the application. You will see the StatusBarAdvPanel with the date text displayed at the bottom right of the application.

  ![Create statusbaradvpanel Through Code](Overview_images/Overview_img82.jpeg) 