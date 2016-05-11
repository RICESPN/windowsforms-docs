---
layout: post
title: How to implement AutoComplete with RichTextBox control | WindowsForms | Syncfusion
description: How to implement AutoComplete with RichTextBox control
platform: WindowsForms
control: Editors Package
documentation: ug
---




# How to implement AutoComplete with RichTextBox control?

Follow the given steps to implement AutoComplete feature with RichTextBox control.

1. Implement the IEditControlsEmbed interface in a RichTextBox class that enables the AutoComplete functionality for the RichTextBox control.

   ~~~ cs



		public class MyRichTextBox : System.Windows.Forms.RichTextBox, IEditControlsEmbed

		{

			  // Returns the active RichTextBox control.

			   public Control GetActiveEditControl(IEditControlsEmbedListener listener)

			   {

						  return (Control)this;

			   }



		}

   ~~~
   {:.prettyprint }

   ~~~ vbnet



		Public Class MyRichTextBox Inherits System.Windows.Forms.RichTextBox Implements IEditControlsEmbed



		' Returns the active RichTextBox control.



		Public Function GetActiveEditControl(ByVal listener As IEditControlsEmbedListener) As Control



			Return CType(Me, Control)



		End Function



		End Class

   ~~~
   {:.prettyprint }


2. Drag and drop the RichTextBox control and the AutoComplete control to a form.

   ~~~ cs



		// Initialization

		Syncfusion.Windows.Forms.Tools.AutoComplete autoComplete1= new Syncfusion.Windows.Forms.Tools.AutoComplete();;

		MyRichTextBox richTextBox1= new MyRichTextBox();

   ~~~
   {:.prettyprint }

   ~~~ vbnet



		' Initialization

		Dim autoComplete1 As Syncfusion.Windows.Forms.Tools.AutoComplete = New Syncfusion.Windows.Forms.Tools.AutoComplete 
		Dim richTextBox1 As MyRichTextBox = New MyRichTextBox

   ~~~
   {:.prettyprint }

3. The AutoComplete control can take an external data source, any data source that implements IList or IListSource, for its history list. Set here is a StringCollection as the DataSource.
4. When this property is set, the AutoComplete control initializes itself with the data source and use that as the basis for its matching routines. For example, when you have a DataSet with a list of names of the states in the US and you specify that as the DataSource, then the AutoComplete control displays all the matches from within these names when you type in the target edit control.

   ~~~ cs



		// Sets the DataSource.

		StringCollection liste = new StringCollection();

			liste.Add("New Jersey");

			liste.Add("North Carolina");

			liste.Add("North Dakota");

			liste.Add("New York");

			liste.Add("New Mexico");

			autoComplete1.DataSource = liste;

   ~~~
   {:.prettyprint }

   ~~~ vbnet

		' Sets the DataSource. 

		Dim liste As StringCollection = New StringCollection 
				liste.Add("New Jersey") 
				liste.Add("North Carolina") 
				liste.Add("North Dakota") 
				liste.Add("New York") 
				liste.Add("New Mexico") 
				autoComplete1.DataSource = liste

   ~~~
   {:.prettyprint }

5. Set the AutoCompleteonautoComplete1 property in the properties page to either AutoSuggest, AutoAppend or both. 
6. SetAutoComplete is the extended property for the AutoComplete property, that is called by the Framework when the AutoComplete property is set on any control. When using the AutoComplete control programmatically, you can use this method to add and remove auto completion for the RichTextBox control.

   ~~~ cs



		this.autoComplete1.SetAutoComplete(this.richTextBox1,Syncfusion.Windows.Forms.Tools.AutoCompleteModes.AutoSuggest);

   ~~~
   {:.prettyprint }

   ~~~ vbnet



		Me.autoComplete1.SetAutoComplete(Me.richTextBox1,Syncfusion.Windows.Forms.Tools.AutoCompleteModes.AutoSuggest)

   ~~~
   {:.prettyprint }

7. The RichTextBox is enabled with the AutoComplete functionality.