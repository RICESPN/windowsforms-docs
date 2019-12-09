---
layout: post
title: Image-Settings | WindowsForms | Syncfusion
description: image settings
platform: WindowsForms
control: EditorsPackage
documentation: ug
---

# Image Settings

The image settings of the CheckBoxAdv control has been discussed in this section.

Images can be set to the CheckBoxAdv when it is in the Checked, Unchecked or Indeterminate state. The CheckBoxAdv allows us to set the following properties in order to display images.

<table>
<tr>
<th>
CheckBoxAdv Properties</th><th>
Description</th></tr>
<tr>
<td>
ImageCheckBox</td><td>
Indicates whether the CheckBox will be drawn using the images provided.</td></tr>
<tr>
<td>
ImageCheckBoxSize</td><td>
Gets or sets the size of the ImageCheckBox.ImageCheckbox property must be set to 'True'.</td></tr>
<tr>
<td>
CheckedImage</td><td>
Gets or sets the image used to draw the CheckBox when checked and mouse not over.</td></tr>
<tr>
<td>
UncheckedImage</td><td>
Gets or sets the image used to draw the CheckBox when unchecked and mouse not over.</td></tr>
<tr>
<td>
IndeterminateImage</td><td>
The image used to draw the CheckBox when indeterminate and mouse not over.</td></tr>
<tr>
<td>
DisabledImage</td><td>
Gets or sets the image used to draw the CheckBox when disabled.</td></tr>
<tr>
<td>
StretchImage</td><td>
Indicates whether the state images of the CheckBox are stretched.</td></tr>
</table>

N> Before setting the images, make sure the ImageCheckBox property is set to 'True'.

{% tabs %}
{% highlight c# %}

this.checkBoxAdv1.ImageCheckBox = true;
this.checkBoxAdv1.ImageCheckBoxSize = new System.Drawing.Size(15, 15);
this.checkBoxAdv1.CheckedImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.CheckedImage")));

this.checkBoxAdv1.UncheckedImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.UncheckedImage")));
this.checkBoxAdv1.IndeterminateImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.IndeterminateImage")));
this.checkBoxAdv1.DisabledImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.DisabledImage")));
this.checkBoxAdv1.StretchImage = false;

{% endhighlight %}

{% highlight vb %}

Me.checkBoxAdv1.ImageCheckBox = True
Me.checkBoxAdv1.ImageCheckBoxSize = New System.Drawing.Size(15, 15)
Me.checkBoxAdv1.CheckedImage = (CType(Resources.GetObject("checkBoxAdv1.CheckedImage"), System.Drawing.Image))

Me.checkBoxAdv1.UncheckedImage = (CType(Resources.GetObject("checkBoxAdv1.UncheckedImage"), System.Drawing.Image))
Me.checkBoxAdv1.IndeterminateImage = (CType(Resources.GetObject("checkBoxAdv1.IndeterminateImage"), System.Drawing.Image))
Me.checkBoxAdv1.DisabledImage = (CType(Resources.GetObject("checkBoxAdv1.DisabledImage"), System.Drawing.Image))
Me.checkBoxAdv1.StretchImage = False

{% endhighlight %}
{% endtabs %}

![Windows forms CheckBoxAdv images displayed in control when it is in checked](Overview_images/CheckBoxAdv_image.jpeg)

## Images Displayed during Mouse Hover

Images can also be set when the mouse is hovered over the CheckBoxAdv control.

<table>
<tr>
<th>
CheckBoxAdv Properties</th><th>
Description</th></tr>
<tr>
<td>
MouseOverCheckedImage</td><td>
Gets or sets the image used to draw the CheckBox when checked and mouse over.</td></tr>
<tr>
<td>
MouseOverDisabledImage</td><td>
Gets or sets the image used to draw the CheckBox when indeterminate and mouse over.</td></tr>
<tr>
<td>
MouseOverUncheckedImage</td><td>
Gets or sets the image used to draw the CheckBox when unchecked and mouse over.</td></tr>
</table>

{% tabs %}
{% highlight c# %}

this.checkBoxAdv1.MouseOverCheckedImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.MouseOverCheckedImage")));
this.checkBoxAdv1.MouseOverIndetermImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.MouseOverIndetermImage")));
this.checkBoxAdv1.MouseOverUncheckedImage = ((System.Drawing.Image)(resources.GetObject("checkBoxAdv1.MouseOverUncheckedImage")));

{% endhighlight %}

{% highlight vb %}

Me.checkBoxAdv1.MouseOverCheckedImage = (CType(Resources.GetObject("checkBoxAdv1.MouseOverCheckedImage"), System.Drawing.Image))
Me.checkBoxAdv1.MouseOverIndetermImage = (CType(Resources.GetObject("checkBoxAdv1.MouseOverIndetermImage"), System.Drawing.Image))
Me.checkBoxAdv1.MouseOverUncheckedImage = (CType(Resources.GetObject("checkBoxAdv1.MouseOverUncheckedImage"), System.Drawing.Image))

{% endhighlight %}
{% endtabs %}

 ![Windows forms CheckBoxAdv images displayed during Mouse hovered on control](Overview_images/CheckBoxAdv_changeimage.jpeg)

