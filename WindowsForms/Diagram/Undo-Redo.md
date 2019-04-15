---
layout: post
title: Undo-or-Redo | Windows Forms | Syncfusion
description: This section explains about how to revert/restore the changes using Undo and Redo commands in Diagram control
platform: windowsforms
control: Diagram
documentation: ug
---

# Undo / Redo

The actions can be recorded into the history manager such that the undo and redo operations can be performed. The recording can be controlled and the undo and redo actions can be performed using the following tools.



Undo / Redo Properties

<table>
<tr>
<th>
History Manager Tool </th><th>
Description</th></tr>
<tr>
<td>
Undo</td><td>
Undo the previous action.</td></tr>
<tr>
<td>
Redo</td><td>
Redo the previous action. Redo action can be performed only after an undo action.</td></tr>
<tr>
<td>
StartAtomicAction</td><td>
Stops recording the actions and hence will not be added to the undo history manager.</td></tr>
<tr>
<td>
EndAtomicAction</td><td>
Cancels the StartAtomicAction process and turns on the recording of actions in the history manager.</td></tr>
</table>


Programmatically, it is implemented as follows:


{% tabs %}
{% highlight c# %}

this.diagram1.Model.HistoryManager.Undo();
this.diagram1.Model.HistoryManager.Redo();
this.diagram1.Model.HistoryManager.StartAtomicAction("Custom Action");
this.diagram1.Model.HistoryManager.EndAtomicAction();

{% endhighlight %}
{% highlight vb %}

Me.diagram1.Model.HistoryManager.Undo()
Me.diagram1.Model.HistoryManager.Redo()
Me.diagram1.Model.HistoryManager.StartAtomicAction("Custom Action")
Me.diagram1.Model.HistoryManager.EndAtomicAction()

{% endhighlight %}
{% endtabs %}