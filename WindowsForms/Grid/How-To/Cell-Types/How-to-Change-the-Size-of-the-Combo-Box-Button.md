---
layout: post
title: How-to-Change-the-Size-of-the-Combo-Box-Button | Windows Forms | Syncfusion
description: how to change the size of the combo box button
platform: windowsforms
control: Grid
documentation: ug
---

# How to Change the Size of the Combo Box Button

### Introduction

Change the size of the combobox button by changing the ButtonBarSize in the CellModel for the control. 

{% tabs %}
{% highlight c# %}

//Creates Combobox Cell model object.
GridComboBoxCellModel model = this.grid.Model.CellModels["ComboBox"] as GridComboBoxCellModel;

//Assigns a new value to its ButtonBarSize property. 
model.ButtonBarSize = new Size(8, 8);

{% endhighlight %}

{% highlight vb %}

'Creates Combobox Cell model object.
Dim model As GridComboBoxCellModel = CType(Me.Grid.Model.CellModels("ComboBox"), GridComboBoxCellModel)

'Assigns a new value to its ButtonBarSize property.
model.ButtonBarSize = New Size(8, 8)

{% endhighlight %}
{% endtabs %}