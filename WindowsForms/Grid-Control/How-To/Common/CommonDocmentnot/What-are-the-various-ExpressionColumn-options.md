---
layout: post
title: What are the various ExpressionColumn options | Windows Forms | Syncfusion
description: What are the various ExpressionColumn options
platform: windowsforms
control: GridGrouping
documentation: ug
---

# What are the various ExpressionColumn options

The following code illustrates various expression column options.


 
{% highlight c# %}


//1. Sets the operators in the expression.

//The computations are performed with level one operations done first.

//Alpha constants used with match and like should be enclosed in apostrophes ('). 

// *, / ,+, - ,&lt;, &gt;, =, &lt;=, &gt;=,match, like, in, between ,or, and 

// * operator used here.

ExpressionFieldDescriptor exp= new ExpressionFieldDescriptor("Expr1","[ColumnName] *2", "System.Int32");



//2. Sets the output/view type.

//Output in double type.

ExpressionFieldDescriptor exp= new ExpressionFieldDescriptor("Expr1","[ColumnName] *2", "System.Double");


{% endhighlight  %}
{% highlight vb %}



' 1. Sets the operators in the expression. 

' Sets operators in the expression.  

' The computations are performed with level one operations done first.                      

' Alpha constants used with match and like should be enclosed in apostrophes ('). 

' *, / ,+, - ,&lt;, &gt;, =, &lt;=, &gt;=,match, like, in, between ,or, and 

' * operator used here.

Dim exp As ExpressionFieldDescriptor = New ExpressionFieldDescriptor("Expr1", "[Id] *2", "System.Int32")



' 2. Sets the output in double type.

Dim exp2 As ExpressionFieldDescriptor = New ExpressionFieldDescriptor("Expr2", "[Expr1] *2", "System.Double")

{% endhighlight  %}

