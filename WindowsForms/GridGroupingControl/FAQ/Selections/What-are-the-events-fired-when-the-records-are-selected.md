---
layout: post
title: What-are-the-events-fired-when-the-records-are-sel | Windows Forms | Syncfusion
description: what are the events fired when the records are selected
platform: windowsforms
control: GridGrouping
documentation: ug
---

# What are the Events Fired when the Records are Selected

Following are the events fired when the records are selected.

{% tabs %}
{% highlight c# %}

//SelectionChanging Event.
this.gridGroupingControl1.SelectedRecordsChanging += new Syncfusion.Grouping.SelectedRecordsChangedEventHandler(this.gridGroupingControl1_SelectedRecordsChanging);

//SelectionChanged Event.
this.gridGroupingControl1.SelectedRecordsChanged += new Syncfusion.Grouping.SelectedRecordsChangedEventHandler(this.gridGroupingControl1_SelectedRecordsChanged);

{% endhighlight %}

{% highlight vb %}

'SelectionChanging Event
Private Sub gridGroupingControl1_SelectedRecordsChanging(ByVal sender As Object, ByVal e As Syncfusion.Grouping.SelectedRecordsChangedEventArgs) Handles gridGroupingControl1.SelectedRecordsChanging
System.Diagnostics.Trace.WriteLine("Action in SelectedRecordsChanging-->" + e.Action)
End Sub

'SelectionChanged Event
Private Sub gridGroupingControl1_SelectedRecordsChanged(ByVal sender As Object, ByVal e As Syncfusion.Grouping.SelectedRecordsChangedEventArgs) Handles gridGroupingControl1.SelectedRecordsChanged
System.Diagnostics.Trace.WriteLine("Action in SelectedRecordsChanged-->" + e.Action)
End Sub

{% endhighlight %}
{% endtabs %}
