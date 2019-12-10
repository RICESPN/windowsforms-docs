---
layout: post
title: Display-Settings | WindowsForms | Syncfusion
description: display settings
platform: WindowsForms
control: SplashPanel
documentation: ug
---

# Display Settings

The section illustrates the display settings available for the SplashPanel control.

The SplashPanel can be displayed or hidden according to the needs of the user. It can be displayed at any specified location. The display settings of the SplashPanel control are illustrated through the following methods.

Methods Table

<table>
<tr>
<th>
Methods</th><th>
Description</th></tr>
<tr>
<td>
ShowSplash</td><td>
Displays the SplashPanel.</td></tr>
<tr>
<td>
HideSplash</td><td>
Hides the SplashPanel.</td></tr>
<tr>
<td>
ShowDialogSplash</td><td>
Displays the SplashPanel as a modal dialog.</td></tr>
<tr>
<td>
IsShowing</td><td>
Indicates whether the splash is currently displayed.</td></tr>
</table>

N> The time interval for which the SplashPanel is displayed can be customized using the Time Interval settings provided in the SplashPanel control.

The above methods are explained below in detail.

ShowSplash() - This method is used to display the SplashPanel at run time.

The parameters discussed for the ShowSplash() method are as follows.

Parameters Table

<table>
<tr>
<th>
Parameters</th><th>
Description</th></tr>
<tr>
<td>
Location</td><td>
Indicates the point in screen coordinates. The value can be 'Point.Empty'.</td></tr>
<tr>
<td>
OwnerForm</td><td>
Indicates the form that will embed the splash form.</td></tr>
<tr>
<td>
DisableOwner</td><td>
Indicates whether the owner form is to be disabled.</td></tr>
</table>


When the SplashPanel is getting displayed, the owner form will be disabled when the DisableOwner parameter is passed as 'True'. You can assign any form as the owner form.

The below code snippet will display the SplashPanel at the specified location with the owner form being disabled. The location will be effective only when the DesktopAlignment property is set as 'Custom'.

{% tabs %}
{% highlight c# %}

Form2 f2 = new Form2();

// To display the SplashPanel call the ShowSplash() method.
this.splashPanel1.ShowSplash(new Point(100, 100), f2, true);

{% endhighlight %}

{% highlight vb %}

Private f2 As Form2 = New Form2

' To display the SplashPanel call the ShowSplash() method.
Me.splashPanel1.ShowSplash(New Point(100,100), f2, True)

{% endhighlight %}
{% endtabs %}

* HideSplash() - The SplashPanel can be hidden by calling this method at run time.

{% tabs %}
{% highlight c# %}

// To hide the SplashPanel call the HideSplash() method.
this.splashPanel1.HideSplash();

{% endhighlight %}

{% highlight vb %}

' To hide the SplashPanel call the HideSplash() method.
Me.splashPanel1.HideSplash()

{% endhighlight %}
{% endtabs %}

* ShowSplashDialog() -The method is used to display the SplashPanel as a modal dialog during run time. 

When this method is called, the user will not be able to interact with the application until the SplashPanel is closed. This is the only difference between the ShowSplash() method and this method.

The parameters discussed for the method are as follows.

Parameters Table

<table>
<tr>
<th>
Parameters</th><th>
Description</th></tr>
<tr>
<td>
OwnerForm</td><td>
Represents the owner form.</td></tr>
<tr>
<td>
Location </td><td>
Specifies the location at which the SplashPanel will be displayed.</td></tr>
</table>


The SplashPanel will be displayed at the position / location specified in this method. By passing a new instance of the owner form to this method, we can display the SplashPanel as a modal dialog.

The below example uses a button click event to call this method. This method is overloaded.

{% tabs %}
{% highlight c# %}

private void button1_Click(object sender, EventArgs e)
{
    this.splashPanel1.ShowDialogSplash(new Point(700, 700), new Form1());
}

{% endhighlight %}

{% highlight vb %}

Private Sub button1_Click(ByVal sender As Object, ByVal e As EventArgs)
Me.splashPanel1.ShowDialogSplash(New Point(700, 700), New Form1())
End Sub

{% endhighlight %}
{% endtabs %}

This overloaded method passes the owner form as a parameter to this method.

{% tabs %}
{% highlight c# %}

private void button1_Click(object sender, EventArgs e)
{
    this.splashPanel1.ShowDialogSplash(new Form1());
}

{% endhighlight %}

{% highlight vb %}

Private Sub button1_Click(ByVal sender As Object, ByVal e As EventArgs)
Me.splashPanel1.ShowDialogSplash(New Form1())
End Sub

{% endhighlight %}
{% endtabs %}

* IsShowing() - This method will tell you whether the SplashPanel is currently displayed or not. This method returns 'True' if the SplashPanel is displayed and 'False' if it is not displayed.

You can call this method in a button click event and view the result in the output window as given below.

{% tabs %}
{% highlight c# %}

// To know whether splash screen is showing
private void button1_Click_1(object sender, EventArgs e)
{
    this.splashPanel1.IsShowing();
    Console.Write(this.splashPanel1.IsShowing());
}

{% endhighlight %}

{% highlight vb %}

' To know whether splash screen is showing
Private Sub button1_Click(ByVal sender As Object, ByVal e As EventArgs)
Me.splashPanel1.IsShowing()
Console.Write(Me.splashPanel1.IsShowing())
End Sub

{% endhighlight %}
{% endtabs %}

### Location

The location for displaying the splash window is specified using the property given below.

Property Table

<table>
<tr>
<th>
SplashPanel Property</th><th>
Description</th></tr>
<tr>
<td>
DiscreetLocation</td><td>
Gets / sets the location to display the splash window. </td></tr>
</table>

A Sample which demonstrates the ShowSplash() and ShowSplashDialog() methods is available in the below sample installation path.

…\My Documents\Syncfusion\EssentialStudio\Version Number\Windows\Tools.Windows\Samples\Advanced Editor Functions\ActionGroupingDemo

## SplashPanel in TaskBar

The SplashPanel can be displayed in the taskbar and it's appearance can be customized using the properties given below.

Property Table

<table>
<tr>
<th>
SplashPanel Property</th><th>
Description</th></tr>
<tr>
<td>
ShowInTaskBar</td><td>
Specifies if the SplashPanel is to be shown in the taskbar.</td></tr>
<tr>
<td>
FormIcon</td><td>
Gets / sets the icon for the SplashPanel.</td></tr>
<tr>
<td>
Text</td><td>
Specifies the text when displayed in the taskbar.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.splashPanel1.ShowInTaskbar = true;
this.splashControl1.FormIcon = ((System.Drawing.Icon)(resources.GetObject("splashControl1.FormIcon")));
this.splashPanel1.Text = "Splash Panel";

{% endhighlight %}

{% highlight vb %}

Me.splashPanel1.ShowInTaskbar = true
Me.splashControl1.FormIcon = DirectCast((resources.GetObject("splashControl1.FormIcon")), System.Drawing.Icon)
Me.splashPanel1.Text = "Splash Panel"

{% endhighlight %}
{% endtabs %}

![](Overview_images/Overview_img50.jpeg) 


## Time interval

The SplashPanel is, by default, a timed display splash screen. The SplashPanel uses internally, a System.Windows.Forms.Timer, to automatically close the splash screen after the set interval is elapsed. This behavior can be changed by setting the TimerInterval property to -1. 

Property Table

<table>
<tr>
<th>
SplashPanel Property</th><th>
Description</th></tr>
<tr>
<td>
TimerInterval</td><td>
The time interval for which the splash screen should be displayed (in milliseconds).</td></tr>
</table>

The splash screen will be displayed for a specific time period and will then be closed.

{% tabs %}
{% highlight c# %}

this.splashPanel1.TimerInterval = 7000;

{% endhighlight %}

{% highlight vb %}

Me.splashPanel1.TimerInterval = 7000

{% endhighlight %}
{% endtabs %}

## Behavior settings

The user will not be able to close or resize the splash image, which is displayed during run time, normally. But by setting certain properties of the SplashPanel, the user can alter the SplashPanel. These properties are explained below in detail.

Property Table

<table>
<tr>
<th>
SplashPanel Property</th><th>
Description</th></tr>
<tr>
<td>
AllowMove</td><td>
Indicates whether the SplashPanel can be moved by the user at run time.</td></tr>
<tr>
<td>
AllowResize</td><td>
Indicates whether the SplashPanel can be resized by the user at run time.</td></tr>
<tr>
<td>
CloseOnClick</td><td>
Indicates whether the SplashPanel gets closed when the user clicks on it.</td></tr>
</table>


When the AllowMove property is set to 'True', the user will be allowed to click within the SplashPanel and move the SplashPanel on the screen.

When the AllowResize property is set to 'True', resize handles will be displayed when the user moves the mouse near the border of the SplashPanel.

N> In the above cases, the splash panel will not be closed, until the host form is closed.

The user can also close the SplashPanel by a single mouse click. This feature can be enabled by setting the CloseOnClick property to 'True'.

{% tabs %}
{% highlight c# %}

this.splashPanel1.AllowMove = true;
this.splashPanel1.AllowResize = true;
this.splashPanel1.CloseOnClick = true;

{% endhighlight %}

{% highlight vb %}

Me.splashPanel1.AllowMove = True
Me.splashPanel1.AllowResize = True
Me.splashPanel1.CloseOnClick = True

{% endhighlight %}
{% endtabs %}
