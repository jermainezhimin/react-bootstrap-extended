# React Bootstrap Extended

> A version of React Bootstrap which accepts props that add Bootstrap's utility classes

## Quick reference

```
import { Panel } from 'react-bootstrap-extended';

// in your render() method
return (<Panel textUppercase textDanger>My panel is uppercase and red</Panel>);
```

## Motivation

At their best, React components expose simple, clean and statically-typed interfaces (via `propTypes`) that effectively hide their internal complexity. However, these components often are not specifically tailored to our needs, and we resort to the use of `className`s (and `style`) to augment their capabilities.

`className`s are problematic because they are strings with absolutely no validation.

In React Bootstrap (which is the best set of web building blocks, bar none), I often find myself adding Bootstrap utility classes to existing components, e.g.

`<Button className="pull-right"></Button>`

Some disadvantages to this method include:

1. It is more difficult to statically analyze and quickly examine. For example, `pul-right` may sneak through code review.
2. It is difficult to distinguish one-off classes (e.g. `className="my-login-button"`) from global classes. This prevents code reuse: another developer will not know that they can re-use the `pull-right` class and instead, will write that CSS themselves.

This package brings that static typing to bootstrap utility classes.

## API

This package exposes all of the original bootstrap components, and utils, and wraps the appropriate ones.

## Full list of props and utility classes

The keys in this object are the prop names. The values are the classes applied.

```
{
  "textMuted": "text-muted",
  "textPrimary": "text-primary",
  "textSuccess": "text-success",
  "textInfo": "text-info",
  "textWarning": "text-warning",
  "textDanger": "text-danger",
  "bgPrimary": "bg-primary",
  "bgSuccess": "bg-success",
  "bgInfo": "bg-info",
  "bgWarning": "bg-warning",
  "bgDanger": "bg-danger",
  "pullLeft": "pull-left",
  "pullRight": "pull-right",
  "navbarLeft": "navbar-left",
  "navbarRight": "navbar-right",
  "centerBlock": "center-block",
  "clearfix": "clearfix",
  "invisible": "invisible",
  "srOnly": "sr-only",
  "srOnlyFocusable": "sr-only sr-only-focusable",
  "textHide": "text-hide",
  "visibleXsBlock": "visible-xs-block",
  "visibleXsInline": "visible-xs-inline",
  "visibleXsInlineBlock": "visible-xs-inline-block",
  "hiddenXs": "hidden-xs",
  "visibleSmBlock": "visible-sm-block",
  "visibleSmInline": "visible-sm-inline",
  "visibleSmInlineBlock": "visible-sm-inline-block",
  "hiddenSm": "hidden-sm",
  "visibleMdBlock": "visible-md-block",
  "visibleMdInline": "visible-md-inline",
  "visibleMdInlineBlock": "visible-md-inline-block",
  "hiddenMd": "hidden-md",
  "visibleLgBlock": "visible-lg-block",
  "visibleLgInline": "visible-lg-inline",
  "visibleLgInlineBlock": "visible-lg-inline-block",
  "hiddenLg": "hidden-lg",
  "visiblePrintBlock": "visible-print-block",
  "visiblePrintInline": "visible-print-inline",
  "visiblePrintInlineBlock": "visible-print-inline-block",
  "hiddenPrint": "hidden-print",
  "textLeft": "text-left",
  "textCenter": "text-center",
  "textRight": "text-right",
  "textJustify": "text-justify",
  "textNowrap": "text-nowrap",
  "textLowercase": "text-lowercase",
  "textUppercase": "text-uppercase",
  "textCapitalize": "text-capitalize",
  "initialism": "initialism"
}
```

## My favorite bootstrap classes are omitted!

I omitted classes like `show`, `hidden`, `caret` and `close` because they are way too generic and will conflict with existing props.

I omitted classes like `lead`, `blockquote-reverse`, etc. because they are too component-specific.

If you want to add these back, a future release will give you that ability!

## TODO

* Nested components are not handled yet.
* Expose an easy way of adding addition classes for classes you custom-defined.

## Contributing

Please, feel free to reach out and contribute! [robert.balicki@gmail.com](mailto:robert.balicki@gmail.com)