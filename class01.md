# What I learned 

## Shay Howe's intro to RWD 

**Responsive Web Design**  is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

**Responsible Web Design** shold have the following :
- Flexible Layouts
- Flexible Grid
- Media Queries

* CSS3 introduced some new relative length units:
- vw:Viewports width
- vh: Viewports height
- vmin: Minimum of the viewport’s height and width 
- vmax: Maximum of the viewport’s height and width

______

### Media Queries 
1. Initializing Media Queries: we should link it in the HTML then in the CSS

2. Logical Operators in Media Queries:different logical operators available for use within media queries, including and, not, and only.

3. Media Features in Media Queries: Media features identify what attributes or properties will be targeted within the media query expression.

*Examples of the features*:
- Height & Width Media Features
- Orientation Media Feature
- Aspect Ratio Media Features
- Pixel Ratio Media Features
- Resolution Media Feature

4. Media Queries Demo:
- Mobile First : approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

**Mobile First Demo** 
The only exception here is that mobile devices only have to render only one CSS declaration. All of the other styles are deferred, only loading on larger viewports and done so without overwriting any initial styles.

* view port height and width : For the best results, and the best looking website, it is recommend that you use the device defaults by applying the device-height and device-width values.

* view port scale: To control how a website is scaled on a mobile device, and how users can continue to scale a website, use the minimum-scale, maximum-scale, initial-scale, and user-scalable properties.

* Viewport Resolution : Letting the browser decide how to scale a website based off any viewport scale values usually does the trick.

**CSS Viewport Rule** Currently some browsers have already implemented the @viewport rule, however support isn’t great across the board. The previously recommended viewport meta tag would look like the following @viewport rule in CSS.

5. Flexible Media: important aspect to responsive web design involves flexible media. As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

________

## All About Floats 

* **Float**  is a CSS positioning property. To understand its purpose and origin, we can look to print design. In a print layout, images may be set into the page such that text wraps around them as needed. This is commonly and appropriately called “text wrap”.

* What are floats used for?
*floats can be used to create entire web layouts.*


* **Clearing the Float** Float’s sister property is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. Again an illustration probably does more good than words do.

* **The Great Collapse**:One of the more bewildering things about working with floats is how they can affect the element that contains them (their “parent” element). If this parent element contained nothing but floated elements, the height of it would literally collapse to nothing. This isn’t always obvious if the parent doesn’t contain any visually noticeable background, but it is important to be aware of.We ***fix*** it by clearing the float after the floated elements in the container but before the close of the container.

* **Techniques for Clearing Floats**
1. The Empty Div Method 
2. The Overflow Method
3. The Easy Clearing Method

* **Problems with Floats**
1. Pushdown
2. Double Margin Bug 
3. 3px Jog 
4. Bottom Margin Bug

____________________

## SMACCS

**What is SMACCS :**

*(Scalable and Modular Architecture for CSS ) is a css methodology that designed by Jonathan Snook in 2011.*

*According to style guide of `SMACSS`, the Css Architecture should not build on 1 stylesheet. *

*It ought to has builded on 5 different categories. The goal of this process is creating flexible, consistent, reusable codes blocks, it prevents iteration of codes.*

>The categories are `base`, `layout`, `module`, `state` and `theme` .
______________________________

## Grids 

`DON'T OVERTHINK IT GRIDS`

**Grids are cool, grids are great**

Follow this Link to Codepen to see a good example about it [click-here](https://codepen.io/noele/pen/AjwuL)


