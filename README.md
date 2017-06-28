# things-tristate-checkbox

This is a web component similar to [`paper-checkbox`](https://elements.polymer-project.org/elements/paper-checkbox).

Example:

```html
    <things-tristate-checkbox>label</things-tristate-checkbox>
    <things-tristate-checkbox state="on">label</things-tristate-checkbox>
```

The web component handles 'aria-checked' attribute according to W3C's [WAI-ARIA 1.0 Authoring Practices](https://www.w3.org/TR/wai-aria-practices/#checkbox).

### Styling
The following custom properties and mixins are available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--things-tristate-unchecked-background-color` | Checkbox background color when input is not checked | `transparent`
`--things-tristate-unchecked-color` | Checkbox border color when input is not checked | `--primary-text-color`
`--things-tristate-unchecked-ink-color` | Selected/focus ripple color when input is not checked
 | `--primary-text-color`
`--things-tristate-checked-color` | Checkbox color when input is checked | `--primary-color`
`--things-tristate-checked-ink-color` | Selected/focus ripple color when input is checked | `--primary-color`
`--things-tristate-checkmark-color` | Checkmark color | `white`
`--things-tristate-label-color` | Label color | `--primary-text-color`
`--things-tristate-label-spacing` | The space between label and checkbox | `8px`
`--things-tristate-error-color` | Checkbox color when invalid | `--error-color`
`--things-tristate-size` | Checkbox size | `18px`

#### From `paper-checkbox` __:__
> This element applies `--paper-font-common-base` but does not import `paper-styles/typography.html`.
> To apply 'Roboto' font to this element, make sure you have imported `paper-styles/typography.html`.

Example:

```html
<demo-snippet class="centered-demo">
  <template>
    <sample-tristate-checkbox></sample-tristate-checkbox>
    <things-tristate-checkbox>label</things-tristate-checkbox>
    <things-tristate-checkbox state="on">label</things-tristate-checkbox>

    <dom-module id="sample-tristate-checkbox">
      <template>
        <things-tristate-checkbox
          id="tristate-checkbox"
          label="Tristate Checkbox"
          state="{{state}}">
        </things-tristate-checkbox>

        <paper-input
          label="Checkbox State"
          value="{{state}}">
        </paper-input>
      </template>

      <script>
        Polymer({
          is: "sample-tristate-checkbox",

          state: {
            type: String,
            notify: true
          }
        });
      </script>
    </dom-module>
  </template>
</demo-snippet>
```


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-tristate-checkbox/`, where `things-tristate-checkbox` is the name of the directory containing it.
