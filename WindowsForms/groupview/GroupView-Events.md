---
layout: post
title: GroupView Events | WindowsForms | Syncfusion
description: Concepts and Features
platform: WindowsForms
control: GroupView
documentation: ug
---
# GroupView events

The list of events and a detailed explanation about each of them is given in the following sections.

* [GroupViewItemHighlighted](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)
* [GroupViewItemRenamed](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)
* [GroupViewItemSelected](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)
* [GroupViewItemsReordered](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)
* [ShowContextMenu](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)
* [GroupViewItemDoubleClick](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html)

## GroupViewItemHighlighted event

The [GroupViewItemHighlighted](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event occurs when a GroupView Item in the GroupView control is highlighted.

The event handler receives an argument of type EventArgs.

{% tabs %}

{% highlight C# %}

//Handle the GroupViewItemHighlighted event.

this.groupView1.GroupViewItemHighlighted+=new EventHandler(groupView1_GroupViewItemHighlighted);



private void groupView1_GroupViewItemHighlighted(object sender, EventArgs e)

{

this.groupView1.HighlightText = true;

this.groupView1.HighlightItemColor = System.Drawing.Color.AliceBlue;

}

{% endhighlight %}



{% highlight VB %} 

'Handle the GroupViewItemHighlighted event. 

AddHandler Me.groupView1.GroupViewItemHighlighted, AddressOf groupView1_GroupViewItemHighlighted 



Private Sub groupView1_GroupViewItemHighlighted(ByVal sender As Object, ByVal e As EventArgs)

    Me.groupView1.HighlightText = True

    Me.groupView1.HighlightItemColor = System.Drawing.Color.AliceBlue

End Sub

{% endhighlight %}

{% endtabs %}

![GroupViewItemHighlighted event usage](Overview_images/Overview_img88.jpeg) 


## GroupViewItemRenamed event

The [GroupViewItemRenamed](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event occurs when a GroupView Item has been renamed by an in-place edit operation.

The event handler receives an argument of type GroupItemRenamedEventArgs. The event properties associated with the GroupItemRenamedEventArgs are as follows.



<table>
<tr>
<th>
Members</th><th>
Description</th></tr>
<tr>
<td>
BackgroundBrush</td><td>
Gets/sets the brush that will be used to draw the specified bounds.</td></tr>
<tr>
<td>
Bounds</td><td>
Returns the bounds for which a brush is requested.</td></tr>
<tr>
<td>
Item</td><td>
Returns the index of the GroupBar Item being drawn.</td></tr>
</table>

{% tabs %}

{% highlight C# %}  

// This event occurs when a GroupView Item in the GroupView is renamed.

private void groupWinForms_GroupViewItemRenamed(object obj, Syncfusion.Windows.Forms.Tools.GroupItemRenamedEventArgs arg)

{

ListViewItem listViewItem1 = new System.Windows.Forms.ListViewItem(new string[] {"GroupViewItemRenamed", "Old Label: " +arg.OldLabel + " New Label: " +arg.NewLabel});

this.listView1.Items.Add(listViewItem1);

}

{% endhighlight %}



{% highlight VB %}

// This event occurs when a GroupView Item in the GroupView is renamed.

Private Sub groupWinForms_GroupViewItemRenamed(ByVal obj As Object, ByVal arg As Syncfusion.Windows.Forms.Tools.GroupItemRenamedEventArgs) Handles groupWinForms.GroupViewItemRenamed

Dim listViewItem1 As ListViewItem = New System.Windows.Forms.ListViewItem(New String() {"GroupViewItemRenamed", "Old Label: " + arg.OldLabel & " New Label: " + arg.NewLabel})

Me.ListView1.Items.Add(listViewItem1)

End Sub


{% endhighlight %}

{% endtabs %}

## GroupViewItemReordered event

The [GroupViewItemsReordered](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event occurs when a GroupView Item in the GroupView control is reordered.

The event handler receives an argument of type GroupItemRenamedEventArgs.

{% tabs %}

{% highlight C# %}  

// This event occurs when a GroupView Item in the GroupView is reordered.

private void groupWinForms_GroupViewItemsReordered(object sender, System.EventArgs e)

{

ListViewItem listViewItem1 = new System.Windows.Forms.ListViewItem(new string[] {"GroupViewItemsReordered"});

this.listView1.Items.Add(listViewItem1);

}

{% endhighlight %}



{% highlight VB %}

// This event occurs when a GroupView Item in the GroupView is reordered.

Private Sub groupWinForms_GroupViewItemsReordered(ByVal sender As Object, ByVal e As System.EventArgs) Handles groupWinForms.GroupViewItemsReordered

Dim listViewItem1 As ListViewItem = New System.Windows.Forms.ListViewItem(New String() {"GroupViewItemsReordered"})

Me.ListView1.Items.Add(listViewItem1)

End Sub

{% endhighlight %}

{% endtabs %}


## GroupViewItemSelected event

The [GroupViewItemSelected](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event occurs when a GroupView Item in the GroupView control is selected.

Accessing the GroupView.SelectedItem property from within the GroupViewItemSelected event handler will allow you to determine the item that was clicked. Based on this appropriate command, handling routines can be invoked.

The GroupView.SelectedItem property is accessed from within the handler to determine the selected item.

{% tabs %}

{% highlight C# %}  

// Provide a handler for the GroupView.GroupViewItemSelected event.

this.groupView1.GroupViewItemSelected += new System.EventHandler(this.groupView1_GroupViewItemSelected); 

// GroupView.GroupViewItemSelected event handler.

// The GroupView.SelectedItem property fetches the index of the selected item, while the item is obtained by referencing the selected index within the GroupView.GroupViewItems collection.

private void groupView1_GroupViewItemSelected(object sender, System.EventArgs e)

{

Trace.WriteLine(String.Concat("Selected Item = ", this.groupWinForms.GroupViewItems[this.groupWinForms.SelectedItem].Text)); 

}

{% endhighlight %}



{% highlight VB %}

' Provide a handler for the GroupView.GroupViewItemSelected event.

AddHandler Me.groupView1.GroupViewItemSelected, New System.EventHandler(AddressOf groupView1_GroupViewItemSelected)

' GroupView.GroupViewItemSelected event handler.

' The GroupView.SelectedItem property fetches the index of the selected item, while the item is obtained by referencing the selected index within the GroupView.GroupViewItems collection.

Private Sub groupView1_GroupViewItemSelected(ByVal sender As Object, ByVal e As System.EventArgs)

MessageBox.Show([String].Concat("Selected Item Index = ", Me.groupView1.SelectedItem.ToString()))

End Sub 

{% endhighlight %}

{% endtabs %}

## ShowContextMenu event

The GroupBar and the GroupView control implement a ShowContextMenu event that is generated when the user right-clicks on the control. Applications can handle this event to create and display a Context Menu for the control. Both controls provide a [ContextMenuItem](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html#Syncfusion_Windows_Forms_Tools_GroupView_ContextMenuItem) property that returns the index of the GroupBar Item or the GroupView Item over which the mouse click occurred and this can be used to populate the menu with accurate item-specific contextual information.

The following code from the GroupBar Demo shows a sample handler for the [GroupBar.ShowContextMenu](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event that uses the EssentialToolsXPMenus.PopupMenu class for the context menu. The handler accesses the control's [GroupBar.ContextMenuItem](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html#Syncfusion_Windows_Forms_Tools_GroupView_ContextMenuItem) property to ascertain whether the mouse click occurred over a GroupBar Item, and if so, to determine the identity of the particular item.

{% tabs %}

{% highlight C# %}

// Handler for the GroupBar.ShowContextMenu event.

private void groupVS_ShowContextMenu(object sender, System.EventArgs e)

{

// Create the XPMenus.PopupMenu instance and populate it with the menu items.

Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu menu = new Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu();

menu.ParentBarItem = new Syncfusion.Windows.Forms.Tools.XPMenus.ParentBarItem();

Syncfusion.Windows.Forms.Tools.GroupBar grp = sender as GroupBar;              



BarItem tab = new BarItem("Add New Tab", new EventHandler(this.TabVSMenuAddNewTab));

tab.Tag = this.grp;

menu.ParentBarItem.Items.Add(tab);        



BarItem delete = new BarItem("Delete Tab", new EventHandler(this.TabMenuRemoveGroup));

delete.Tag = this.grp;

menu.ParentBarItem.Items.Add(delete);

        ...

// If the mouse click occurred over a GroupBarItem then get that item's client control and update the menu with client specific menu items.

if(this.grp.ContextMenuItem != -1)

{

GroupView view = this.grp.GroupBarItems[this.grp.ContextMenuItem].Client as GroupView;



BarItem move = new BarItem("Move &Up", new EventHandler(this.TabVSMenuMoveUpDown));

move.Tag = view;

menu.ParentBarItem.Items.Add(move);

move.Enabled = false;

}

// Finally invoke the XPMenus.PopupMenu.Show() method to display the context menu.

menu.Show(this.grp, this.grp.PointToClient(Cursor.Position));             

}

{% endhighlight %}



{% highlight VB %} 

// Handler for the GroupBar.ShowContextMenu event.

Private Sub groupVS_ShowContextMenu(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles groupVStudio.ShowContextMenu

' Create the XPMenus.PopupMenu instance and populate it with the menu items.

Dim menu As Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu = New Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu()

menu.ParentBarItem = New Syncfusion.Windows.Forms.Tools.XPMenus.ParentBarItem()



Private grp As Syncfusion.Windows.Forms.Tools.GroupBar = CType(IIf(TypeOf sender Is GroupBar, sender, Nothing), GroupBar)



Dim tab As BarItem = New BarItem("Add New Tab", New EventHandler(Me.TabVSMenuAddNewTab))

tab.Tag = Me.grp

menu.ParentBarItem.Items.Add(tab)



Dim delete As BarItem = New BarItem("Delete Tab", New EventHandler(Me.TabMenuRemoveGroup))

delete.Tag = Me.grp

menu.ParentBarItem.Items.Add(delete)



' If the mouse click occurred over a GroupBarItem then get that item's client control and update the menu with client specific menu items.

If Me.grp.ContextMenuItem &lt;&gt; -1 Then

Dim view As GroupView =  Me.grp.GroupBarItems(Me.grp.ContextMenuItem).Client as GroupView 

Dim move As BarItem = New BarItem("Move &Up", New EventHandler(Me.TabVSMenuMoveUpDown))

move.Tag = view

menu.ParentBarItem.Items.Add(move)

move.Enabled = False

End If

' Finally invoke the XPMenus.PopupMenu.Show() method to display the context menu.

menu.Show(Me.grp, Me.grp.PointToClient(Cursor.Position))

End Sub

{% endhighlight %}

{% endtabs %}

The following code from the GroupView Demo shows a sample handler for the GroupView.ShowContextMenu event. The handler accesses the GroupView.HighlightedItem property to ascertain whether the mouse click occurred over a GroupView Item and populates the menu accordingly.

{% tabs %}

{% highlight C# %}

// Handler for the GroupView.ShowContextMenu event.

private void group_ShowContextMenu(object sender, System.EventArgs e)

{

Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu menu = new Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu();

menu.ParentBarItem = new Syncfusion.Windows.Forms.Tools.XPMenus.ParentBarItem();



BarItem item = new BarItem("Add New Item", new EventHandler(this.group_MenuAddNewItem));

menu.ParentBarItem.Items.Add(item);



BarItem remove = new BarItem("Remove Item", new EventHandler(this.group_MenuRemoveItem));

menu.ParentBarItem.Items.Add(remove);



// Enable the RemoveItem menu item only if the mouse click occurred over a GroupView Item.

if(this.groupWinForms.HighlightedItem == -1)

remove.Enabled = false;



// Show the context menu using the Cursor.Position value for the location.

menu.Show(this.groupWinForms, this.groupWinForms.PointToClient(Cursor.Position));

}   

 {% endhighlight %}



{% highlight VB %}

' Handler for the GroupView.ShowContextMenu event.

Private Sub group_ShowContextMenu(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles groupWinForms.ShowContextMenu



Dim menu As Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu = New Syncfusion.Windows.Forms.Tools.XPMenus.PopupMenu()

menu.ParentBarItem = New Syncfusion.Windows.Forms.Tools.XPMenus.ParentBarItem()



Dim item As BarItem = New BarItem("Add New Item", New EventHandler(Me.group_MenuAddNewItem))

 menu.ParentBarItem.Items.Add(item)



Dim remove As BarItem = New BarItem("Remove Item", New EventHandler(Me.group_MenuRemoveItem))

menu.ParentBarItem.Items.Add(remove)



' Enable the RemoveItem menu item only if the mouse click occurred over a GroupView Item.

If Me.groupWinForms.HighlightedItem = -1 Then

remove.Enabled = False

End If



' Show the context menu using the Cursor.Position value for the location.

menu.Show(Me.groupWinForms, Me.gcWinForms.PointToClient(Cursor.Position))

End Sub

{% endhighlight %}

{% endtabs %}

![ShowContextMenu](Overview_images/Overview_img89.jpeg) 

## GroupViewItemDoubleClick event

The [GroupViewItemDoubleClick](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.Tools.GroupView.html) event occurs when a GroupView Item in the GroupView control is double-clicked.

The event handler receives an argument of type GroupViewItemDoubleClickArgs.

<table>
<tr>
<th>
Members</th><th>
Description</th></tr>
<tr>
<td>
SelectedItem</td><td>
Gets/Sets the currently selected GroupView item</td></tr>
</table>

{% tabs %}

{% highlight C# %}

//This event occurs when the GroupView item is double clicked.

void groupView1_GroupViewItemDoubleClick(Syncfusion.Windows.Forms.Tools.GroupView sender, Syncfusion.Windows.Forms.Tools.GroupViewItemDoubleClickEventArgs e)

{
	MessageBox.Show(e.SelectedItem.Text + " is double clicked");
}

{% endhighlight %}

{% highlight VB %}

'This event occurs when the GroupView item is double clicked.

Private Sub groupView1_GroupViewItemDoubleClick(ByVal sender As Syncfusion.Windows.Forms.Tools.GroupView, ByVal e As Syncfusion.Windows.Forms.Tools.GroupViewItemDoubleClickEventArgs) 

	 MessageBox.Show(e.SelectedItem.Text & " is double clicked")
     
End Sub

{% endhighlight %}

{% endtabs %}
