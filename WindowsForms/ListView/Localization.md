---
layout: post
title: Localization
description: This section explains about the Localization support in SfListView.
platform: windowsforms
control: SfListView
documentation: ug
---

# Localization           
Localization is a process of translating the application resources into different languages for some specific cultures. The SfListView can be localized by adding the resource file. The application culture can be changed by setting `CurrentUICulture` before InitializeComponent method.

## Localize at sample level
To localize the SfListView based on the  [CurrentUICulture](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.currentuiculture(v=vs.110).aspx) using resource files, follow the steps:

1) Create a new folder and name it as Resources in your application.

2) Add the default resource file of the SfListView into Resources folder.You can download the Syncfusion.SfListView.WinForms.resx [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ResourceFile1283641291).

![](Localization_images/Localization_img1.png)
                     
3) Right-click on the Resources folder, select Add and then NewItem.

4) In Add New Item wizard, select the Resource File option and name the filename as Syncfusion.SfListView.WinForms.<culture name>.resx. For example, give name as Syncfusion.SfListView.WinForms.de-DE.resx for German culture.The culture name that indicates the name of language and country.

![](Localization_images/Localization_img2.png)	 

5) Now, select Add option to add the resource file in Resources folder.

![](Localization_images/Localization_img3.png)

6) Add the Name/Value pair in Resource Designer of Syncfusion. SfListView.WinForms.de-DE.resx file and change its corresponding value to the corresponding culture.
 
 ![](Localization_images/Localization_img4.png)
 
7) Now, set the CurrentCulture of the Application before the InitializeComponent method and run the sample.

{% tabs %}
{% highlight c# %}
public Form1()
{
 System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("de-DE"); 
 System.Threading.Thread.CurrentThread.CurrentUICulture = new System.Globalization.CultureInfo("de-DE"); 
 InitializeComponent();
}
{% endhighlight %}
{% highlight vb %}
Public Sub New()
 System.Threading.Thread.CurrentThread.CurrentCulture = New System.Globalization.CultureInfo("de-DE")
 System.Threading.Thread.CurrentThread.CurrentUICulture = New System.Globalization.CultureInfo("de-DE")
 InitializeComponent()
End Sub
{% endhighlight %}
{% endtabs %}
 
![](Localization_images/Localization_img5.png)
 
## Editing default resource file
The default resource file can be edited by adding it to Resources folder of the application where the SfListView reads the static texts here.
The default resource file can be download from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ResourceFile1283641291).

![](Localization_images/Localization_img6.png)

Now, change the Name and Value pair in Resource Designer of Syncfusion.SfListView.WinForms.resx file.

![](Localization_images/Localization_img7.png)

Run the sample.

![](Localization_images/Localization_img8.png) 
 
## Localize resource file with different assembly or namespace
By default, the SfListView tries to read the resource file from executing assembly and its default namespace by using the `Assembly.GetExecuteAssembly` method. When the resource file is located at different assembly or namespace, it can be set to the SfListView by using the `SR.SetResources` method.

{% tabs %}
{% highlight c# %}
public Form1()
{
  System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("de-DE");
  System.Threading.Thread.CurrentThread.CurrentUICulture = new System.Globalization.CultureInfo("de-DE");
  SR.SetResources(typeof(CustomListView).Assembly, "SfListViewExt");
  InitializeComponent();
}
{% endhighlight %}
{% highlight vb %}
Public Sub New()
  System.Threading.Thread.CurrentThread.CurrentCulture = New System.Globalization.CultureInfo("de-DE")
  System.Threading.Thread.CurrentThread.CurrentUICulture = New System.Globalization.CultureInfo("de-DE")
  SR.SetResources(GetType(CustomListView).Assembly, "SfListViewExt")
  InitializeComponent()
End Sub
{% endhighlight %}
{% endtabs %}

## RightToLeft
Items of the SfListView can be aligned from right to left and vice versa using the following property.

{% tabs %}
{% highlight c# %}
sfListView1.RightToLeft = RightToLeft.Yes;
{% endhighlight %}
{% highlight vb %}
sfListView1.RightToLeft = RightToLeft.Yes
{% endhighlight %}
{% endtabs %}

![](Localization_images/Localization_img9.png)