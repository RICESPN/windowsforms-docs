---
layout: post
title: How to find the nearest port when mouse hover on the node | Diagram | Windows Forms | Syncfusion
description: This page explains about when mouse hover on the node, how to find the nearest port and establish the connection to the port.
platform: WindowsForms
control: Diagram
documentation: ug
---

# How to find the nearest ConnectionPoint when mouse hover on the node

By default, when hover over the Diagram nodes, the CentralPort will be highlighted and establish connection to the node. If you disabled the CentralPort, then highlight the ConnectionPoint (which is currently under in the mouse pointer) to establish the connection.

Now, you can customize the DiagramController class and override the GetConnectionPointAtPoint method to get the nearest ConnectionPoint to highlight and establish the connection in application. 

The following code example illustrates to highlight and establishing the connection with the nearest ConnectionPoint while hovering the node.

### Establish the connection with nearest ConnectionPoint

You should customize the DiagramController class in your application. Refer to the following code example for customizing the DiagramController class.
 
{% tabs %}

{% highlight c# %}
public class CustomController : DiagramController
{
private int hitpadding = 20;
public CustomController()
: base()
{

}

public CustomController(Syncfusion.Windows.Forms.Diagram.View view)
: base(view)
{

}
public override ConnectionPoint GetConnectionPointAtPoint(PointF ptSnapping)
{
ConnectionPoint port = base.GetConnectionPointAtPoint(ptSnapping);

NodeCollection nodes = this.Model.Nodes;
foreach (Node node in nodes)
{
if (!(node is ConnectorBase))
{
double lowdistance = 0;
int index = 0;
RectangleF nodeBounds = node.GetNodeBounds(false, true);
nodeBounds.Inflate(hitpadding, hitpadding);
if (nodeBounds.Contains(ptSnapping))
{
//to find the nearest port...
for (int i = 1; i < node.Ports.Count; i++)
{                            
ConnectionPoint port1 = node.Ports[i];
PointF portPos = port1.GetPosition();
portPos = node.ConvertToModelCoordinates(portPos);
//To find lowest distance of port from current point...
double dis = Geometry.PointDistance(ptSnapping, portPos);
if (dis < lowdistance || i == 1)
{
lowdistance = dis;
index = i;
}
}
return node.Ports[index];
}
}
}
return port;            
}
}
{% endhighlight %}

{% highlight vbnet %}
Public Class CustomController
Inherits DiagramController
Private hitpadding As Integer = 20
Public Sub New()
MyBase.New()

End Sub

Public Sub New(ByVal view As Syncfusion.Windows.Forms.Diagram.View)
MyBase.New(view)

End Sub

Public Overrides Function GetConnectionPointAtPoint(ByVal ptSnapping As PointF) As ConnectionPoint
Dim port As ConnectionPoint = MyBase.GetConnectionPointAtPoint(ptSnapping)

Dim nodes As NodeCollection = Me.Model.Nodes
For Each node As Node In nodes
If Not(TypeOf node Is ConnectorBase) Then
Dim lowdistance As Double = 0
Dim index As Integer = 0
Dim nodeBounds As RectangleF = node.GetNodeBounds(False, True)
nodeBounds.Inflate(hitpadding, hitpadding)
If nodeBounds.Contains(ptSnapping) Then
'to find the nearest port...
For i As Integer = 1 To node.Ports.Count - 1
Dim port1 As ConnectionPoint = node.Ports(i)
Dim portPos As PointF = port1.GetPosition()
portPos = node.ConvertToModelCoordinates(portPos)
'To find lowest distance of port from current point...
Dim dis As Double = Geometry.PointDistance(ptSnapping, portPos)
If dis < lowdistance OrElse i = 1 Then
lowdistance = dis
index = i
End If
Next i
Return node.Ports(index)
End If
End If
Next node
Return port
End Function

End Class
{% endhighlight %}

{% endtabs %}

