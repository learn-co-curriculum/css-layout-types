# CSS Layout Types

## Learning Goals

- Use CSS layout types: Fixed, Elastic, and Fluid
- Set sizing properties: width, min-width, max-width, height, min-height, and max-height
- Set sizing elements using (px) pixel values
- Set sizing elements using (em) em values
- Set sizing elements using (%) percent values
- Use the overflow property
- Create fluid heights

## Introduction

This lesson will discuss sizing elements and the differences between using
pixels, ems, percents, and the overflow property.

Make sure to check out the code examples in the Resources section to see how
these properties work!

### Layout Types

Let's discuss CSS layout types: fixed (sometimes referred to as static),
elastic, and fluid (sometimes referred to as liquid).

#### Fixed (px)

In a fixed (static) layout, elements are sized using pixels. One of the nice
things about this is that our elements will be the same size on all screens. It
is a measurement that is independent and unaffected by the size of the device we
are viewing from. The only downside is if we create an element that is wider or
taller than the device size we will see scroll bars, and the user will have to
scroll to see the rest of the content that is out of view. Or, if the screen
size is much larger than our element there may be substantial white space around
the element. In other words we are not necessarily utilizing all of the screen
space.

#### Elastic (em)

Elastic layouts size elements using (em) ems. An em is a typographic unit that
describes a the size of a single character, typically the default is 1em = 16 px
in size.

> “A pixel is an unscalable dot on a computer screen, whereas an em is a square
> of its font size. Because font sizes vary, the em is a relative unit that
> responds to users’ text-size preferences.” – Patrick Griffiths, A List Apart

One advantage of using ems to scale elements in a layout is that as a user
scales the text up and down using their zoom settings it will also scale the
elements set as ems. this way your text will always be in proportion to the
container it is within. There are also some disadvantages such as, if a user
scales elements that occupy the same space overlap is possible unless the
developer invests a lot of time testing font sizes across many different device
sizes and make s adjustments accordingly.

#### Fluid (%)

Fluid (liquid) layouts size elements using (%) percents. This allows for a
layout that will stretch and expand or contract to the size of the users
device. This allows developers to make use of the entirety of space on the
screen. Also your users will never see scroll bars if used it is implemented
correctly. Some drawbacks would be that as designers we lose some control over
where media and text will wrap as screens change size on different devices.

#### Hybrid

Hybrid layouts use a combination of all of the size values mentioned above.
Ultimately it is up to us as designers to choose the correct layout for
different situations. It is best to understand the pros and cons of each type
and understand when to use one the other or blend them together. More on
responsive design techniques will be discussed in a later lesson.

### Scaling Properties

In order to size our elements we can use the width, height, and min and max
properties for each. Below are a list of these properties with some possible
values separated by `|` pipes.

`width: 1px | 1em | 100%`

`min-width: 1px | 1em | 100%`

`max-width: 1px | 1em | 100%`

`height: 1px | 1em | 100%`

`min-height: 1px | 1em | 100%`

`max-height: 1px | 1em | 100%`

### Overflow

Occasionally when content is larger than its element, it will overflow outside
of it. The `overflow` property allows us to control the way content displays
when it is overflowing outside its element.

`overflow: visible;`

Any content that doesn't fit within the dimensions of its element will cross
over its edges and overflow outside of it.

`overflow: hidden;`

Any content that doesn't fit within the dimensions of the element will be
hidden.

`overflow: scroll;`

Scroll bars will be present upon the element and any content that doesn't fit
within the dimensions of the element will be hidden, but able to be scrolled to.
This essentially turns the element into a small scrolling window where you can
scroll to reveal the hidden content within the element.

`overflow: auto;`

Scroll bars will only be present upon the element if content is larger than the
element, otherwise if no scroll bars are needed they will not be present. Any
content that doesn't fit within the dimensions of the element will be hidden,
but able to be scrolled to. This essentially turns the element into a small
scrolling window where you can scroll to reveal the hidden content within the
element.

### Creating Fluid Heights

In order to create a fluid height, it is important to understand that a height
of a percentage only takes up a percent in relation to its parent element. Let's
say for example that we place a div directly within the body of our page and set
that div to height 100%. Even though the div has 100% height, its parent element
`<body>`, is only as tall as its inner content; our div. This means that in
order to scale our div the full height of the screen we have to set any parent
elements (html, body) to 100% height also.

 ```html
<body>
  <div>Hello</div>
</body>
```

```css
html, body, div {
    height: 100%;
}
```

## Conclusion

In this lesson, you have learned about the different sizing elements you can use
with CSS. To summarize:

- We can size elements using width, height, and min and max values. These
  properties accept pixels, ems, and percents as values.
- Fixed Layouts use pixels. Pixels size look the same on all devices, but may
  create scroll bars of the content is wider than the device or leave empty space
  if the content is much smaller than the device size.
- Elastic Layouts use ems (a typographic unit of measure). Ems insure that when
  a user scales up and down the content, it will maintain the size relationship
  between the layout element and the size of the text within it. This requires
  more testing to insure that none of the content overlaps at different sizes.
- Fluid layouts are sized using percents. They will expand or contract to the
  size of the device. On larger screens they will be larger, on smaller screens
  smaller. This limits our control over when content or media will wrap to the
  next line below.
- Ultimately it is up to us to understand the pros and cons of each type, and
  design the best layout to suit our needs and preference.
- The `overflow` property lets us control the way content that is larger than
  its element displays.
- We can set a fluid height by giving it, and all its parents a `height: 100%`.

## Resources

- [Box Sizing - Code Example](http://jsfiddle.net/flatiron_school/99Tgm/)
- [Fluid Height - Code Example](http://jsfiddle.net/flatiron_school/zDBf3/)
- [Overflow - Code Example](http://jsfiddle.net/flatiron_school/sFfw5/)
- [MDN - CSS - Width](https://developer.mozilla.org/en-US/docs/Web/CSS/width)
- [MDN - CSS - Min-Width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width)
- [MDN - CSS - Max-Width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width)
- [MDN - CSS - Height](https://developer.mozilla.org/en-US/docs/Web/CSS/height)
- [MDN - CSS - Min-Height](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)
- [MDN - CSS - Max-Height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)
- [Smashing Magazine - Which Layout Is Right For You](https://www.smashingmagazine.com/2009/06/fixed-vs-fluid-vs-elastic-layout-whats-the-right-one-for-you/)
