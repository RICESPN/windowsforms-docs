---
layout: post
title: Overview | WindowsForms | Syncfusion
description: overview
platform: WindowsForms
control: Control Name undefined
documentation: ug
---

# MDI Child Forms

## Overview

>**Important**
Starting with v16.2.0.x, if you refer to Syncfusion assemblies from trial setup or from the NuGet feed, include a license key in your projects. Refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to learn about registering Syncfusion license key in your Windows Forms application to use our components.

This section illustrates how to create MDI Child forms using the ChildFrameBarManager.

## Assembly deployment

Refer [control dependencies](https://help.syncfusion.com/windowsforms/control-dependencies#childframebarmanager) section to get the list of assemblies or NuGet package needs to be added as reference to use the control in any application.
 
Please find more details regarding how to install the nuget packages in windows form application in the below link:
 
[How to install nuget packages](https://help.syncfusion.com/windowsforms/nuget-packages)

## Creating MDI ParentForm

Follow the steps below to create MDI parent form and MDI child form.

1. Set up an MDIParent form by setting Form.IsMdIContainer property to true.
2. Add bar items, 'Open' and 'Exit', under File menu bar using MainFrameBarManager. Refer to Creating Menus.

   ![](Overview_images/Overview_img1.jpeg)



3. Create a new form named TextEditor, with the controls FontListBox and ColorUIControl. We will consider this form as the MDIChildForm.

   ![](Overview_images/Overview_img2.jpeg)
 


4. Drag-and-Drop ChildFrameBarManager to the child form and add necessary Bar items. Adding bar items using ChildFrameBarManager is similar to MainFrameBarManager.

   ![](Overview_images/Overview_img3.jpeg)



5. Now merge the toolbars and menus of the child form with the Main form using RegisterMDIChildType function as follows.

{% highlight c# %}



this.MainFrameBarManager1.RegisterMdiChildTypes(new Type[]{typeof(TextEditorForm)});

{% endhighlight %}

{% highlight vbnet %}



Me.MainFrameBarManager1.RegisterMdiChildTypes(New Type(){GetType(TextEditorForm)})

{% endhighlight %}

A sample demonstrating the MDI feature is available in the below sample installation location.

…\_My Documents\Syncfusion\EssentialStudio\Version Number\Windows\Tools.Windows\Samples\Advanced Editor Functions\ActionGroupingDemo_

