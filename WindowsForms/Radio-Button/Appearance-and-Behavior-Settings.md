---
layout: post
title: Appearance-and-Behavior-Settings | WindowsForms | Syncfusion
description: appearance and behavior settings
platform: WindowsForms
control: RadioButtonAdv
documentation: ug
---

# Appearance and Behavior Settings

This section discusses the appearance and behavior settings of the RadioButtonAdv control.

## Appearance settings

### DrawFocusRectangle

The focus rectangle can be hidden or made visible using the below given property.

<table>
<tr>
<th>
RadioButtonAdv Property</th><th>
Description</th></tr>
<tr>
<td>
DrawFocusRectangle</td><td>
Determines if the focus rectangle is visible when it gets the focus. The default value is set to 'True'.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.radioButtonAdv1.DrawFocusRectangle = true;

{% endhighlight %}

{% highlight vb %}

Me.radioButtonAdv1.DrawFocusRectangle = True

{% endhighlight %}
{% endtabs %}

## Behavior settings

### AutoHeight

The height of the RadioButtonAdv can be automatically set using the property given below.


<table>
<tr>
<th>
RadioButtonAdv Property</th><th>
Description</th></tr>
<tr>
<td>
AutoHeight</td><td>
Determines if the RadioButton will automatically calculate its height.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.radioButtonAdv1.AutoHeight = true;

{% endhighlight %}

{% highlight vb %}

Me.radioButtonAdv1.AutoHeight = True

{% endhighlight %}
{% endtabs %}

### RaiseEventOnClick

The below given property can be used to fire the OnClick event of the RadioButtonAdv.


<table>
<tr>
<th>
RadioButtonAdv Property</th><th>
Description</th></tr>
<tr>
<td>
RaiseEventOnClick</td><td>
Specifies whether the OnClick event should be fired. The default value is set to 'True'.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.radioButtonAdv1.RaiseEventOnClick = true;

{% endhighlight %}

{% highlight vb %}

Me.radioButtonAdv1.RaiseEventOnClick = True

{% endhighlight %}
{% endtabs %}
