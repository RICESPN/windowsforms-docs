---
layout: post
title: What-are-the-events-fired-when-the-group-is-expand | Windows Forms | Syncfusion
description: what are the events fired when the group is expanded / expanding?
platform: windowsforms
control: GridGrouping
documentation: ug
---

# What are the Events Fired when the Group is Expanded or Expanding

Following are the events fired when the group is expanding or expanded.

{% tabs %}
{% highlight c# %}

//Shows the GroupExpanding event.
private void gridGroupingControl1_GroupExpanding(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
//Shows all the records in the group, which is being Expanded.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Expanding event "+r.Info);
    }
}

//Shows the GroupExpanded event.
private void gridGroupingControl1_GroupExpanded(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
//Shows all the records in the group, which has expanded.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Expanded event "+r.Info);
    }
}

{% endhighlight  %}

{% highlight vb %}

//Shows the GroupExpanding event.
private void gridGroupingControl1_GroupExpanding(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
// Shows all the records in the group, which is being Expanded.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Expanding event "+r.Info);
    }
}

//Shows the GroupExpanded event.
private void gridGroupingControl1_GroupExpanded(object sender, Syncfusion.Grouping.GroupEventArgs e)
{
//Shows all the records in the group, which has expanded.
    foreach(Record r in e.Group.Records)
    {
        Console.WriteLine("Expanded event "+r.Info);
    }
}

{% endhighlight  %}
{% endtabs %}