---
layout: post
title: SplashPanel-Events | WindowsForms | Syncfusion
description: splashpanel events
platform: WindowsForms
control: SplashPanel
documentation: ug
---

# SplashPanel Events

The list of events and a detailed explanation about each of them is given in the following sections.

Events Table

<table>
<tr>
<th>
SplashPanel Events</th><th>
Description</th></tr>
<tr>
<td>
BeforeSplash</td><td>
Specifies the function which will be triggered before the splash image is displayed.</td></tr>
<tr>
<td>
SplashDisplayed</td><td>
Specifies the function which will be triggered when splash image is displayed.</td></tr>
<tr>
<td>
SplashClosing</td><td>
Specifies the function which will be triggered when the splash image is closing.</td></tr>
<tr>
<td>
SplashClosed</td><td>
Specifies the function which will be triggered when the splash image is closed.</td></tr>
<tr>
<td>
SplashMouseEnter</td><td>
Specifies the function which will be triggered when mouse enters the splash image.</td></tr>
<tr>
<td>
SplashMouseLeave</td><td>
Specifies the function which will be triggered when the mouse leaves the splash image.</td></tr>
</table>


Follow the below steps and use the corresponding events to get the results.

1. Create a SplashPanel and a TextBox in a form.
2. Set the textbox properties and add the textbox to the form as given below.

{% tabs %}
{% highlight c# %}

// Declare the controls.
private Syncfusion.Windows.Forms.Tools.SplashPanel splashPanel1;
private System.Windows.Forms.TextBox textBox1;
private delegate void SetStringDelegate(string val);
private Point currentPt1;

// Initialize the controls.
this.splashPanel1 = new Syncfusion.Windows.Forms.Tools.SplashPanel();
this.textBox1 = new System.Windows.Forms.TextBox();

// Set the properties for the textbox.
this.textBox1.Dock = System.Windows.Forms.DockStyle.Fill;
this.textBox1.ForeColor = System.Drawing.Color.Black;
this.textBox1.Location = new System.Drawing.Point(0, 0);
this.textBox1.Multiline = true;
this.textBox1.Name = "textBox1";
this.textBox1.ScrollBars = System.Windows.Forms.ScrollBars.Vertical;
this.textBox1.Size = new System.Drawing.Size(248, 142);
this.textBox1.TabIndex = 4;
this.textBox1.Text = "";

// Add the textbox to the form.
this.Controls.Add(this.textBox1);
private void OutputText(string text)
{
    textBox1.Text = textBox1.Text + text;
}

{% endhighlight %}

{% highlight vb %}

' Declare the controls.
Friend WithEvents splashPanel1 As Syncfusion.Windows.Forms.Tools.SplashPanel
Friend WithEvents textBox1 As System.Windows.Forms.TextBox
Private Delegate Sub SetStringDelegate(ByVal val As String) 'Any string value
Private currentPt1 As Point

' Initialize the controls.
Me.splashPanel1 = New Syncfusion.Windows.Forms.Tools.SplashPanel
Me.textBox1 = New System.Windows.Forms.TextBox

' Set the properties for the textbox.
Me.textBox1.Dock = System.Windows.Forms.DockStyle.Fill
Me.textBox1.ForeColor = System.Drawing.Color.Black
Me.textBox1.Location = New System.Drawing.Point(0, 0)
Me.textBox1.Multiline = True
Me.textBox1.Name = "textBox1"
Me.textBox1.ScrollBars = System.Windows.Forms.ScrollBars.Vertical
Me.textBox1.Size = New System.Drawing.Size(272, 190)
Me.textBox1.TabIndex = 5
Me.textBox1.Text = ""

' Add the textbox to the form.
Me.Controls.Add(Me.textBox1)
Private Sub OutputText(ByVal text As String)
textBox1.Text = textBox1.Text & text
End Sub

{% endhighlight %}
{% endtabs %}

## BeforeSplash event

When the application is loaded and before the splash screen is displayed, the BeforeSplash event will be triggered.

### Event data

The event handler receives an argument of type CancelEventArgs containing data related to this event. The following CancelEventArgs member provides information specific to this event.

Member Table

<table>
<tr>
<th>
Member</th><th>
Description</th></tr>
<tr>
<td>
Cancel</td><td>
Indicates whether the event should be canceled.</td></tr>
</table>

You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the BeforeSplash event.
this.splashPanel1.BeforeSplash +=new CancelEventHandler(splashPanel1_BeforeSplash);
private void splashPanel1_BeforeSplash(object sender, System.ComponentModel.CancelEventArgs e)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "BeforeSplash", ((Control)sender).Name);
    textBox1.Text = textBox1.Text + message;

// To cancel this event, give the below code.
    args.Cancel = true;
}

{% endhighlight %}

{% highlight vb %}

' Handle the BeforeSplash event.
AddHandler Me.splashPanel1.BeforeSplash, AddressOf splashPanel1_BeforeSplash
Private Sub splashPanel1_BeforeSplash(ByVal sender As Object, ByVal e As System.ComponentModel.CancelEventArgs) Handles splashPanel1.BeforeSplash
Dim message As String = String.Format("Event: {0} Object: {1}" & Constants.vbCrLf, "BeforeSplash", (CType(sender, Control)).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(AddressOf OutputText), New Object() { message })
Else
OutputText(message)
End If

' To cancel this event, give the below code.
args.Cancel = True
End Sub

{% endhighlight %}
{% endtabs %}


## SplashDisplayed event

When the application is loaded and when the SplashPanel is displayed, the SplashDisplayed event will be raised. The event handler receives an argument of type EventArgs containing data related to this event.

You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the SplashDisplayed event.
this.splashPanel1.SplashDisplayed +=new EventHandler(splashPanel1_SplashDisplayed);
private void splashPanel1_SplashDisplayed(object sender, System.EventArgs e)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "SplashDisplayed", ((Control)sender).Name);
    if (this.InvokeRequired)
    {
        this.Invoke(new SetStringDelegate(OutputText), new object[] { message });
    }
    else
    {
        textBox1.Text = textBox1.Text + message;
    }
}

{% endhighlight %}

{% highlight vb %}

' Handle the SplashDisplayed event.
AddHandler Me.splashPanel1.SplashDisplayed, AddressOf splashPanel1_SplashDisplayed
Private Sub splashPanel1_SplashDisplayed(ByVal sender As Object, ByVal e As System.EventArgs) Handles splashPanel1.SplashDisplayed
Dim message As String = String.Format("Event: {0} Object: {1}" & Constants.vbCrLf, "SplashDisplayed", (CType(sender, Control)).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(AddressOf OutputText), New Object() { message })
Else
OutputText(message)
End If
End Sub

{% endhighlight %}
{% endtabs %}

## SplashClosing event

At run time, after the splash screen is displayed for a specified time and when it is closing, the SplashClosing event will be triggered.

### Event data

The event handler receives an argument of type CancelEventArgs containing data related to this event. The following CancelEventArgs member provides information specific to this event.

Member Table

<table>
<tr>
<th>
Member</th><th>
Description</th></tr>
<tr>
<td>
Cancel</td><td>
Indicates whether the event should be canceled.</td></tr>
</table>


You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the SplashClosing event.
this.splashPanel1.SplashClosing +=new CancelEventHandler(splashPanel1_SplashClosing);
private void splashPanel1_SplashClosing(object sender, Syncfusion.Windows.Forms.Tools.SplashClosedEventArgs args)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "SplashClosing", ((Control)sender).Name);
    if (this.InvokeRequired)
    {
        this.Invoke(new SetStringDelegate(OutputText), new object[] { message });
    }
    else
    {
        OutputText(message);
    }
    if(this.Controls.Contains(this.splashPanel1) == false)
    this.Controls.Add(this.splashPanel1);
    this.splashPanel1.Location = this.currentPt1;
    this.splashPanel1.Visible = true;
}

{% endhighlight %}

{% highlight vb %}

' Handle the SplashClosing event.
AddHandler Me.splashPanel1.SplashClosing, AddressOf splashPanel1_SplashClosing
Private Sub splashPanel1_SplashClosing(ByVal sender As Object, ByVal args As Syncfusion.Windows.Forms.Tools.SplashClosedEventArgs)
Dim message As String = [String].Format("Event: {0} Object: {1}" & Chm(13) & "" & Chm(10) & "", "SplashClosing", DirectCast(sender, Control).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(OutputText), New Object() {message})
Else
OutputText(message)
End If
If Me.Controls.Contains(Me.splashPanel1) = False Then
Me.Controls.Add(Me.splashPanel1)
End If
Me.splashPanel1.Location = Me.currentPt1
Me.splashPanel1.Visible = True
End Sub

{% endhighlight %}
{% endtabs %}

## SplashClosed event

At run time, after the splash screen is displayed for a specified time and when it is closed, the SplashClosed event will be triggered.

### Event data

The event handler receives an argument of type SplashClosedEventArgs containing data related to this event. The following SplashClosedEventArgs member provides information specific to this event.

Member Table

<table>
<tr>
<th>
Member</th><th>
Description</th></tr>
<tr>
<td>
SplashCloseType</td><td>
Returns the value which indicates the way in which the splash was closed.</td></tr>
</table>

You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the SplashClosed event.
this.splashPanel1.SplashClosed +=new SplashClosedEventHandler(splashPanel1_SplashClosed);
private void splashPanel1_SplashClosed(object sender, Syncfusion.Windows.Forms.Tools.SplashClosedEventArgs args)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "SplashClosing", ((Control)sender).Name);
    if (this.InvokeRequired)
    {
        this.Invoke(new SetStringDelegate(OutputText), new object[] { message });
    }
    else
    {
        OutputText(message);
    }
    if(this.Controls.Contains(this.splashPanel1) == false)
    this.Controls.Add(this.splashPanel1);
    this.splashPanel1.Location = this.currentPt1;
    this.splashPanel1.Visible = true;

// Returns the SplashCloseType value indicating the way in which the splash was closed.
    args.SplashCloseType.ToString();
}

{% endhighlight %}

{% highlight vb %}

' Handle the SplashClosed event.
AddHandler Me.splashPanel1.SplashClosed, AddressOf splashPanel1_SplashClosed
Private Sub splashPanel1_SplashClosed(ByVal sender As Object, ByVal args As Syncfusion.Windows.Forms.Tools.SplashClosedEventArgs) Handles splashPanel1.SplashClosed
Dim message As String = String.Format("Event: {0} Object: {1}" & Constants.vbCrLf, "SplashClosing", (CType(sender, Control)).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(AddressOf OutputText), New Object() { message })
Else
OutputText(message)
End If
If Me.Controls.Contains(Me.splashPanel1) = False Then
Me.Controls.Add(Me.splashPanel1)
End If
Me.splashPanel1.Location = Me.currentPt1
Me.splashPanel1.Visible = True

' Returns the SplashCloseType value indicating the way in which the splash was closed.
args.SplashCloseType.ToString()
End Sub

{% endhighlight %}
{% endtabs %}

SplashClosed event is raised when the SplashFormClosedNotify() method is called. This method is an implementation of the ISplashWrapperFormListener for receiving notification from the SplashWrapperForm when the splash window is closed.

{% tabs %}
{% highlight c# %}

this.splashPanel1.SplashFormClosedNotify();

{% endhighlight %}

{% highlight vb %}

Me.splashPanel1.SplashFormClosedNotify()

{% endhighlight %}
{% endtabs %}

## SplashMouseEnter event

When an application with SplashPanel is loaded, the splash screen will be displayed based on the alignment that is set. At this time, when the mouse is moved over the SplashPanel that is visible in the application, the SplashMouseEnter event will be raised. This event will not be triggered after the splash screen is closed.

The event handler receives an argument of type EventArgs containing data related to this event.

You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the SplashMouseEnter event.
this.splashPanel1.SplashMouseEnter +=new EventHandler(splashPanel1_SplashMouseEnter);
private void splashPanel1_SplashMouseEnter(object sender, System.EventArgs e)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "SplashMouseEnter", ((Control)sender).Name);
    if (this.InvokeRequired)
    {
        this.Invoke(new SetStringDelegate(OutputText), new object[] { message });
    }
    else
    {
        OutputText(message);
    }
}

{% endhighlight %}

{% highlight vb %}

' Handle the SplashMouseEnter event.
AddHandler Me.splashPanel1.SplashMouseEnter, AddressOf splashPanel1_SplashMouseEnter
Private Sub splashPanel1_SplashMouseEnter(ByVal sender As Object, ByVal e As System.EventArgs) Handles splashPanel1.SplashMouseEnter
Dim message As String = String.Format("Event: {0} Object: {1}" & Constants.vbCrLf, "SplashMouseEnter", (CType(sender, Control)).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(AddressOf OutputText), New Object() { message })
Else
OutputText(message)
End If
End Sub

{% endhighlight %}
{% endtabs %}

## SplashMouseLeave event

When an application with SplashPanel is loaded, the splash screen will be displayed based on the alignment that is set. At this time, when the mouse moves over the SplashPanel and then leaves the SplashPanel, the SplashMouseLeave event will be raised. This event will not be triggered after the splash screen is closed.

The event handler receives an argument of type EventArgs containing data related to this event.

You can handle this event by including the below code.

{% tabs %}
{% highlight c# %}

// Handle the SplashMouseLeave event.
this.splashPanel1.SplashMouseLeave +=new EventHandler(splashPanel1_SplashMouseLeave);
private void splashPanel1_SplashMouseLeave(object sender, System.EventArgs e)
{
    string message = String.Format("Event: {0} Object: {1}\r\n", "SplashMouseLeave", ((Control)sender).Name);
    if (this.InvokeRequired)
    {
        this.Invoke(new SetStringDelegate(OutputText), new object[] { message });
    }
    else
    {
        string text = message;
        textBox1.Text = textBox1.Text + text;
    }
}

{% endhighlight %}

{% highlight vb %}

' Handle the SplashMouseLeave event.
AddHandler Me.splashPanel1.SplashMouseLeave, AddressOf splashPanel1_SplashMouseLeave
Private Sub splashPanel1_SplashMouseLeave(ByVal sender As Object, ByVal e As System.EventArgs) Handles splashPanel1.SplashMouseLeave
Dim message As String = String.Format("Event: {0} Object: {1}" & Constants.vbCrLf, "SplashMouseLeave", (CType(sender, Control)).Name)
If Me.InvokeRequired Then
Me.Invoke(New SetStringDelegate(AddressOf OutputText), New Object() { message })
Else
OutputText(message)
End If
End Sub

{% endhighlight %}
{% endtabs %}
