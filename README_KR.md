# things-tristate-checkbox

tristate-checkbox
`tristate-checkbox`는[`paper-checkbox`](https://elements.polymer-project.org/elements/paper-checkbox)와 유사한 web component이다.

Example:

```html
    <things-tristate-checkbox>label</things-tristate-checkbox>
    <things-tristate-checkbox state="on">label</things-tristate-checkbox>
```

web component는 W3C의[WAI-ARIA 1.0 Authoring Practices](https://www.w3.org/TR/wai-aria-practices/#checkbox)에 따라 'aria-checked'속성을 처리합니다.

### Styling
The following custom properties and mixins are available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--things-tristate-unchecked-background-color` | input에 체크되어 있지 않을 때 checkbox의 배경 색 | `transparent`
`--things-tristate-unchecked-color` | input에 체크되어 있지 않을 때 Checkbox border 색 | `--primary-text-color`
`--things-tristate-unchecked-ink-color` | input에 체크되어 있지 않을 때 Selected/focus ripple 색 | `--primary-text-color`
`--things-tristate-checked-color` | input에 체크되어 있을 때 Checkbox 색 | `--primary-color`
`--things-tristate-checked-ink-color` | input에 체크되어 있을 때 Selected/focus ripple 색 | `--primary-color`
`--things-tristate-checkmark-color` | Checkmark 색 | `white`
`--things-tristate-label-color` | Label 색 | `--primary-text-color`
`--things-tristate-label-spacing` | label과 checkbox사이의 공간 | `8px`
`--things-tristate-error-color` | invalid상태 때 Checkbox 색 | `--error-color`
`--things-tristate-size` | checkbox의 사이즈 | `18px`

#### From `paper-checkbox` __:__
> 이 element는 `--paper-font-common-base`을 적용하지만 `paper-styles/typography.html`을 import하지 않는다.
> 이 element에 'Roboto' 폰트를 적용하려면, `paper-styles/typography.html`를 가져왔는지 확인해야한다.

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

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

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


## Example 1. Things tristate checkbox
`<things-tristate-checkbox>` Things Tristate checkbox
