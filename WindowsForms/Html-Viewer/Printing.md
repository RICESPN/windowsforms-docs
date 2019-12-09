---
layout: post
title: Printing | WindowsForms | Syncfusion
description:  printing
platform: WindowsForms
control: HTML UI
documentation: ug
---

#  Printing

The HTMLUI control supports printing that helps the user in developing a hard copy of the document displayed in the HTMLUI control. Also the Print Preview feature lets the user to preview the page before being printed, and change the page according to the requirements.

{% tabs %}

{% highlight C# %}



//Document initialization

HTMLUIPrintDocument pd = new HTMLUIPrintDocument(this.htmluiControl1.Document);



//Print Preview

PrintPreviewDialog dlg = new PrintPreviewDialog();

dlg.Document = pd;

dlg.ShowDialog();



//Print

PrintDialog dialog = new PrintDialog();

dialog.AllowSomePages = true;

dialog.Document = pd;

if (dialog.ShowDialog() == DialogResult.OK)

pd.Print();

{% endhighlight %}

{% highlight VB %}



'Document initialization

Dim pd As New HTMLUIPrintDocument(Me.HtmluiControl1.Document)



'Print Preview

Dim dlg As New PrintPreviewDialog()

dlg.Document = pd

dlg.ShowDialog()



'Print

Dim dialog As New PrintDialog()

dialog.AllowSomePages = True

dialog.Document = pd

If dialog.ShowDialog() = DialogResult.OK Then

pd.Print()

End If

{% endhighlight %}

{% endtabs %}

Along with printing feature, HTMLUI control supports previewing of the document before printing. This following code snippet shows how the print preview feature is enabled in HTMLUI.

{% tabs %}

{% highlight C# %}



// Document Initialization

private void PrintPreViewButton_Click(object sender, System.EventArgs e)

{

  HTMLUIPrintDocument pd = new HTMLUIPrintDocument(this.htmluiControl1.Document);



  // Initialize the new instance of the System.Window.Forms.PrintPreviewDialog Class

  PrintPreviewDialog dlg = new PrintPreviewDialog() ;

  dlg.Document = pd;

  dlg.ShowDialog();

}  

{% endhighlight %}

{% highlight VB %}



' Document Initialization 

Private Sub PrintPreViewButton_Click(ByVal sender As Object, ByVal e As System.EventArgs)

Dim pd As HTMLUIPrintDocument = New HTMLUIPrintDocument(Me.htmluiControl1.Document)



' Initialize the new instance of the System.Window.Forms.PrintPreviewDialog Class

Dim dlg As PrintPreviewDialog = New PrintPreviewDialog()

dlg.Document = pd

dlg.ShowDialog()

End Sub

{% endhighlight %}

{% endtabs %}

The following figure shows the Print preview page that appears when the corresponding button is clicked. This illustrates the Printing feature in HTMLUI.

![](Printing_images/Printing_img1.png)



## HTMLUIPrinting sample

This sample shows how an HTML document available in the HTMLUI can be printed.

![](Printing_images/Printing_img2.jpeg)





By default, this sample can be found under the following location:

...\_My Documents\Syncfusion\EssentialStudio\Version Number\Windows\HTMLUI.Windows\Samples\Advanced Editor Functions\ActionGroupingDemo_

