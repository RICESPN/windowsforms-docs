---
layout: post
title: Getting-Started | WindowsForms | Syncfusion
description: getting started
platform: WindowsForms
control: Splitter
documentation: ug
---

# Getting started

This section briefly describes how to design the SplitterControl in the Windows Forms application.

* Add the SplitterControl control.
* Configure the SplitterControl control.

## Add the SplitterControl

1. Create a new Windows Forms Application Project in VS IDE through the New Project Wizard.
2. Drag and drop the SplitterControl in the Form from the Toolbox.

![](Getting-Started_images/Getting-Started_img1.png)



## Configure the SplitterControl

To add SplitterControl to the Windows Forms Application through the following code example:

1. Include the namespaces Syncfusion.Windows.Forms and Syncfusion.Windows.Forms.Tools.

   {% tabs %}

   {% highlight C# %}

		//Namespaces.

		using Syncfusion.Windows.Forms.Tools;

		using Syncfusion.Windows.Forms;

   {% endhighlight %}


   {% highlight VB %}

		‘Namespaces.

		Imports Syncfusion.Windows.Forms

		Imports Syncfusion.Windows.Forms.Tools

   {% endhighlight %}

   {% endtabs %}


2. Create an instance of the SplitterControl and add it to the Form.

   {% tabs %}

   {% highlight C# %}

		//Creates the SplitterControl instance.

		SplitterControl splitterControl1=new Syncfusion.Windows.Forms.SplitterControl();

		this.Controls.Add(splitterControl1);

   {% endhighlight %}

    {% highlight VB %}

		‘Creates the SplitterControl instance.

		Dim splitterControl1 As New Syncfusion.Windows.Forms.SplitterControl()



		Me.Controls.Add(splitterControl1)

   {% endhighlight %}

   {% endtabs %}






