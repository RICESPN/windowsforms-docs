---
layout: post
title: How-to-Set-the-Number-of-Rows-or-Columns
description: how to set the number of rows or columns
platform: WindowsForms
control: Grid
documentation: ug
---

# How to Set the Number of Rows or Columns

## Introduction

Dynamically changing the RowCount or ColCount properties while a GridControl is being displayed is an efficient way to add or remove rows and/or columns from a GridControl. Using the designer, set grid’s RowCount and ColCount properties. From code, set these properties after the call to InitializeComponent in the form's constructor (or anytime later in your code after the GridControl has been created). 

### Example

{% highlight c# %}



public Form1()

{

        //

        //Requires for Windows Form Designer support.

        //

        InitializeComponent();



        //

        //TODO: Add any constructor code after InitializeComponent call.

        //



        //Sets the number of rows.             

        gridControl1.RowCount = 20;



        //Sets the number of columns.    

        gridControl1.ColCount = 200;

}


{% endhighlight  %}
{% highlight vbnet %}



  Public Sub New()

        MyBase.New()



'This call is required by the Windows Form Designer.

        InitializeComponent()



'Adds any initialization after the InitializeComponent() call.



'Sets the number of rows.             

        GridControl1.RowCount = 20 



'Sets the number of columns.    

        GridControl1.ColCount = 200 

    End Sub

{% endhighlight  %}

