---
layout: post
title: Getting started | SfNumericTextBox | WindowsForms | Syncfusion  
description: This section provides the information about how to begin the SfNumericTextBox control.
platform: WindowsForms
control: SfNumericTextBox
documentation: ug
---

# Getting Started

This section will give a step-by-step procedure to design a SfNumericTextBox control and the overview of its basic functionalities.

## Assembly deployment

Refer [control dependencies](https://help.syncfusion.com/windowsforms/control-dependencies#sfnumerictextbox) section to get the list of assemblies or NuGet package needs to be added as reference to use the control in any application.
 
Please find more details regarding how to install the nuget packages in windows form application in the below link:
 
[How to install nuget packages](https://help.syncfusion.com/windowsforms/nuget-packages)

## Configuring Numeric TextBox

## Adding SfNumericTextBox control through Designer

SfNumericTextBox can be added through designer by following the below steps.
**1.**	Create a new **Windows Form Application**.
**2.**	Drag and Drop SfNumericTextBox from the toolbox into the designer page.

![Drag and drop the SfNumericTextBox control to form](Gettingstarted_images/SfNumericTextBoxAdd.png)

**3.**	Once you drag drop the SfNumericTextBox into the designer page, the SfNumericTextBox will be added successfully into the application with the required libraries. The below mentioned assemblies will be added automatically into the application.
    *	Syncfusion.Core.WinForms.dll
    *	Syncfusion.SfInput.WinForms.dll

![SfNumericTextBox control added by designer](Gettingstarted_images/SfNumericTextBoxDesignerAdd.png)

## Adding SfNumericTextBox control through code

**1.**	SfNumericTextBox can be added through code-behind by following the below steps.
**2.**	Add the below assemblies into the project file.
    *	Syncfusion.Core.WinForms.dll
    *	Syncfusion.SfInput.WinForms.dll
**3.**	Initialize a SfNumericTextBox by using the below code in code behind.

{% tabs %}

{% highlight C# %}

private Syncfusion.WinForms.Input.SfNumericTextBox numericTextBox = new Syncfusion.WinForms.Input.SfNumericTextBox();

{% endhighlight %}

{% highlight VB %}

Private numericTextBox As Syncfusion.WinForms.Input.SfNumericTextBox = New Syncfusion.WinForms.Input.SfNumericTextBox() 

{% endhighlight %}

{% endtabs %}

**4.**	Use the below code for adding the initialized SfNumericTextBox to the application.

{% tabs %}

{% highlight C# %}

this.numericTextBox.Size = new System.Drawing.Size(100, 20);

this.numericTextBox.Value = 123.45;

this.Controls.Add(this.numericTextBox);

{% endhighlight %}

{% highlight VB %}

Me.numericTextBox.Size = new System.Drawing.Size(100, 20)

Me.numericTextBox.Value = 123.45

Me.Controls.Add(Me.numericTextBox)

{% endhighlight %}

{% endtabs %}

## Adding Value to the control

It assigns the value to SfNumericTextBox. It holds the double value which can also hold null value. The [AllowNull](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~AllowNull.html) property needs to be set to make the Value nullable. The [Text](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~Text.html) property of the control gets formatted from the Value property.

{% tabs %}

{% highlight C# %}

// To set the Value to the SfNumericTextBox.
this.numericTextBox.Value = 123.45;

{% endhighlight %}

{% highlight VB %}

‘ To set the Value to the SfNumericTextBox.
Me.numericTextBox.Value = 123.45

{% endhighlight %}

{% endtabs %}

![Value assigned in numeric text box control](Gettingstarted_images/Value.png)

## Formatting the value

Formatting functionality allows to format the value based on the FormatMode of the control. By default, the value gets parsed from the application’s CurrentUICulture. Custom formatting can also be done using [NumberFormatInfo](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~NumberFormatInfo.html) property, which allow to set decimal separator, group separator, negative symbol, number of decimal digit, currency symbol, percent symbol.

{% tabs %}

{% highlight C# %}

this.numericTextBox.FormatMode = Syncfusion.WinForms.Input.Enums.FormatMode.Currency;
this.numericTextBox.NumberFormatInfo = new System.Globalization.NumberFormatInfo();
this.numericTextBox.NumberFormatInfo.CurrencySymbol = "€";

{% endhighlight %}

{% highlight VB %}

Me.numericTextBox.FormatMode = Syncfusion.WinForms.Input.Enums.FormatMode.Currency
Me.numericTextBox.NumberFormatInfo = New System.Globalization.NumberFormatInfo()
Me.numericTextBox.NumberFormatInfo.CurrencySymbol = "€"

{% endhighlight %}

{% endtabs %}

![Formatting the value](Gettingstarted_images/Formatting.png)

## Different types of format modes

String formatting is the replacement of string in specified string format. Based on the string formatting, the numbers can be formatted into three different modes. They are

*	Numeric
*	Percent
*	Currency

This mode can be applied in SfNumericTextBox by using the [FormatMode](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~FormatMode.html) property. By default, the FormatMode is set as Numeric.

{% tabs %}

{% highlight C# %}

// To set the format mode as currency.
this.numericTextBox.FormatMode = Syncfusion.WinForms.Input.Enums.FormatMode.Currency;

{% endhighlight %}

{% highlight VB %}

' To set the format mode as currency.
Me.numericTextBox.FormatMode = Syncfusion.WinForms.Input.Enums.FormatMode.Currency

{% endhighlight %}

{% endtabs %}

![Format mode](Gettingstarted_images/Mode.png)

## Adding watermark to the control

SfNumericTextBox comes with the in-built watermark support. [WatermarkText](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~WatermarkText.html) helps to display the details about what value need to enter. [WatermarkText](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~WatermarkText.html) property allows to show the watermark for the control when the value of the control is set to null.

{% tabs %}

{% highlight C# %}

// Sets the watermark text to SfNumericTextBox.
this.numericTextBox.WatermarkText = "Enter your age";

{% endhighlight %}

{% highlight VB %}

' Sets the watermark text to SfNumericTextBox.
Me.numericTextBox.WatermarkText = "Enter your age"

{% endhighlight %}

{% endtabs %}

![Watermark support](Gettingstarted_images/Watermark.png)

## Minimum and Maximum value support

We can define the range of value which can be accept by the control. To define this range, we need to provide minimum possible value and maximum possible value using the property [MinValue](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~MinValue.html) and [MaxValue](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~MaxValue.html) respectively.

{% tabs %}

{% highlight C# %}

// The below codes assign the minimum value of SfNumericTextBox as 10 and maximum value as 100. i,e the value can accept the range between 10 to 100. 
this.numericTextBox.MinValue = 10;
this.numericTextBox.MaxValue = 100;

{% endhighlight %}

{% highlight VB %}

‘ The below codes assign the minimum value of SfNumericTextBox as 10 and maximum value as 100. i,e the value can accept the range between 10 to 100.
Me.numericTextBox.MinValue = 10
Me.numericTextBox.MaxValue = 100

{% endhighlight %}

{% endtabs %}

## Hiding the trail zeros in value

The trailing zeros after the decimal digit can be removed by using the property named [HideTrailingZeros](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~HideTrailingZeros.html).

{% tabs %}

{% highlight C# %}

// Hides the trailing zeros.
this.numericTextBox.HideTrailingZeros = true;

{% endhighlight %}

{% highlight VB %}

' Hides the trailing zeros.
Me.numericTextBox.HideTrailingZeros = True

{% endhighlight %}

{% endtabs %}

![Hide the decimal value](Gettingstarted_images/HideZeros.png)

## Adding custom units to the value

Allows to set the units or custom message at front or end of the text. This can be set using the [Prefix](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~Prefix.html) and [Suffix](https://help.syncfusion.com/cr/windowsforms/Syncfusion.SfInput.WinForms~Syncfusion.WinForms.Input.SfNumericTextBox~Suffix.html) property.

{% tabs %}

{% highlight C# %}

// Sets the custom unit in SfNumericTextBox.
this.numericTextBox.Suffix = "inches";

{% endhighlight %}

{% highlight VB %}

' Sets the custom unit in SfNumericTextBox.
Me.numericTextBox.Suffix = "inches";

{% endhighlight %}

{% endtabs %}

![Custom units added in numeric text box](Gettingstarted_images/CustomUnit.png)