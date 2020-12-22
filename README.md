public class LinearLayout
extends ViewGroup

java.lang.Object
   ↳	android.view.View
 	   ↳	android.view.ViewGroup
 	 	   ↳	android.widget.LinearLayout
Known direct subclasses
ActionMenuView, NumberPicker, RadioGroup, SearchView, TabWidget, TableLayout, TableRow, ZoomControls

A layout that arranges other views either horizontally in a single column or vertically in a single row.

The following snippet shows how to include a linear layout in your layout XML file:




<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
   android:layout_width="match_parent"
   android:layout_height="match_parent"
   android:paddingLeft="16dp"
   android:paddingRight="16dp"
   android:orientation="horizontal"
   android:gravity="center">

   <!-- Include other widget or layout tags here. These are considered
           "child views" or "children" of the linear layout -->

 </LinearLayout>
 
 
 
Set android:orientation to specify whether child views are displayed in a row or column.

To control how linear layout aligns all the views it contains, set a value for android:gravity. For example, the snippet above sets android:gravity to "center". The value you set affects both horizontal and vertical alignment of all child views within the single row or column.

You can set android:layout_weight on individual child views to specify how linear layout divides remaining space amongst the views it contains. See the Linear Layout guide for an example.

See LinearLayout.LayoutParams to learn about other attributes you can set on a child view to affect its position and size in the containing linear layout.

Summary
Nested classes
class	LinearLayout.LayoutParams
Per-child layout information associated with ViewLinearLayout. 



XML attributes
android:baselineAligned	When set to false, prevents the layout from aligning its children's baselines. 
android:baselineAlignedChildIndex	When a linear layout is part of another layout that is baseline aligned, it can specify which of its children to baseline align to (that is, which child TextView). 
android:divider	Drawable to use as a vertical divider between buttons. 
android:gravity	Specifies how an object should position its content, on both the X and Y axes, within its own bounds. 
android:measureWithLargestChild	When set to true, all children with a weight will be considered having the minimum size of the largest child. 
android:orientation	Should the layout be a column or a row? Use "horizontal" for a row, "vertical" for a column. 
android:weightSum	Defines the maximum weight sum. 
Inherited XML attributes
From class android.view.ViewGroup
From class android.view.View


Constants
int	HORIZONTAL
int	SHOW_DIVIDER_BEGINNING
Show a divider at the beginning of the group.

int	SHOW_DIVIDER_END
Show a divider at the end of the group.

int	SHOW_DIVIDER_MIDDLE
Show dividers between each item in the group.

int	SHOW_DIVIDER_NONE
Don't show any dividers.

int	VERTICAL
Inherited constants
From class android.view.ViewGroup
From class android.view.View
Inherited fields
From class android.view.View
Public constructors
LinearLayout(Context context)
LinearLayout(Context context, AttributeSet attrs)
LinearLayout(Context context, AttributeSet attrs, int defStyleAttr)
LinearLayout(Context context, AttributeSet attrs, int defStyleAttr, int defStyleRes)
Public methods
LinearLayout.LayoutParams	generateLayoutParams(AttributeSet attrs)
Returns a new set of layout parameters based on the supplied attributes set.

CharSequence	getAccessibilityClassName()
Return the class name of this object to be used for accessibility purposes.

int	getBaseline()
Return the offset of the widget's text baseline from the widget's top boundary.

int	getBaselineAlignedChildIndex()
Drawable	getDividerDrawable()
int	getDividerPadding()
Get the padding size used to inset dividers in pixels

int	getGravity()
Returns the current gravity.

int	getOrientation()
Returns the current orientation.

int	getShowDividers()
float	getWeightSum()
Returns the desired weights sum.

boolean	isBaselineAligned()
Indicates whether widgets contained within this layout are aligned on their baseline or not.

boolean	isMeasureWithLargestChildEnabled()
When true, all children with a weight will be considered having the minimum size of the largest child.

void	onRtlPropertiesChanged(int layoutDirection)
Called when any RTL property (layout direction or text direction or text alignment) has been changed.

void	setBaselineAligned(boolean baselineAligned)
Defines whether widgets contained in this layout are baseline-aligned or not.

void	setBaselineAlignedChildIndex(int i)
void	setDividerDrawable(Drawable divider)
Set a drawable to be used as a divider between items.

void	setDividerPadding(int padding)
Set padding displayed on both ends of dividers.

void	setGravity(int gravity)
Describes how the child views are positioned.

void	setHorizontalGravity(int horizontalGravity)
void	setMeasureWithLargestChildEnabled(boolean enabled)
When set to true, all children with a weight will be considered having the minimum size of the largest child.

void	setOrientation(int orientation)
Should the layout be a column or a row.

void	setShowDividers(int showDividers)
Set how dividers should be shown between items in this layout

void	setVerticalGravity(int verticalGravity)
void	setWeightSum(float weightSum)
Defines the desired weights sum.

boolean	shouldDelayChildPressedState()
Return true if the pressed state should be delayed for children or descendants of this ViewGroup.

Protected methods
boolean	checkLayoutParams(ViewGroup.LayoutParams p)
LinearLayout.LayoutParams	generateDefaultLayoutParams()
Returns a set of layout parameters with a width of ViewGroup.LayoutParams.MATCH_PARENT and a height of ViewGroup.LayoutParams.WRAP_CONTENT when the layout's orientation is VERTICAL.

LinearLayout.LayoutParams	generateLayoutParams(ViewGroup.LayoutParams lp)
Returns a safe set of layout parameters based on the supplied layout params.

void	onDraw(Canvas canvas)
Implement this to do your drawing.

void	onLayout(boolean changed, int l, int t, int r, int b)
Called from layout when this view should assign a size and position to each of its children.

void	onMeasure(int widthMeasureSpec, int heightMeasureSpec)
Measure the view and its content to determine the measured width and the measured height.

Inherited methods
From class android.view.ViewGroup
From class android.view.View
From class java.lang.Object
From interface android.view.ViewParent
From interface android.view.ViewManager
From interface android.graphics.drawable.Drawable.Callback
From interface android.view.KeyEvent.Callback
From interface android.view.accessibility.AccessibilityEventSource
XML attributes
android:baselineAligned
When set to false, prevents the layout from aligning its children's baselines. This attribute is particularly useful when the children use different values for gravity. The default value is true.

May be a boolean value, such as "true" or "false".

Related methods:

setBaselineAligned(boolean)
android:baselineAlignedChildIndex
When a linear layout is part of another layout that is baseline aligned, it can specify which of its children to baseline align to (that is, which child TextView).

May be an integer value, such as "100".

Related methods:

setBaselineAlignedChildIndex(int)
android:divider
Drawable to use as a vertical divider between buttons.

May be a reference to another resource, in the form "@[+][package:]type/name" or a theme attribute in the form "?[package:]type/name".

May be a color value, in the form of "#rgb", "#argb", "#rrggbb", or "#aarrggbb".

Related methods:

setDividerDrawable(Drawable)
android:gravity
Specifies how an object should position its content, on both the X and Y axes, within its own bounds.

Must be one or more (separated by '|') of the following constant values.

Constant	Value	Description
bottom	50	Push object to the bottom of its container, not changing its size.
center	11	Place the object in the center of its container in both the vertical and horizontal axis, not changing its size.
center_horizontal	1	Place object in the horizontal center of its container, not changing its size.
center_vertical	10	Place object in the vertical center of its container, not changing its size.
clip_horizontal	8	Additional option that can be set to have the left and/or right edges of the child clipped to its container's bounds. The clip will be based on the horizontal gravity: a left gravity will clip the right edge, a right gravity will clip the left edge, and neither will clip both edges.
clip_vertical	80	Additional option that can be set to have the top and/or bottom edges of the child clipped to its container's bounds. The clip will be based on the vertical gravity: a top gravity will clip the bottom edge, a bottom gravity will clip the top edge, and neither will clip both edges.
end	800005	Push object to the end of its container, not changing its size.
fill	77	Grow the horizontal and vertical size of the object if needed so it completely fills its container.
fill_horizontal	7	Grow the horizontal size of the object if needed so it completely fills its container.
fill_vertical	70	Grow the vertical size of the object if needed so it completely fills its container.
left	3	Push object to the left of its container, not changing its size.
right	5	Push object to the right of its container, not changing its size.
start	800003	Push object to the beginning of its container, not changing its size.
top	30	Push object to the top of its container, not changing its size.
Related methods:

setGravity(int)
android:measureWithLargestChild
When set to true, all children with a weight will be considered having the minimum size of the largest child. If false, all children are measured normally.

May be a boolean value, such as "true" or "false".

Related methods:

setMeasureWithLargestChildEnabled(boolean)
android:orientation
Should the layout be a column or a row? Use "horizontal" for a row, "vertical" for a column. The default is horizontal.

Must be one of the following constant values.

Constant	Value	Description
horizontal	0	Defines an horizontal widget.
vertical	1	Defines a vertical widget.
Related methods:

setOrientation(int)
android:weightSum
Defines the maximum weight sum. If unspecified, the sum is computed by adding the layout_weight of all of the children. This can be used for instance to give a single child 50% of the total available space by giving it a layout_weight of 0.5 and setting the weightSum to 1.0.

May be a floating point value, such as "1.2".

Constants
HORIZONTAL
Added in API level 1

public static final int HORIZONTAL
Constant Value: 0 (0x00000000)

SHOW_DIVIDER_BEGINNING
Added in API level 11

public static final int SHOW_DIVIDER_BEGINNING
Show a divider at the beginning of the group.

Constant Value: 1 (0x00000001)

SHOW_DIVIDER_END
Added in API level 11

public static final int SHOW_DIVIDER_END
Show a divider at the end of the group.

Constant Value: 4 (0x00000004)

SHOW_DIVIDER_MIDDLE
Added in API level 11

public static final int SHOW_DIVIDER_MIDDLE
Show dividers between each item in the group.

Constant Value: 2 (0x00000002)

SHOW_DIVIDER_NONE
Added in API level 11

public static final int SHOW_DIVIDER_NONE
Don't show any dividers.

Constant Value: 0 (0x00000000)

VERTICAL
Added in API level 1

public static final int VERTICAL
Constant Value: 1 (0x00000001)

Public constructors
LinearLayout
Added in API level 1

public LinearLayout (Context context)
Parameters
context	Context
LinearLayout
Added in API level 1

public LinearLayout (Context context, 
                AttributeSet attrs)
Parameters
context	Context
attrs	AttributeSet: This value may be null.
LinearLayout
Added in API level 11

public LinearLayout (Context context, 
                AttributeSet attrs, 
                int defStyleAttr)
Parameters
context	Context
attrs	AttributeSet: This value may be null.
defStyleAttr	int
LinearLayout
Added in API level 21

public LinearLayout (Context context, 
                AttributeSet attrs, 
                int defStyleAttr, 
                int defStyleRes)
Parameters
context	Context
attrs	AttributeSet
defStyleAttr	int
defStyleRes	int
Public methods
generateLayoutParams
Added in API level 1

public LinearLayout.LayoutParams generateLayoutParams (AttributeSet attrs)
Returns a new set of layout parameters based on the supplied attributes set.

Parameters
attrs	AttributeSet: the attributes to build the layout parameters from
Returns
LinearLayout.LayoutParams	an instance of ViewGroup.LayoutParams or one of its descendants
getAccessibilityClassName
Added in API level 23

public CharSequence getAccessibilityClassName ()
Return the class name of this object to be used for accessibility purposes. Subclasses should only override this if they are implementing something that should be seen as a completely new class of view when used by accessibility, unrelated to the class it is deriving from. This is used to fill in AccessibilityNodeInfo#setClassName.

Returns
CharSequence	
getBaseline
Added in API level 1

public int getBaseline ()
Return the offset of the widget's text baseline from the widget's top boundary. If this widget does not support baseline alignment, this method returns -1.

Returns
int	the offset of the baseline within the widget's bounds or -1 if baseline alignment is not supported
getBaselineAlignedChildIndex
Added in API level 1

public int getBaselineAlignedChildIndex ()
Returns
int	The index of the child that will be used if this layout is part of a larger layout that is baseline aligned, or -1 if none has been set.
getDividerDrawable
Added in API level 16

public Drawable getDividerDrawable ()
Related XML Attributes:

android:divider
Returns
Drawable	the divider Drawable that will divide each item.
See also:

setDividerDrawable(Drawable)
getDividerPadding
Added in API level 14

public int getDividerPadding ()
Get the padding size used to inset dividers in pixels

Returns
int	
See also:

setShowDividers(int)
setDividerDrawable(Drawable)
setDividerPadding(int)
getGravity
Added in API level 24

public int getGravity ()
Returns the current gravity. See Gravity

Returns
int	the current gravity.
See also:

setGravity(int)
getOrientation
Added in API level 1

public int getOrientation ()
Returns the current orientation.

Returns
int	either HORIZONTAL or VERTICAL Value is HORIZONTAL, or VERTICAL
getShowDividers
Added in API level 11

public int getShowDividers ()
Returns
int	A flag set indicating how dividers should be shown around items. Value is either 0 or a combination of SHOW_DIVIDER_NONE, SHOW_DIVIDER_BEGINNING, SHOW_DIVIDER_MIDDLE, and SHOW_DIVIDER_END
See also:

setShowDividers(int)
getWeightSum
Added in API level 1

public float getWeightSum ()
Returns the desired weights sum.

Returns
float	A number greater than 0.0f if the weight sum is defined, or a number lower than or equals to 0.0f if not weight sum is to be used.
isBaselineAligned
Added in API level 1

public boolean isBaselineAligned ()
Indicates whether widgets contained within this layout are aligned on their baseline or not.

Returns
boolean	true when widgets are baseline-aligned, false otherwise
isMeasureWithLargestChildEnabled
Added in API level 11

public boolean isMeasureWithLargestChildEnabled ()
When true, all children with a weight will be considered having the minimum size of the largest child. If false, all children are measured normally.

Related XML Attributes:

android:measureWithLargestChild
Returns
boolean	True to measure children with a weight using the minimum size of the largest child, false otherwise.
onRtlPropertiesChanged
Added in API level 17

public void onRtlPropertiesChanged (int layoutDirection)
Called when any RTL property (layout direction or text direction or text alignment) has been changed. Subclasses need to override this method to take care of cached information that depends on the resolved layout direction, or to inform child views that inherit their layout direction. The default implementation does nothing.

Parameters
layoutDirection	int: Value is View.LAYOUT_DIRECTION_LTR, or View.LAYOUT_DIRECTION_RTL
setBaselineAligned
Added in API level 1

public void setBaselineAligned (boolean baselineAligned)
Defines whether widgets contained in this layout are baseline-aligned or not.

Related XML Attributes:

android:baselineAligned
Parameters
baselineAligned	boolean: true to align widgets on their baseline, false otherwise
setBaselineAlignedChildIndex
Added in API level 1

public void setBaselineAlignedChildIndex (int i)
Related XML Attributes:

android:baselineAlignedChildIndex
Parameters
i	int: The index of the child that will be used if this layout is part of a larger layout that is baseline aligned.
setDividerDrawable
Added in API level 11

public void setDividerDrawable (Drawable divider)
Set a drawable to be used as a divider between items.

Related XML Attributes:

android:divider
Parameters
divider	Drawable: Drawable that will divide each item.
See also:

setShowDividers(int)
setDividerPadding
Added in API level 14

public void setDividerPadding (int padding)
Set padding displayed on both ends of dividers. For a vertical layout, the padding is applied to left and right end of dividers. For a horizontal layout, the padding is applied to top and bottom end of dividers.

Parameters
padding	int: Padding value in pixels that will be applied to each end
See also:

setShowDividers(int)
setDividerDrawable(Drawable)
getDividerPadding()
setGravity
Added in API level 1

public void setGravity (int gravity)
Describes how the child views are positioned. Defaults to GRAVITY_TOP. If this layout has a VERTICAL orientation, this controls where all the child views are placed if there is extra vertical space. If this layout has a HORIZONTAL orientation, this controls the alignment of the children.

Related XML Attributes:

android:gravity
Parameters
gravity	int: See Gravity
setHorizontalGravity
Added in API level 1

public void setHorizontalGravity (int horizontalGravity)
Parameters
horizontalGravity	int
setMeasureWithLargestChildEnabled
Added in API level 11

public void setMeasureWithLargestChildEnabled (boolean enabled)
When set to true, all children with a weight will be considered having the minimum size of the largest child. If false, all children are measured normally. Disabled by default.

Related XML Attributes:

android:measureWithLargestChild
Parameters
enabled	boolean: True to measure children with a weight using the minimum size of the largest child, false otherwise.
setOrientation
Added in API level 1

public void setOrientation (int orientation)
Should the layout be a column or a row.

Related XML Attributes:

android:orientation
Parameters
orientation	int: Pass HORIZONTAL or VERTICAL. Default value is HORIZONTAL. Value is HORIZONTAL, or VERTICAL
setShowDividers
Added in API level 11

public void setShowDividers (int showDividers)
Set how dividers should be shown between items in this layout

Parameters
showDividers	int: One or more of SHOW_DIVIDER_BEGINNING, SHOW_DIVIDER_MIDDLE, or SHOW_DIVIDER_END to show dividers, or SHOW_DIVIDER_NONE to show no dividers. Value is either 0 or a combination of SHOW_DIVIDER_NONE, SHOW_DIVIDER_BEGINNING, SHOW_DIVIDER_MIDDLE, and SHOW_DIVIDER_END
setVerticalGravity
Added in API level 1

public void setVerticalGravity (int verticalGravity)
Parameters
verticalGravity	int
setWeightSum
Added in API level 1

public void setWeightSum (float weightSum)
Defines the desired weights sum. If unspecified the weights sum is computed at layout time by adding the layout_weight of each child. This can be used for instance to give a single child 50% of the total available space by giving it a layout_weight of 0.5 and setting the weightSum to 1.0.

Parameters
weightSum	float: a number greater than 0.0f, or a number lower than or equals to 0.0f if the weight sum should be computed from the children's layout_weight
shouldDelayChildPressedState
Added in API level 14

public boolean shouldDelayChildPressedState ()
Return true if the pressed state should be delayed for children or descendants of this ViewGroup. Generally, this should be done for containers that can scroll, such as a List. This prevents the pressed state from appearing when the user is actually trying to scroll the content. The default implementation returns true for compatibility reasons. Subclasses that do not scroll should generally override this method and return false.

Returns
boolean	
Protected methods
checkLayoutParams
Added in API level 1

protected boolean checkLayoutParams (ViewGroup.LayoutParams p)
Parameters
p	ViewGroup.LayoutParams
Returns
boolean	
generateDefaultLayoutParams
Added in API level 1

protected LinearLayout.LayoutParams generateDefaultLayoutParams ()
Returns a set of layout parameters with a width of ViewGroup.LayoutParams.MATCH_PARENT and a height of ViewGroup.LayoutParams.WRAP_CONTENT when the layout's orientation is VERTICAL. When the orientation is HORIZONTAL, the width is set to LayoutParams#WRAP_CONTENT and the height to LayoutParams#WRAP_CONTENT.

Returns
LinearLayout.LayoutParams	a set of default layout parameters or null
generateLayoutParams
Added in API level 1

protected LinearLayout.LayoutParams generateLayoutParams (ViewGroup.LayoutParams lp)
Returns a safe set of layout parameters based on the supplied layout params. When a ViewGroup is passed a View whose layout params do not pass the test of checkLayoutParams(android.view.ViewGroup.LayoutParams), this method is invoked. This method should return a new set of layout params suitable for this ViewGroup, possibly by copying the appropriate attributes from the specified set of layout params.

Parameters
lp	ViewGroup.LayoutParams: The layout parameters to convert into a suitable set of layout parameters for this ViewGroup.
Returns
LinearLayout.LayoutParams	an instance of ViewGroup.LayoutParams or one of its descendants
onDraw
Added in API level 1

protected void onDraw (Canvas canvas)
Implement this to do your drawing.

Parameters
canvas	Canvas: the canvas on which the background will be drawn
onLayout
Added in API level 1

protected void onLayout (boolean changed, 
                int l, 
                int t, 
                int r, 
                int b)
Called from layout when this view should assign a size and position to each of its children. Derived classes with children should override this method and call layout on each of their children.

Parameters
changed	boolean: This is a new size or position for this view
l	int: Left position, relative to parent
t	int: Top position, relative to parent
r	int: Right position, relative to parent
b	int: Bottom position, relative to parent
onMeasure
Added in API level 1

protected void onMeasure (int widthMeasureSpec, 
                int heightMeasureSpec)
Measure the view and its content to determine the measured width and the measured height. This method is invoked by measure(int, int) and should be overridden by subclasses to provide accurate and efficient measurement of their contents.

CONTRACT: When overriding this method, you must call setMeasuredDimension(int, int) to store the measured width and height of this view. Failure to do so will trigger an IllegalStateException, thrown by measure(int, int). Calling the superclass' onMeasure(int, int) is a valid use.

The base class implementation of measure defaults to the background size, unless a larger size is allowed by the MeasureSpec. Subclasses should override onMeasure(int, int) to provide better measurements of their content.

If this method is overridden, it is the subclass's responsibility to make sure the measured height and width are at least the view's minimum height and width (getSuggestedMinimumHeight() and getSuggestedMinimumWidth()).

Parameters
widthMeasureSpec	int: horizontal space requirements as imposed by the parent. The requirements are encoded with View.MeasureSpec.
heightMeasureSpec	int: vertical space requirements as imposed by the parent. The requirements are encoded with View.MeasureSpec.
