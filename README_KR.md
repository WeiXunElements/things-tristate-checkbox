# things-tristate-checkbox

이는 [`paper-checkbox`](https://elements.polymer-project.org/elements/paper-checkbox)와 유사한 web component이다.

Example:

```html
    <things-tristate-checkbox>label</things-tristate-checkbox>
    <things-tristate-checkbox state="on">label</things-tristate-checkbox>
```

web component는 W3C의 [WAI-ARIA 1.0 Authoring Practices](https://www.w3.org/TR/wai-aria-practices/#checkbox)에 따라 'aria-checked' 속성을 처리합니다.

### Styling
스타일에 사용할 수 있는 사용자 정의 속성 및 혼합 유형은 다음과 같습니다.

Custom property | Description | Default
----------------|-------------|----------
`--things-tristate-unchecked-background-color` | input이 체크되어 있지 않을 때 checkbox의 배경색 | `transparent`
`--things-tristate-unchecked-color` | input이 체크되어 있지 않을 때 Checkbox border 색상 | `--primary-text-color`
`--things-tristate-unchecked-ink-color` | input이 체크되어 있지 않을 때 Selected/focus ripple 색상 | `--primary-text-color`
`--things-tristate-checked-color` | input이 체크되어 있을 때 Checkbox 색상 | `--primary-color`
`--things-tristate-checked-ink-color` | input이 체크되어 있을 때 Selected/focus ripple 색상 | `--primary-color`
`--things-tristate-checkmark-color` | Checkmark 색상 | `white`
`--things-tristate-label-color` | Label 색상 | `--primary-text-color`
`--things-tristate-label-spacing` | label과 checkbox 사이의 공간 | `8px`
`--things-tristate-error-color` | invalid 상태일 때의 Checkbox 색상 | `--error-color`
`--things-tristate-size` | checkbox 사이즈 | `18px`

#### From `paper-checkbox` __:__
> 이 element는 `--paper-font-common-base`를 적용하지만 `paper-styles/typography.html`을 import하지 않는다.
> 이 element에 'Roboto' 폰트를 적용하려면, `paper-styles/typography.html`을 가져왔는지 확인해야 한다.

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

Eelement의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

다음, element의 종속성을 다운로드한다.

    bower install


## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-tristate-checkbox`가 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-tristate-checkbox/`를 통해 이를 미리 확인할 수 있다. 
