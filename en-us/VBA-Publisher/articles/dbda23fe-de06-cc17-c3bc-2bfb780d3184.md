
# ThreeDFormat.Visible Property (Publisher)

 **Last modified:** July 28, 2015

 **In this article**
 [Syntax](#sectionSection0)
 [Remarks](#sectionSection1)
 [Example](#sectionSection2)


Returns or sets an  **MsoTriState** constant indicating whether the specified object or the formatting applied to the specified object is visible. Read/write.


## Syntax
<a name="sectionSection0"> </a>

 _expression_. **Visible**

 _expression_A variable that represents a  **ThreeDFormat** object.


## Remarks
<a name="sectionSection1"> </a>

The  **Visible** property value can be one of the **MsoTriState** constants declared in the Microsoft Office type library and shown in the following table.



|**Constant**|**Description**|
|:-----|:-----|
| **msoFalse**|The specified object or formatting is not visible.|
| **msoTriStateMixed**|Return value only. The specified shape range contains both objects with visible formatting and objects with invisible formatting.|
| **msoTriStateToggle**| Set value only. Switches the specified object between visible and invisble.|
| **msoTrue**|The specified object or formatting is visible.|

## Example
<a name="sectionSection2"> </a>

This example sets the horizontal and vertical offsets for the shadow of shape three on the first page in the active publication. The shadow is offset 5 points to the right of the shape and 3 points above it. If the shape does not already have a shadow, this example adds one to it.


```
With ActiveDocument.Pages(1).Shapes(3).Shadow 
 .Visible = msoTrue 
 .OffsetX = 5 
 .OffsetY = -3 
End With
```

