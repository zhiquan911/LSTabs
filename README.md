LSTabs
======

LSTabs for iOS is a small collection of well-documented classes that provides:

*   An easy way to apply a tint color to a UIButton. 
*   A base class to construct compound controls (such as colored buttons with badges or more complex components) and provides a common interface to bind the view to a data model
*   A base class to create static or scrollable collections of controls, add/remove items to the collection, animate the insertion or removal of items, receive notifications when an item changes its state
*   A basic interface to display the items of a collection in a vertical or horizontal layout

See the demo project for more details.


Available classes
======

*   <b>LSTintedButton</b>: a UIButton which is able to color its background image with a tint color. Separate tints can be applied to each button's state
*   <b>LSTabControl</b>: a UIControl subclass which basically aggregate a button with a badge view and bind it with a model class (LSTabItem)
*   <b>LSTabItem</b>: basic data model used to encapsulate informations about an LSTabControl subclass and receive delegate messages when something in the model is changed
*   <b>LSTabBarView</b>: view to manage a collection of LSTabControl items. Provides a basic interface to change the layout polices
*   <b>LSScrollTabBarView</b>: makes the previous class scrollable in horizontal direction. Other layout sample implementations are available in the demo project (see for examples the classes VerticalScrollTabBarView or TestVerticalScrollTabBarView)


Adding LSTabs to your project
======

Just drag and drop the required .h and .m files onto your project (make sure to select "Copy items into destination group's folder" when required).
You should only copy those files you plan to use in your project.


Requirements
======

LSTabs works from iOS 4.3 to the latest versions (the last tested version is 6.0.2).

<b>Works both with ARC and non-ARC projects.</b> (remember to add the "-fno-objc-arc" option to each .m files if your project is ARC).

It depends on the following Apple frameworks:
*   Foundation.framework
*   UIKit.framework
*   CoreGraphics.framework


Limitations
======

*   LSTabBarView currently is NOT able to handle contentMode = UIViewContentModeScaleToFill. It has to be implemented!
*   in LSScrollTabBarView the overflowLeft/overflowRight views handling needs to be completed and tested

