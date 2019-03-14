---
layout: post
title: How-to-change-the-MDI-tab-size | WindowsForms | Syncfusion
description: how to change the mdi tab size
platform: WindowsForms
control: TabbedMDIManager
documentation: ug
---

# How to change the MDI tab size

You should handle theTabControlAdded event handler and use [ItemSize](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Tools.Windows~Syncfusion.Windows.Forms.Tools.TabControlAdv~ItemSize.html) property to change the tab size.

{% tabs %}

{% highlight C# %}



// Handle the TabControlAdded event. 

this.tabbedMDIManager.TabControlAdded += new TabbedMDITabControlEventHandler(tabbedMDIManager_TabControlAdded); 

private void tabbedMDIManager_TabControlAdded(object sender, TabbedMDITabControlEventArgs args) 

{ 

// To change the size. 

args.TabControl.ItemSize = new Size(40, 40); 

}

{% endhighlight %}

{% highlight VB %}



' Handle the TabControlAdded event. 

AddHandler tabbedMDIManager.TabControlAdded, AddressOf tabbedMDIManager_TabControlAdded

Private Sub tabbedMDIManager_TabControlAdded(ByVal sender As Object, ByVal args As TabbedMDITabControlEventArgs)

' To change the size. 

args.TabControl.ItemSize = New Size(40, 40)

End Sub


{% endhighlight %}

{% endtabs %}