---
layout: post
title: Getting Started for Syncfusion ColorUIControl | WindowsForms | Syncfusion
description: Gives information about working with ColorUIControl and its basic setting by using designer and programatically
platform: WindowsForms
control: ColorUI 
documentation: ug
---

# Getting Started

ColorUIControl can be added through designer by just dragging-and-dropping it from the toolbox onto the Windows Form Designer. 

![Creating control using Designer](ColorUI_images/Overview_img226.jpeg)

It can also be created programmatically as discussed below.

1. Include the required namespace.

{% tabs %}
{% highlight c# %}

using Syncfusion.Windows.Forms.Tools;

{% endhighlight %}

{% highlight vb %}

Imports Syncfusion.Windows.Forms.Tools

{% endhighlight %}
{% endtabs %}

2. Create an instance of the ColorUIControl control class. Specify its size and add it to the form.

{% tabs %}
{% highlight c# %}

// Declaring and Initializing the control
private Syncfusion.Windows.Forms.ColorUIControl colorUIControl1;
this.colorUIControl1=new Syncfusion.Windows.Forms.ColorUIControl();

//Specify the size for the control
this.colorUIControl1.Size = new System.Drawing.Size(200, 136);
Adding ColorUIControl to the form
this.Controls.Add(this.colorUIControl1);

{% endhighlight %}

{% highlight vb %}

' Declaring and Initializing the control
Private colorUIControl1 As Syncfusion.Windows.Forms.ColorUIControl
Me.colorUIControl1 = New Syncfusion.Windows.Forms.ColorUIControl()

'Specify the size for the control
Me.colorUIControl1.Size = New System.Drawing.Size(200, 136)

' Adding ColorUIControl to the form
Me.Controls.Add(Me.colorUIControl1)

{% endhighlight %}
{% endtabs %}

   ![ColorUIControl](ColorUI_images/Overview_img227.jpeg)
