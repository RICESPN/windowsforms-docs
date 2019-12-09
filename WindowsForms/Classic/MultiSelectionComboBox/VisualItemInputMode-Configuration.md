---
layout: post
title: VisualItemInputMode-Configuration | WindowsForms | Syncfusion
description: visualiteminputmode configuration
platform: WindowsForms
control: Editors Package
documentation: ug
---

# VisualItemInputMode Configuration

The property named VisualItemInputMode helps to define the Visual Items in Text Input.



<table>
<tr>
<th>
Property</th><th>
Description</th></tr>
<tr>
<td>
VisualItemInputMode</td><td>
Gets/Sets the VisualItem Text input mode.</td></tr>
<tr>
<td>
DisplayMemberMode</td><td>
To set SelectedItem as the text input of VisualItem.</td></tr>
<tr>
<td>
ValueMemberMode</td><td>
To set SelectedValue as the text input of VisualItem.</td></tr>
<tr>
<td>
VisualItemMode</td><td>
To set custom text input for VisualItem, based on the end-user’s requirement.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

//Define the Visual items as DisplayMember
this.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.DisplayMemberMode;

//Define the Visual items as ValueMember
this.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.ValueMemberMode;

//To set custom text input for VisualItem, based on end user requirement.
this.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.VisualItemMode;

{% endhighlight %}

{% highlight vb %}

'Define the Visual items as DisplayMember
Me.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.DisplayMemberMode

'Define the Visual items as ValueMember
Me.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.ValueMemberMode

'To set custom text input for VisualItem, based on end user requirement.
Me.multiSelectionComboBox1.VisualItemInputMode = Syncfusion.Windows.Forms.Tools.VisualItemInputMode.VisualItemMode

{% endhighlight %}
{% endtabs %}
