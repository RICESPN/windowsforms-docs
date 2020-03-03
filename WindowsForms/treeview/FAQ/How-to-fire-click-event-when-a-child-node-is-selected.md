---
layout: post
title: How-to-fire-click-event-when-a-child-node-is-selected | WindowsForms | Syncfusion
description: how to fire click event, when a child node is selected
platform: WindowsForms
control: TreeView 
documentation: ug
---

# How to Fire Click Event, When a Child Node is Selected

Whenever a TreeViewAdv is selected, AfterSelect event will be raised. You can raise a Click event when a child node is selected, inside this handler using the following code snippet. 

{% tabs %}
{% highlight c# %}

private void treeViewAdv1_AfterSelect(object sender, EventArgs e)
{

// iterate through parent nodes in the collection 
    foreach (TreeNodeAdv node in this.treeViewAdv1.Nodes)
    {
        if (node.IsSelected)
        {
            Console.WriteLine(node.Text + "is selected");
        }
        CheckForChildren(node);
    }
}
private void CheckForChildren(TreeNodeAdv node)
{

// check whether each parent node has child nodes 
    if (node.HasChildren && node.Nodes.Count > 0)
    {

// iterate through child nodes in the collection
        foreach (TreeNodeAdv childNode in node.Nodes)
        {
            if (childNode.IsSelected)
            {
                Console.WriteLine(childNode.Text + "is selected");
            }

// Do recursive call
            CheckForChildren(childNode);
        }
    }
}

{% endhighlight %}

{% highlight vb %}

Private Sub treeViewAdv1_AfterSelect(ByVal sender As Object, ByVal e As EventArgs)

' iterate through parent nodes in the collection 
For Each node As TreeNodeAdv In Me.treeViewAdv1.Nodes
If node.IsSelected Then
Console.WriteLine(node.Text & "is selected")
End If
CheckForChildren(node)
Next node
End Sub
Private Sub CheckForChildren(ByVal node As TreeNodeAdv)

' check whether each parent node has child nodes 
If node.HasChildren AndAlso node.Nodes.Count > 0 Then

' iterate through child nodes in the collection
For Each childNode As TreeNodeAdv In node.Nodes
If childNode.IsSelected Then
Console.WriteLine(childNode.Text & "is selected")
End If

' Do recursive call
CheckForChildren(childNode)
Next childNode
End If
End Sub

{% endhighlight %}
{% endtabs %}
