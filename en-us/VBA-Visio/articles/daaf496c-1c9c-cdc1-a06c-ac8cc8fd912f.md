
# Application.DocumentOpened Event (Visio)

 **Last modified:** July 28, 2015

 _**Applies to:** Visio 2013 Preview_

Occurs after a document is opened.


## Syntax

Private Sub  _expression__**DocumentOpened**( **_ByVal doc As [IVDOCUMENT]_**)

 _expression_A variable that represents an  **Application** object.


### Parameters



|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
|doc|Required| **[IVDOCUMENT]**|The document that was opened.|

## Remarks

The  **DocumentOpened** event is often added to the **EventList** collection of a Microsoft Visio template file (.vst). The event's action is triggered whenever an existing document is opened.

If you're using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own  **Event** objects, use the **Add** or **AddAdvise** method. To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. To create an **Event** object that receives notification, use the **AddAdvise** method. To find an event code for the event you want to create, see [Event codes](de8f5c7a-421d-ebcf-22b6-4310a202ef64.md).

You can add  **DocumentOpened** events to the **EventList** collection of an **Application** object, **Documents** collection, or **Document** object. The first two are straightforwardâ€”if a document is opened or created in the scope of the **Application** object or its **Documents** collection, the **DocumentOpened** event occurs.

However, adding a  **DocumentOpened** event to the **EventList** collection of a **Document** object makes sense only if the event's action is **visActCodeRunAddon**. In this case, the event is persistableâ€”it can be stored with the document. If the document that contains the persistent event is opened, its action is triggered. If a new document is based on or copied from the document that contains the persistent event, the  **DocumentOpened** event is copied to the new document and its action is triggered. However, if the event's action is **visActCodeAdvise**, that event is not persistable and therefore is not stored with the document; hence it is never triggered.

You can prevent code from running in response to the  **DocumentCreated**,  **DocumentOpened** or **DocumentAdded** event and all events from firing by setting the value of the **EventsEnabled** property of an **Application** object to **False**.

