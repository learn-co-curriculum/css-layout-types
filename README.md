# CSS Layout Types

## Overview

This lesson will discuss sizing elements and the differences bewteen using pixels, ems, and percents.

## Objectives

1. Explore different CSS layout types.
2. Sizing elements using (px) pixel values.
2. Sizing elements using (em) em values.
3. Sizing elements using (%) percent values.
4. Sizing properties: width, min-width, max-width, height, min-height, max-height.

## Scaling Elements

<iframe width="640" height="480" src="https://www.youtube.com/embed/E9PFJLlJJ8Q?rel=0" frameborder="0" allowfullscreen></iframe>

*Note: Slides for this lecture video are provided in the resources at the bottom of this lesson.*

### Layout Types

Lets discuss the layout types: fixed (sometimes referred to as static), elastic, and fluid (sometimes referred to as liquid).

#### Fixed (px)

In a fixed (static) layout, elements are sized using pixels. One of the nice things about this is that our elements will be the same size on all screens. It is a measurement that is independent and uneffected by the size of the device we are viewing from. The only downside is if we create an element that is wider or taller than the device size we will see scrollbars, and the user will have to scroll to see the rest of the content that is out of view. Or, if the screen size is much larger than our element there may be substantial white space around the element. In other words we are not neccesarily ustilizing all of the screen space.

#### Elastic (em)

Elastic layouts size elements using (em) ems. An em is a typographic unit that describes a the size of a single character, typically the default is 1em = 16 px in size.

    “A pixel is an unscalable dot on a computer screen, whereas an em is a square of its font size. Because font sizes vary, the em is a relative unit that responds to users’ text-size preferences.” – Patrick Griffiths, A List Apart

One advatage of using ems to scale elements in a layout is that as a user scales the text up and down using their zoom settings it will also scale the elements set as ems. this way your text will always be in proportion to the container it is within. There are also some disadvantages such as, if a user scales elements that occupy the same space overlap is possible unless the developer invests a lot of time testing font sizes across many different device sizes and make s adjustments accordingly. 

#### Fluid (%)

Fluid (liquid) layouts 

#### Min/Max

...

## Summary

- ...

## Resources

- [Presentation Slides](https://docs.google.com/presentation/d/1UTUWDczUiDZ6byuhyHv0L3zJXQjdlnZheZXhRVLOL3Q/edit?usp=sharing)
- [Box Sizing - Code Example](http://jsfiddle.net/flatiron_school/99Tgm/)
- [MDN - CSS - Width](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
- [MDN - CSS - Min-Width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width)
- [MDN - CSS - Max-Width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width)
- [MDN - CSS - Height](https://developer.mozilla.org/en-US/docs/Web/CSS/height)
- [MDN - CSS - Min-Height](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)
- [MDN - CSS - Max-Height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)
- [Smashing Magazibe - Which Layout Is Right For You](https://www.smashingmagazine.com/2009/06/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/)

