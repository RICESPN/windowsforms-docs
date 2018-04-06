---
layout: post
title: How-to-programmatically-select-the-record-in-the-d | WindowsForms | Syncfusion
description: how to programmatically select the record in the dropdown that matches the text typed in comboboxadv?
platform: WindowsForms
control: ComboBoxAdv
documentation: ug
---

# How to Programmatically Select the Record in the Dropdown that matches the Text Typed in ComboBoxAdv

You can handle the DropDown event of the ComboBoxAdv control and set it as shown in the following code example.

{% tabs %}
{% highlight c# %}

//ComboBoxAdv dropdown event
private void comboBoxAdv1_DropDown(object sender, System.EventArgs e)
{
    this.comboBoxAdv1.ListBox.SelectedItem = this.comboBoxAdv1.TextBox.Text;
}

{% endhighlight %}

{% highlight vb %}

'ComboBoxAdv dropdown event
Private Sub comboBoxAdv1_DropDown(ByVal sender As Object, ByVal e As System.EventArgs)
    Me.comboBoxAdv1.ListBox.SelectedItem = Me.comboBoxAdv1.TextBox.Text
End Sub

{% endhighlight %}
{% endtabs %}

