---
layout: post
title: GridDataBoundGrid | Windows Forms | Syncfusion
description: Learn about How to Change the Row Header to Display Line Numbers Instead of the Black Triangle in Griddataboundgrid in Windows Forms GridDataBoundGrid and more.
platform: windowsforms
control: DataBoundGrid
documentation: ug
---

# Grid data bound in WinForms GridDataBoundGrid(Classic)

You can achieve this by setting the row header base style to Header, and handling PrepareViewStyleInfo event handler to set the line numbers. Refer to the code snippet below, which illustrates this.

{% tabs %}
{% highlight c# %}

//In the Form Load.
private void Form1_Load(object sender, System.EventArgs e)
{
    this.gridDataBoundGrid1.DataSource = GetTable();
    this.gridDataBoundGrid1.BaseStylesMap["Row Header"].StyleInfo.CellType = "Header";
}

//GridPrepareViewStyleInfo.
private void grid_PrepareViewStyleInfo(object sender, GridPrepareViewStyleInfoEventArgs e)
{
    if (e.ColIndex == 0 && e.RowIndex > 0)
    {
        e.Style.Text = e.RowIndex.ToString();
        e.Style.Font.Bold = false;
    }
}

{% endhighlight %}

{% highlight vb %}

'In the Form Load.
Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) Handles MyBase.Load
Me.gridDataBoundGrid1.DataSource = GetTable()
Me.gridDataBoundGrid1.BaseStylesMap("Row Header").StyleInfo.CellType = "Header"
End Sub 'Form1_Load

'GridPrepareViewStyleInfo.
Private Sub gridDataBoundGrid1_PrepareViewStyleInfo(ByVal sender As Object, ByVal e As Syncfusion.Windows.Forms.Grid.GridPrepareViewStyleInfoEventArgs) Handles gridDataBoundGrid1.PrepareViewStyleInfo
If e.ColIndex = 0 AndAlso e.RowIndex > 0 Then
e.Style.Text = e.RowIndex.ToString()
e.Style.Font.Bold = False
End If
End Sub

{% endhighlight %}
{% endtabs %}
