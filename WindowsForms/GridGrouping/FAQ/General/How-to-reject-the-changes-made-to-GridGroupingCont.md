---
layout: post
title: How-to-reject-the-changes-made-to-GridGroupingCont | Windows Forms | Syncfusion
description: how to reject the changes made to gridgroupingcontrol
platform: windowsforms
control: GridGrouping
documentation: ug
---

# How to Reject the Changes made to GridGroupingControl

By default, any changes made to GridGroupingControl will affect the underlying data source. In order to cancel the changes, you can make use of RejectChanges method to reject the recent changes made to the data source. Also, ensure that AcceptChanges method is called after date source is filled, as RejectChanges method will roll back all the changes made to the data source since the last time the AcceptChanges method was called.

{% tabs %}
{% highlight C# %}

private void button1_Click(object sender, EventArgs e) 
{ 
    DataTable dt = this.gridGroupingControl1.DataSource as DataTable; 
    dt.RejectChanges(); 
}
{% endhighlight %}

{% highlight vb %}

Private Sub button1_Click(ByVal sender As Object, ByVal e As EventArgs)
Dim dt As DataTable = TryCast(Me.gridGroupingControl1.DataSource, DataTable)
dt.RejectChanges()

End Sub
{% endhighlight %}
{% endtabs %}
