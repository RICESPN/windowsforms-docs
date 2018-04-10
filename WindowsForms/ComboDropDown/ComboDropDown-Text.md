---
layout: post
title: ComboDropDown-Text | WindowsForms | Syncfusion
description: combodropdown text
platform: WindowsForms
control: ComboDropDown
documentation: ug
---

# ComboDropDown Text

ComboDropDown control supports the properties which can change the appearance and behavior of the control's edit portion.

![](Overview_images/Overview_img284.jpeg) 



<table>
<tr>
<th>
ComboDropDown Properties</th><th>
Description</th></tr>
<tr>
<td>
CharacterCasing</td><td>
Specifies the ComboDropDown control modifies the case of characters when they are typed in the edit portion.</td></tr>
<tr>
<td>
NumberOnly</td><td>
Specifies whether the user should be forced to enter only numbers in the edit portion of ComboDropDown.</td></tr>
<tr>
<td>
ReadOnly</td><td>
Specifies whether the text in the edit portion of ComboDropDown should be set to read-only or can be changed. By default it will be set to false.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.comboDropDown1.CharacterCasing = System.Windows.Forms.CharacterCasing.Upper;
this.comboDropDown1.NumberOnly = true;
this.comboDropDown1.ReadOnly = true;
this.comboDropDown1.CaseSensitiveAutocomplete = false;
this.comboDropDown1.MatchFirstCharacterOnly = false;

{% endhighlight %}

{% highlight vb %}

Me.comboDropDown1.CharacterCasing = System.Windows.Forms.CharacterCasing.Upper
Me.comboDropDown1.NumberOnly = True
Me.comboDropDown1.ReadOnly = True
Me.comboDropDown1.CaseSensitiveAutocomplete = False
Me.comboDropDown1.MatchFirstCharacterOnly = False

{% endhighlight %}
{% endtabs %}

## Banner Text Support

We can set banner text for the ComboBoxDropDown control. Refer [BannerTextProvider](/windowsforms/bannertextprovider/overview) Component topic for more details.

![](Overview_images/Overview_img285.jpeg) 







