---
layout: post
title: How to prevent closing of docked window
description: How to prevent closing of docked window
platform: WindowsForms
control: DockingManager
documentation: ug
---

# How to prevent closing of docked window?

This can be done in the DockVisibilityChanging event. When the end users tries to change the docking control visibility, this event will be handled. The members of this event is as follows.


<table>
<tr>
<th>
Members</th><th>
Description</th></tr>
<tr>
<td>
Cancel</td><td>
This property gets / sets the value indicating whether the event should be canceled.</td></tr>
<tr>
<td>
Control</td><td>
Gets the control which is undergoing the transfer.</td></tr>
</table>




{% highlight C# %}


private void dockingManager1_DockVisibilityChanging(object sender, Syncfusion.Windows.Forms.Tools.DockVisibilityChangingEventArgs arg)

{

    arg.Cancel = true;

}

{% endhighlight %}




{% highlight vbnet %}



Private Sub dockingManager1_DockVisibilityChanging(ByVal sender As Object, ByVal arg As Syncfusion.Windows.Forms.Tools.DockVisibilityChangingEventArgs) Handles dockingManager1.DockVisibilityChanging

    arg.Cancel = True

End Sub

{% endhighlight %}


Additionally, the dock visibility of a control can be retrieved using GetDockVisibility method by passing the control as the parameter. Also DockVisibility can be set for the controls using SetDockVisibility method.

