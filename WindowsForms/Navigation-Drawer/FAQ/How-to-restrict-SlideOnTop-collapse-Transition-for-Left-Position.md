---
layout: post
title: Restrict transition | WindowsForms | Syncfusion
description: how to restrict slideontop collapse transition for left position?
platform: WindowsForms
control: Frequently Asked Questions
documentation: ug
---

# How to restrict SlideOnTop collapse transition for left position?

This requirement can be achieved by handling the Closing Event.

**Closing event**

This [Closing](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.NavigationDrawer.html) event occurs before DrawerPanel Collapsing initialized.

{% tabs %}
{% highlight c# %}
//Disables the SlideOnTop in Left when Transition Collapses begins
void navigationDrawer1_Closing(object sender, CancelEventArgs e)
{
if (this.navigationDrawer1.Transition == Transition.SlideOnTop && this.navigationDrawer1.Position == SlidePosition.Left)
{
e.Cancel = true;
}
}
{% endhighlight %}
{% highlight VB %}
'Disables the SlideOnTop in Left when Transition Collapses begins
Private Sub navigationDrawer1_Closing(sender As Object, e As CancelEventArgs)
If Me.navigationDrawer1.Transition = Transition.SlideOnTop AndAlso Me.navigationDrawer1.Position = SlidePosition.Left Then
e.Cancel = True
End If
End Sub
{% endhighlight %}
{% endtabs %}

