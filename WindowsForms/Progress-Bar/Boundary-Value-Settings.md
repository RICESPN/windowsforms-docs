---
layout: post
title: Boundary-Value-Settings | WindowsForms | Syncfusion
description: boundary value settings
platform: WindowsForms
control: ProgressBarAdv
documentation: ug
---

# Boundary value settings

The ProgressBarAdv during it's progressive operation indicates a minimum value and a maximum value for the process.

It provides the below properties to set the boundary values for the control and also the interval for the progression.

Property table

<table>
<tr>
<th>
ProgressBarAdv property</th><th>
Description</th></tr>
<tr>
<td>
Minimum</td><td>
Determines the lower bound of the range of the ProgressBarAdv.</td></tr>
<tr>
<td>
Maximum</td><td>
Determines the higher bound of the range of the ProgressBarAdv.</td></tr>
<tr>
<td>
Value</td><td>
The current value between the minimum and maximum values.</td></tr>
<tr>
<td>
Step</td><td>
Determines the amount to increment or decrement the value of the ProgressBarAdv when the Increment() or Decrement() method is called.</td></tr>
</table>


Create a ProgressBarAdv and set the below properties to see the changes.

{% tabs %}

{% highlight C# %}

this.progressBarAdv1.Maximum = 200;

this.progressBarAdv1.Minimum = 25;

this.progressBarAdv1.Step = 50;

this.progressBarAdv1.Value = 100;

{% endhighlight %}

{% highlight VB %}

Me.progressBarAdv1.Maximum = 200

Me.progressBarAdv1.Minimum = 25

Me.progressBarAdv1.Step = 50

Me.progressBarAdv1.Value = 100

{% endhighlight %}

{% endtabs %}

![](Overview_images/Overview_img22.jpeg) 


The methods associated with the above properties are given below.

Methods table

<table>
<tr>
<th>
Methods</th><th>
Description</th></tr>
<tr>
<td>
Increment</td><td>
Increments the Value property associated with the Step value.</td></tr>
<tr>
<td>
Decrement</td><td>
Decrements the Value property associated with the Step value.</td></tr>
</table>

