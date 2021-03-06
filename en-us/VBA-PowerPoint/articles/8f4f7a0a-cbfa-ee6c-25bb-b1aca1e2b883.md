
# LineFormat.EndArrowheadStyle Property (PowerPoint)

 **Last modified:** July 28, 2015

 **In this article**
 [Syntax](#sectionSection0)
 [Remarks](#sectionSection1)
 [Example](#sectionSection2)


Returns or sets the style of the arrowhead at the end of the specified line. Read/write.


## Syntax
<a name="sectionSection0"> </a>

 _expression_. **EndArrowheadStyle**

 _expression_A variable that represents an  **LineFormat** object.


### Return Value

MsoArrowheadStyle


## Remarks
<a name="sectionSection1"> </a>

The  **EndArrowheadStyle** proerty value can be one of these **MsoArrowheadStyle** constants.



| **msoArrowheadDiamond**|
| **msoArrowheadNone**|
| **msoArrowheadOpen**|
| **msoArrowheadOval**|
| **msoArrowheadStealth**|
| **msoArrowheadStyleMixed**|
| **msoArrowheadTriangle**|

## Example
<a name="sectionSection2"> </a>

This example adds a line to  `myDocument`. There's a short, narrow oval on the line's starting point and a long, wide triangle on its endpoint.


```
Set myDocument = ActivePresentation.Slides(1)

With myDocument.Shapes.AddLine(100, 100, 200, 300).Line

    .BeginArrowheadLength = msoArrowheadShort

    .BeginArrowheadStyle = msoArrowheadOval

    .BeginArrowheadWidth = msoArrowheadNarrow

    .EndArrowheadLength = msoArrowheadLong

    .EndArrowheadStyle = msoArrowheadTriangle

    .EndArrowheadWidth = msoArrowheadWide

End With
```


## See also
<a name="sectionSection2"> </a>


#### Concepts


 [LineFormat Object](11c955d5-bbda-d99f-cec9-fc6187450a12.md)
#### Other resources


 [LineFormat Object Members](71884432-fcec-8163-ff00-0854d9ae0bb8.md)
