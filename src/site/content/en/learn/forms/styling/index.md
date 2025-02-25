---
title: Styling forms
description: >
  In this module, you learn how to style forms.
authors:
  - michaelscharnagl
date: 2021-10-07
---

## Help users use your form with their preferred browser

To ensure people can use your form, use the elements built for the job, 
such as `<input>`, `<textarea>`, `<select>`, and `<button>`. 
This is the baseline for a usable form.

{% Codepen {
  user: 'web-dot-dev',
  id: '9d0576454b3b2d0fc001addab70d25bc',
  height: 300
} %}

The default browser styles don't look great, let's change that.

{% Aside %}
Progressive enhancement (PE) is a strategy that provides a baseline of essential content and features for as many users as possible. 
It ensures the best possible experience for users on modern browsers.

You start with content, use 
[semantic HTML](https://developer.mozilla.org/docs/Glossary/Semantics#semantics_in_html), 
add future-proof CSS, and add robust JavaScript as a last step.
{% endAside %}

## Ensure form controls are readable for everyone

The default font size for form controls in most browsers is too small. 
To ensure your form controls are readable, change the font size with CSS:

{% Codepen {
  user: 'web-dot-dev',
  id: '477f5e58a406c6f86bfbfc9da1f18a69',
  height: 300
} %}

Increase the `font-size` and `line-height` to improve readability.

```css
.form-element {
  font-size: 1.3rem;
  line-height: 1.2;
}
``` 

{% Aside %}
Use relative units like `em` (relative to the base size of the parent's element) or `rem` 
(relative to the base size of the document) for the font size, 
to ensure the size responds to user preference. 
You can change the base `font-size` and all elements with a relative `font-size` automatically. 
For `line-height` use a unitless value, to keep the line height relative to the font size.

Learn more about 
[pixels vs. relative units in CSS](https://www.24a11y.com/2019/pixels-vs-relative-units-in-css-why-its-still-a-big-deal/).
{% endAside %}

## Help users navigate through your form

As a next step, change the layout of your form, and increase the spacing of form elements, 
to help users understand which elements belong together.

{% Codepen {
  user: 'web-dot-dev',
  id: 'f2aca03916816074010e896f064f456a',
  height: 300
} %}

The `margin` CSS property increases space between elements, 
and the `padding` property increases space around the element's content.

For the general layout, use Flexbox or Grid. 
Learn more about [CSS layout methods](/learn/css/layout/).

## Ensure form controls look like form controls

Make it easy for people to fill out your form by using well-understood styles for your form controls. 
For example, style `<input>` elements with a solid border. 

{% Aside %}
The default `<input>` border color is too light in many browsers. 
The lack of contrast makes it hard for some users to see the `<input>`. 
[Open this demo](https://codepen.io/web-dot-dev/pen/9d0576454b3b2d0fc001addab70d25bc) in Chrome on Android to see the default styles.
{% endAside %}

{% Codepen {
  user: 'web-dot-dev',
  id: 'd0740e968b5c72a0cf180359e80f5efc',
  height: 500
} %}


```css
input,
textarea {
  border: 1px solid;
}
```

## Help users submit your form

Consider using a `background` for your `<button>` to match your site style, 
and override or remove the default `border` styles.

{% Codepen {
  user: 'web-dot-dev',
  id: 'f0052d40806fd750362fa0abaab01dcf',
  height: 500
} %}

{% Aside %}
In modern browsers, you can style a `<button>` like any other element, 
so you should always use a semantic `<button>`, or `<input type="submit">`. 
Using the element built for the job provides many built-in usability and accessibility 
benefits that you won't get when using a generic element, for example, a `<div>`. 
You'll learn about the built-in features in other modules.

Learn more about 
[reverting the default style of a `<button>`](https://archive.hankchizljaw.com/wrote/introducing-the-button-element/#heading-oh-these-are-hard-to-style-though).
{% endAside %}

## Help users understand the current state

Browsers apply a default style for `:focus`. 
You can override the styles for `:focus` to match the color to your brand. 

```css
button:focus {
    outline: 4px solid green;
}
```

{% Aside %}
Only remove the `outline` on `:focus` if you also add other appropriate focus styles, 
to ensure that  default and focus styles are distinguishable.

Learn more about 
[designing focus indicators](https://www.sarasoueidan.com/blog/focus-indicators/).
{% endAside %}

{% Assessment 'styling' %}

## Resources

- [Learn CSS](/learn/css)
- [CSS layout methods](/learn/css/layout)
- [Designing focus indicators](https://www.sarasoueidan.com/blog/focus-indicators/)
- [Reverting the default style of a `<button>`](https://archive.hankchizljaw.com/wrote/introducing-the-button-element/#heading-oh-these-are-hard-to-style-though).
