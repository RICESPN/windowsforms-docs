---
layout: post
title: DateTime Editing in Windows Forms DateTimePicker | Syncfusion
description: Editing mode supports default text editing and mask mode that helps to restrict the date input in formatted values based on a date-time pattern.
platform: WindowsForms
control: SfDateTimeEdit
documentation: ug
---

# DateTime Editing in Windows Forms DateTimePicker (SfDateTimeEdit)

The DateTime value of the `SfDateTimeEdit` control can be updated by editing the text in the control. The [DateTimeEditingMode](https://help.syncfusion.com/cr/windowsforms/Syncfusion.WinForms.Input.SfDateTimeEdit.html#Syncfusion_WinForms_Input_SfDateTimeEdit_DateTimeEditingMode) decides how to insert the input values for the SfDateTimeEdit from the keyboard. The DateTimeText can be edited by two ways as follows:

* Default editing
* Mask editing

## Default editing

The DateTime can be edited in the textbox of the `SfDateTimeEdit` control when the [DateTimeEditingMode](https://help.syncfusion.com/cr/windowsforms/Syncfusion.WinForms.Input.SfDateTimeEdit.html#Syncfusion_WinForms_Input_SfDateTimeEdit_DateTimeEditingMode) is default. In default editing mode, the value can be assigned in any valid format. Even if the text box text is not in the correct pattern, the SfDateTimeEdit control automatically updates the value in the correct pattern on lost focus. i.e, if the date time pattern is LongDate with pattern "dddd, MMMM dd, yyyy" and date is entered as "Mar 28 2017" in the editing text box, the DateTimeText will be automatically converted according to the LongDate pattern while pressing the enter key or on lost focus of the control.

{% tabs %}

{% highlight C# %}

Syncfusion.WinForms.Input.SfDateTimeEdit dateTimeEdit = new Syncfusion.WinForms.Input.SfDateTimeEdit();

this.Controls.Add(dateTimeEdit);

dateTimeEdit.Value = new DateTime(2017, 6, 27);

dateTimeEdit.DateTimeEditingMode = DateTimeEditingMode.Default;

{% endhighlight  %}

{% highlight VB %}

Dim dateTimeEdit As Syncfusion.WinForms.Input.SfDateTimeEdit = New Syncfusion.WinForms.Input.

Me.Controls.Add(dateTimeEdit)

dateTimeEdit.Value = New DateTime(2017, 6, 27)

dateTimeEdit.DateTimeEditingMode = DateTimeEditingMode.Default

{% endhighlight  %}

{% endtabs %} 

![Default editing](editing-support-images/default.png)

## Mask editing

The mask edit mode provides an easy and reliable way of collecting user input and displaying standard data in a specific format. In mask editing mode, the date will be separated into different fields such as date, month, year, minutes, hours, and seconds. The field can be updated by selecting the field and pressing the up or down arrow to increase or decrease the selected field respectively.

{% tabs %}

{% highlight C# %}

Syncfusion.WinForms.Input.SfDateTimeEdit dateTimeEdit = new Syncfusion.WinForms.Input.SfDateTimeEdit();

this.Controls.Add(dateTimeEdit);

dateTimeEdit.Value = new DateTime(2018, 2, 01);

dateTimeEdit.DateTimeEditingMode = DateTimeEditingMode.Mask;

{% endhighlight  %}

{% highlight VB %}

Dim dateTimeEdit As Syncfusion.WinForms.Input.SfDateTimeEdit = New Syncfusion.WinForms.Input.SfDateTimeEdit

Me.Controls.Add(dateTimeEdit)

dateTimeEdit.Value = New DateTime(2018, 2, 1)

dateTimeEdit.DateTimeEditingMode = DateTimeEditingMode.Mask

{% endhighlight  %}

{% endtabs %}

![Mask editing](editing-support-images/mask.png)

## ReadOnly

This control supports `ReadOnly` which is used to restrict edit date and time fields in the `SfDateTimeEdit`. By setting the [ReadOnly](https://help.syncfusion.com/cr/windowsforms/Syncfusion.WinForms.Input.SfDateTimeEdit.html#Syncfusion_WinForms_Input_SfDateTimeEdit_ReadOnly) to **true**, you can restrict the text editing in the `SfDateTimeEdit` and you can change the value only by clicking up-down buttons or pick the date from the drop-down `SfCalendar`.

{% tabs %}

{% highlight C# %}

//Enable the User interactions

this.dateTimeEdit.ReadOnly = false;

{% endhighlight  %}

{% highlight VB %}

'Enable the User interactions

Me.dateTimeEdit.ReadOnly = false

{% endhighlight  %}

{% endtabs %}

![Read only support](editing-support-images/readonly.png)
