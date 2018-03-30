---
layout: post
title: What-are-the-options-in-the-summary-columns | Windows Forms | Syncfusion
description: what are the options in the summary columns
platform: windowsforms
control: GridGrouping
documentation: ug
---

# What are the Options in the Summary Columns

The options in the summary columns are illustrated using the code below.

{% tabs %}
{% highlight c# %}

//Disables the change of summary value during the filter criteria.

//summaryDescriptor is GridSummaryColumnDescriptor. 

//This ignores filtering of the grid. So, the summary value does not change.
summaryDescriptor.IgnoreRecordFilterCriteria=true;

{% endhighlight  %}

{% highlight vb %}

'Disables the change of summary value during the filter criteria.

'summaryDescriptor is GridSummaryColumnDescriptor. 

'This ignores filtering of the grid. So, the summary value does not change.
summaryDescriptor.IgnoreRecordFilterCriteria=True

{% endhighlight  %}
{% endtabs %}
