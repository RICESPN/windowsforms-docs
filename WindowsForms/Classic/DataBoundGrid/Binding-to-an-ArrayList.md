---
layout: post
title: Binding-to-an-ArrayList | Windows Forms | Syncfusion
description: binding to an arraylist
platform: windowsforms
control: DataBoundGrid
documentation: ug
---

# Binding to an ArrayList

You can bind an ArrayList that holds objects with public properties. Given below is an example, which substantiates this point.

1. We first define an object called Person with two public properties: FirstName and LastName.
2. We then create an ArrayList holding a collection of these objects.
3. To bind this ArrayList to Grid Data Bound Grid, we set the grid's DataSource property after dropping Grid Data Bound Grid onto the form.

Given below is the code sample for this.

{% tabs %}
{% highlight c# %}

//Creates the Person object class.

public class Person
{
    private string lastName;
    private string firstName;

    public Person(string firstName, string lastName)
    {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    public string FirstName
    {
        get{return firstName;}
        set{firstName = value;}
    }

    public string LastName
    {
        get{return lastName;}
        set{lastName = value;}
    }
}

//Code within your Form Load event handler.

private void Form1_Load(object sender, System.EventArgs e)
{
    ArrayList al = new ArrayList();
    al.Add(new Person("John", "Smith"));
    al.Add(new Person("Mary", "Tucker"));
    al.Add(new Person("Sue", "Gaskins"));
    al.Add(new Person("John", "Jacobs"));
    al.Add(new Person("Sam", "Garfunkel"));
    al.Add(new Person("George", "Shepherd"));
    al.Add(new Person("Becky", "Dunsford"));
    this.gridDataBoundGrid1.DataSource = al;
}
{% endhighlight  %}
{% highlight vb %}
'Creates the Person object class.

Public Class Person
Private firstName As String
Private lastName As String

Public Sub New(ByVal firstName As String, ByVal lastName As String)
Me.firstName = firstName
Me.lastName = lastName
End Sub

Public Property LastName()
Get
Return lastName
End Get
Set(ByVal Value)
lastName = Value
End Set
End Property

Public Property FirstName()
Get
Return firstName
End Get
Set(ByVal Value)
firstName = Value
End Set
End Property
End Class

'Code within your Form Load event handler.

Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
Dim al As ArrayList = New ArrayList()
al.Add(New Person("John", "Smith"))
al.Add(New Person("Mary", "Tucker"))
al.Add(New Person("Sue", "Gaskins"))
al.Add(New Person("John", "Jacobs"))
al.Add(New Person("Sam", "Garfunkel"))
al.Add(New Person("George", "Shepherd"))
al.Add(New Person("Becky", "Dunsford"))
Me.GridDataBoundGrid1.DataSource = al
End Sub
{% endhighlight  %}
{% endtabs %} 

N> Download sample demo from [here](https://www.syncfusion.com/downloads/support/directtrac/general/ze/ArrayListBinding854674391).

## ArrayList Class with IBindingList Support

Any change that you make to the grid will be posted back to the ArrayList. Keep in mind that you cannot add new items to the ArrayList through the grid. Instead, make sure that your data source supports the IBindingList interface and that it implements an appropriate AddNew method. The IBindingList support determines whether you can add new items and sort items as well as do searching for other basic aspects of list behavior. 

![](Binding-to-an-ArrayList_images/Binding-to-an-ArrayList_img1.jpeg) 



Here is a minimal implementation of an ArrayList-derived class that also supports IBindingList. If you add this class to the above code and in the Form-Load change the ArrayList to PersonList, then you will be able to add new entries to your underlying PersonList data source by using the AppendRow at the bottom of the grid. Notice that the implementation of IBindingList.AddNew as well as the IBindingList.AllowNew property will indicate that new rows are allowed.

