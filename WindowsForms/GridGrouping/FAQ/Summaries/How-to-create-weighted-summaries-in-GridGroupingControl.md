---
layout: post
title: How-to-create-weighted-summaries-in-GridGroupingCo | Windows Forms | Syncfusion
description: how to create weighted summaries in gridgroupingcontrol
platform: windowsforms
control: GridGrouping
documentation: ug
---

# How to Create Weighted Summaries in GridGroupingControl

You can create custom summaries that perform weighted average calculations using code naming convention to pass the column holding the weights to the summary descriptor. Refer to the code snippet below, which illustrates this.

{% tabs %}
{% highlight c# %}

private void gridGroupingControl1_QueryCustomSummary(object sender, GridQueryCustomSummaryEventArgs e)
{
    if(e.SummaryDescriptor.SummaryType == SummaryType.Custom) 
    {
        e.SummaryDescriptor.CreateSummaryMethod = new CreateSummaryDelegate(WeightedSummary.CreateSummaryMethod);
    }
    e.Handled = true;
}

private GridSummaryColumnDescriptor GetWeightedSummaryColumnDescriptor(string sourceCol, string weightCol)
{
    GridSummaryColumnDescriptor summaryColumnDescriptor = new GridSummaryColumnDescriptor();
    summaryColumnDescriptor.Name = string.Format("{0}_{1}", sourceCol, weightCol); //special name following the convention above
    summaryColumnDescriptor.DataMember = sourceCol; //the column this summary is applied to
    summaryColumnDescriptor.DisplayColumn = sourceCol; //where this summary is displayed
    summaryColumnDescriptor.Format = "{WeightedAverage:#.#}"; //what is displayed in the summary
    summaryColumnDescriptor.SummaryType = SummaryType.Custom; //marks this as a Custom Summary
    summaryColumnDescriptor.Appearance.AnySummaryCell.HorizontalAlignment = GridHorizontalAlignment.Right;
    summaryColumnDescriptor.MaxLength = 6;
    return summaryColumnDescriptor;
}

{% endhighlight  %}

{% highlight vb %}

'Custom summary.
Private Sub gridGroupingControl1_QueryCustomSummary(ByVal sender As Object, ByVal e As GridQueryCustomSummaryEventArgs)
If e.SummaryDescriptor.SummaryType = SummaryType.Custom Then
e.SummaryDescriptor.CreateSummaryMethod = New CreateSummaryDelegate(AddressOf WeightedSummary.CreateSummaryMethod)
End If
e.Handled = True
End Sub
Private Function GetWeightedSummaryColumnDescriptor(ByVal sourceCol As String, ByVal weightCol As String) As GridSummaryColumnDescriptor
Dim summaryColumnDescriptor As GridSummaryColumnDescriptor = New GridSummaryColumnDescriptor
summaryColumnDescriptor.Name = String.Format("{0}_{1}", sourceCol, weightCol) 'special name following the convention above
summaryColumnDescriptor.DataMember = sourceCol 'the column this summary is applied to
summaryColumnDescriptor.DisplayColumn = sourceCol 'where this summary is displayed
summaryColumnDescriptor.Format = "{WeightedAverage:#.#}" 'what is displayed in the summary
summaryColumnDescriptor.SummaryType = SummaryType.Custom 'marks this as a Custom Summary
summaryColumnDescriptor.Appearance.AnySummaryCell.HorizontalAlignment = GridHorizontalAlignment.Right
summaryColumnDescriptor.MaxLength = 6
Return summaryColumnDescriptor
End Function

{% endhighlight  %}
{% endtabs %}
