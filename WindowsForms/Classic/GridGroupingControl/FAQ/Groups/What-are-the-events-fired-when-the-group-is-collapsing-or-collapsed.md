---
layout: post
title: What-are-the-events-fired-when-the-group-is-collap | Windows Forms | Syncfusion
description: what are the events fired when the group is collapsing or collapsed
platform: windowsforms
control: GridGrouping
documentation: ug
---

# What are the Events Fired when the Group is Collapsing or Collapsed

Following are the events triggered when the group is collapsing or collapsed.

{% tabs %}
{% highlight c# %}

//Shows the GroupCollapsing event.
private void gridGroupingControl1_GroupCollapsing(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
//Shows all the records in the group, which is being collapsed.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Collapsing event "+r.Info);
    }
}

//Shows the GroupCollapsed event.
private void gridGroupingControl1_GroupCollapsed(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
//Shows all the records in the group which has collapsed.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Collapsed event "+r.Info);
    }
}

{% endhighlight  %}

{% highlight vb %}

'Shows the GroupCollapsed events.
Private Sub gridGroupingControl1_GroupCollapsed(ByVal sender As Object, ByVal e As Syncfusion.Grouping.GroupEventArgs) Handles 
gridGroupingControl1.GroupCollapsed()
For Each r As Record In e.Group.Records
    Console.WriteLine("Collapsed event " + r.Info)
Next r
End Sub

'Shows the GroupCollapsing events.
Private Sub gridGroupingControl1_GroupCollapsing(ByVal sender As Object, ByVal e As Syncfusion.Grouping.GroupEventArgs) Handles 
gridGroupingControl1.GroupCollapsing()
For Each r As Record In e.Group.Records
    Console.WriteLine("Collapsing event " + r.Info)
Next r
End Sub

{% endhighlight  %}
{% endtabs %}