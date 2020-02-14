---
layout: post
title: Overview in Tooltip Control for Windows Forms | Syncfusion
description: This section explains about the tooltip component for windows forms and it's important key features such as multiple items, tooltip customization and etc
platform: windowsforms
control: SfToolTip
documentation: ug

---
# Windows Forms Tooltip (SfToolTip) Overview

The `SfToolTip` appears automatically as a pop-up and shows the information of purpose of the control when resetting the pointer on the control. The control includes the control adding feature that allows an end user to add the user control to the SfToolTip so, end user can customize any ToolTip item in the `SfToolTip`.

## Key Features

Following are the key features of the `SfToolTip` :

* `Multiple items` : Supports adding more tooltip items.
* `Adding controls` : Supports loading a control in the tooltip item.
* `ToolTip content customization` : Supports customizing the appearance of the tooltip item.

## Choose between different tooltip controls

Syncfusion WinForms suite comes up with following different tooltips namely :

* [SfToolTip](https://www.syncfusion.com/products/windows-forms/tooltip)
* [SuperToolTip](https://help.syncfusion.com/windowsforms/supertooltip/supertooltip)

### SfToolTip

[SfToolTip](https://help.syncfusion.com/windowsforms/sftooltip/overview) is a component that provides options to display multiple lines, multiple items, and balloon styles. This also provides support to load images and host any custom UI control.

### SuperToolTip

[SuperToolTip](https://help.syncfusion.com/windowsforms/supertooltip/supertooltip) component is used to display text and image with various customization options. This also allows you to customize the back color, fore color, separator and html text.

### SfToolTip vs SuperToolTip

Both SfToolTip and SuperToolTip controls are used for the same purposes. But, the SfToolTip control offers rich set of features over SuperToolTip. When multi items support and specific tooltip customization are needed, use SfToolTip. Comparatively, the style customization of the SfToolTip control is better than SuperToolTip.

You can see some of the specific API differences between SfToolTip and SuperToolTip as follows.

<table>
<tr>
<td>
{{'**SfToolTip**'| markdownify }}
</td>
<td>
{{'**SuperToolTip**'| markdownify }}
</td>
<td>
{{'**Description**'| markdownify }}
</td>
</tr>
<tr>
<td>
Text
</td>
<td>
Text
</td>
<td>
Sets the text to be displayed in the tooltip item.
</td>
</tr>
<tr>
<td>
Image
</td>
<td>
Image
</td>
<td>
Sets the image to be shown on the tooltip.
</td>
</tr>
<tr>
<td>
AutoPopDelay
</td>
<td>
ToolTipDuration
</td>
<td>
Specifies the duration of the tooltip to be visible.
</td>
</tr>
<tr>
<td>
ToolTipInfo.ToolTipStyle
</td>
<td>
Style
</td>
<td>
Specifies the style of the tooltip: Regular rectangle or balloon style.
</td>
</tr>
<tr>
<td>
ToolTipInfo.MaxWidth
</td>
<td>
MaxWidth
</td>
<td>
Specifies the maximum width of the tooltip.
</td>
</tr>
</table>

The following list of features are in SfToolTip over SuperToolTip.

<table>
<tr>
<td>
{{'**Feature**'| markdownify }}
</td>
<td>
{{'**Description**'| markdownify }}
</td>
</tr>
<tr>
<td>
Multiple items
</td>
<td>
Adds multiple items as tooltip. To learn more about adding control as a pop-up information, refer to {{'[here](https://help.syncfusion.com/windowsforms/sftooltip/tooltip-content#adding-multiple-items-into-a-tooltip)'| markdownify }}.

</td>
</tr>
<tr>
<td>
 custom user control
</td>
<td>
Adds control as pop-up information. To learn more about custom user control, refer to {{'[here](https://help.syncfusion.com/windowsforms/sftooltip/tooltip-content#adding-custom-user-control-into-a-tooltip)'| markdownify }}. 

</td>
</tr>
<tr>
<td>
Custom drawing
</td>
<td>
Draws the custom tooltip item appearance. To learn more about drawing custom tooltip, refer to {{'[here](https://help.syncfusion.com/windowsforms/sftooltip/working-with-sftooltip#custom-drawing-of-tooltip)'| markdownify }}.
</td>
</tr>
<tr>
<td>
Appearance customization
</td>
<td>
Individually customizes the appearance of tooltip item shown using SfToolTip, whereas all tooltip items shown using SuperToolTip can have the same appearance. To learn more about appearance customization, refer to {{'[here](https://help.syncfusion.com/windowsforms/sftooltip/appearance)'| markdownify }}.
</td>
</tr>
</table>
