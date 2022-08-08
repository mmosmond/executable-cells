# executable-cells

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tomouellette/executable-cells/HEAD)

## Usage

The steps below describe how to add executable cells (using the specifications outlined in requirements.*) to your markdown or static html pages.

First, add the following script to the top of your markdown document or, alternatively, inside your header if it is an html page.

```html
<script type="text/x-thebe-config">
  {
      requestKernel: true,
      mountActivateWidget: true,
      mountStatusWidget: true,
      binderOptions: {
      repo: "binder-examples/requirements",
      },
  }
</script>
<script src="https://unpkg.com/thebe@latest/lib/index.js"></script>
```

Second, add a button that allows for a user to activate a binder kernel. If the default button style isn't satisfactory, you can modify it by altering the CSS classes *thebe-status* and/or *thebe-activate* in a separate .css stylesheet.

```html
<div style="float: left;" class="thebe-activate"></div>
<div class="thebe-status"></div>
```

Finally, to make an executable cell in your markdown or html document, enclose your code with the following tags.

```html
<pre data-executable="true" data-language="python">
    [code goes here]
</pre>
```

## References

For more details on integrating executable cells into documents or building executable notebooks, please visit the Thebe project (https://github.com/executablebooks/thebe).