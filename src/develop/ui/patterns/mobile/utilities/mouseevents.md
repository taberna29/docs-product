---
tags: runtime-mobileandreactiveweb;  
summary: The Mouse Events UI Pattern enables click events on a specific widget or pattern.
---

# Mouse Events

You can use the Mouse Events UI Pattern when the user needs to select elements on the interface with high precision.

![](images/mouseevents-1-ss.png)

The following example shows how you can use the Touch Events UI pattern to display the distance the mouse is dragged left and right across the screen.

1. In Service Studio, in the Toolbox, search for `Mouse Events`.

    The Touch events widget is displayed.

    ![](images/mouseevents-2-ss.png)

1. From the Toolbox, drag the Touch Events widget into the Main Content area of your application's screen.

    ![](images/mouseevents-3-ss.png)

1. From the Toolbox, drag the Center Content widget into the Main Content area of your screen.
 
    ![](images/touchevents-3-ss.png)

1. On the **Properties** tab, enter a name in the **Name** property. In this example, we enter `card`.

    ![](images/touchevents-4-ss.png)

1. Add 2 local variables by right-clicking on your screen name and selecting **Add Local Variable**.

    In this example we call name them **Drag** and **Distance**. Both local variables are of data type text.

    ![](images/touchevents-5-ss.png)

1. Add the relevant content to the Center Content widget placeholders. 

    In this example, we add text and 2 expressions to the Center placeholder, and text to the Bottom placeholder. 

   ![](images/touchevents-6-ss.png)

   Each of the expressions are set to the local variables respectively (**Drag** and **Distance**). 

   ![](images/touchevents-7-ss.png)

1. Add a client action by right-clicking your screen name and selecting **Add Client Action**. 

1. Enter a name for the client action. In this example, we enter `MouseEventsMove`.

   ![](images/touchevents-8-ss.png)

1. Add 2 input parameters by right-clicking the client action and selecting **Add Input Parameter**.

    In this example, we add the **OffsetX** and **OffsetY** input parameters and set their data type to decimal.

    ![](images/touchevents-9-ss.png)

1. Add the relevant logic to the client action. In this example, we add the following:

    ![](images/touchevents-10-ss.png)

1. Select the Mouse Events widget and set the **WidgetId**, **PreventDefaults**, and the **Handler** properties. 

    ![](images/touchevents-11-ss.png)

    The **WidgetId** is set to **card.Id**, the **PreventDefaults** to **False**, **OfFsetX** to **OffsetX**, and **OffsetY** to **OffsetY**.

After following these steps and publishing the module, you can test the pattern in your app.

## Properties

| Property | Description |
|---|---|
| IsHorizontal (Boolean): Optional | If True, content is displayed horizontally. This is the default. If False, the content is displayed vertically. |
| ExtendedClass (Text): Optional  | <p>Add custom style classes to the Align Center UI Pattern. You define your [custom style classes](../../../look-feel/css.md) in your application using CSS.</p> <p>Examples <ul><li>_Blank_ - No custom styles are added (default value).</li><li>_"myclass"_ - Adds the _myclass_ style to the Align Center UI styles being applied.</li><li>_"myclass1" "myclass2"_ - Adds the _myclass1_ and _myclass2_ styles to the Align Center UI styles being applied.</li></ul></p> |