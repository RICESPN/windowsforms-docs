---
layout: post
title: Bookmark Navigation in Windows Forms PDF Viewer | Syncfusion
description: Bookmark navigation allows users to view the bookmarks and navigate to the destination saved in the bookmarks in PDF Viewer Windows Forms Application.
platform: windowsforms
control: PdfViewerControl
documentation: ug
---

# Bookmark Navigation in Windows Forms PDF Viewer (PdfViewerControl)

PDF Viewer control allows users to navigate to the bookmarks present in the loaded PDF document at the UI level. 

## Steps to perform bookmark navigation in PdfViewerControl.

1.	Open the bookmarks contained PDF document to enable the bookmark button in `PdfViewerControl`.
2.	Clicking on the bookmark button from the left pane will list the bookmarks present in the PDF document.
3.	To jump to a specific section, click its name in the bookmark pane.
4.	If the bookmark has some children, you can explore them by clicking on the “+” button to the left of it.

![Bookmark Button](Bookmark_Navigation_images/Bookmark_Navigation_images1.png)  

## Programmatically navigate to a bookmark destination

You can navigate to the desired bookmark destination using the `GotoBookmark(PdfBookmark)` method in `PdfDocumentView`. The target/destination bookmark should be provided as the parameter to this method. Refer to the following code sample.

{% tabs %}
{% highlight c# %}

//Loads the PDF document in PdfLoadedDocument
PdfLoadedDocument loadedDocument = new PdfLoadedDocument(documentStream);

//Retrieves the bookmark collection from the loaded PDF document
PdfBookmarkBase bookmark = loadedDocument.Bookmarks;

//Navigate to the specified bookmark destination offset
pdfDocumentView.GoToBookmark(bookmark[0]);

{% endhighlight %}
{% highlight VB %}

Loads the PDF document in PdfLoadedDocument
Dim loadedDocument As PdfLoadedDocument = New PdfLoadedDocument(documentStream)

`Retrieves the bookmark collection from the loaded PDF document
Dim bookmark As PdfBookmarkBase = loadedDocument.Bookmarks

`Navigate to the specified bookmark destination offset
pdfDocumentView.GoToBookmark(bookmark(0))

{% endhighlight %}
{% endtabs %}

## Enabling and disabling bookmark feature

You can enable and disable the bookmark button from the built-in toolbar using the `IsBookmarkEnabled` property available in `PdfViewerControl`.

<table>
<tr>
<th>
Property</th><th>
Action</th></tr>
<tr>
<td>
{{'[IsBookmarkEnabled](https://help.syncfusion.com/cr/windowsforms/Syncfusion.Windows.Forms.PdfViewer.PdfViewerControl.html#Syncfusion_Windows_Forms_PdfViewer_PdfViewerControl_IsBookmarkEnabled)'| markdownify }}</td><td>
Enables or disables the bookmark feature.</td></tr>
</table>

This property removes the bookmark button and disables the bookmark feature when it is set to false and vice versa.

{% tabs %}
{% highlight c# %}

//Bookmark feature is disabled
pdfViewerControl.IsBookmarkEnabled = false;

{% endhighlight %}
{% highlight VB %}

'Bookmark feature is disabled
pdfViewerControl.IsBookmarkEnabled = false

{% endhighlight %}
{% endtabs %}

The following screenshot shown the Bookmark navigation in `PdfViewerControl`,

![Bookmark Navigation](Bookmark_Navigation_images/Bookmark_Navigation_images2.png)
