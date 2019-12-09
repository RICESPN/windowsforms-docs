---
layout: post
title: Event-Handling | WindowsForms | Syncfusion
description: event handling
platform: WindowsForms
control: EditorsPackage
documentation: ug
---

# Event Handling

EditableList controls contains events present in the Windows Button, TextBox and ListBox.

 EditableList.ListBox.SelectedValueChanged

This event is triggered when the value of the SelectedValue property is changed on list control.

 EditableList.TextBox.TextChanged

This event is triggered when the value of the Text property is changed on list control.

 EditableList.DragDrop

This event is triggered when the drag-and-drop operation is completed.

 EditableList.DragEnter

This event is triggered when a object is dragged into control's bounds.

[Handling Drag drop events](//docs.syncfusion.com/windowsforms/tools)

DragDrop and DragEnter events can be handled to drag and drop the external objects into the EditableList control.

DragEnter event can be handled to drag the file into the text area of EditableList control. The following code illustrates this.

{% tabs %}
{% highlight c# %}

private void editableList1_DragEnter(object sender, System.Windows.Forms.DragEventArgs e)
{
	if (e.Data.GetDataPresent(DataFormats.FileDrop))
		e.Effect = DragDropEffects.All;
	else
		e.Effect = DragDropEffects.None;
}

{% endhighlight %}

{% highlight vb %}

Private Sub editableList1_DragEnter(ByVal sender As Object, ByVal e AsSystem.Windows.Forms.DragEventArgs)
If e.Data.GetDataPresent(DataFormats.FileDrop) Then
e.Effect = DragDropEffects.All
Else
e.Effect = DragDropEffects.None
End If
End Sub

{% endhighlight %}
{% endtabs %}

DragDrop event can be handled to drop the files at any location into the EditableList control. The following code illustrates this.

{% tabs %}
{% highlight c# %}

private void editableList1_DragDrop(object sender, System.Windows.Forms.DragEventArgs e)
{
    string[] files = (string[])e.Data.GetData("FileDrop", false);
    foreach (string s in files)
    {
        this.editableList1.ListBox.Items.Add(s.Substring(1 + s.LastIndexOf(@"\")));
    }
}

{% endhighlight %}

{% highlight vb %}

Private Sub editableList1_DragDrop(ByVal sender As Object, ByVal e AsSystem.Windows.Forms.DragEventArgs)
Dim files As String() = CType(e.Data.GetData("FileDrop", False), String())
For Each s As String In files
Me.editableList1.ListBox.Items.Add(s.Substring(1 & s.LastIndexOf("\")))
Next s
End Sub

{% endhighlight %}
{% endtabs %}
