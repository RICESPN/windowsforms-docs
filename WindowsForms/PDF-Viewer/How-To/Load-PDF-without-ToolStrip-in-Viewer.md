---
layout: post
title: Load-PDF-without-ToolStrip-in-Viewer | Windows Forms | Syncfusion
description: Learn how to load the pdf without the toolstrip in viewer by using PdfDocumentView control instead of PdfViewerControl.
platform: windowsforms
control: PdfViewerControl
documentation: ug
---

# Load PDF without Toolbar

In order to view PDF without the toolbar, make use of PdfDocumentView control instead of PdfViewerControl. Other features and options are similar to PdfViewerControl.


{% tabs %}
{%highlight c#%}
PdfDocumentView pdfDocumentView1 = new PdfDocumentView();

pdfDocumentView1.Load("Sample.pdf");

{%endhighlight%}

{%highlight vb%}
Dim pdfDocumentView1 As New PdfDocumentView()

pdfDocumentView1.Load("Sample.pdf")

{%endhighlight%}
{% endtabs %}

The following is the image of a PDF document viewed in PdfDocumentView.

![Load PDF Without Toolstrip in Windows PDF Viewer](Load-PDF-without-ToolStrip-in-Viewer_images/Load-PDF-without-ToolStrip-in-Viewer_img1.png)



