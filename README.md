# panza
Panza is a collection of ui-components for react-native modelled after iOS.

This library is currently undergoing a rewrite and will be updated soon along with new documentation.

<p>
<img src='images/panza-ios-large.png' width='375px' />
<img src='images/panza-android-large.png' width='360px' />
</p>

## Getting Started
```
$ npm i panza --save
$ npm i react-native-vector-icons --save
$ rnpm link react-native-vector-icons
```

## Components

### Inputs
* [InputRow](documentation/InputRow.md)
* [InputGroup](documentation/InputGroup.md)
* [InputHelpText](documentation/InputHelpText.md)
* [InputToggle](documentation/InputToggle.md)
* [InputPicker](documentation/InputPicker.md)
* [InputDatePicker](documentation/InputDatePicker.md)
* [RemovableInput](documentation/RemovableInput.md)
* [AddRow](documentation/AddRow.md)
* [TouchableInput](documentation/TouchableInput.md)

### Rows
* [TouchableRow](documentation/TouchableRow.md)
* [RowSeparator](documentation/RowSeparator.md)
* [RowImage](documentation/RowImage.md)
* [SectionHeader](documentation/SectionHeader.md)

### Navigation
* [NavBar](documentation/NavBar.md)
* [NavTitle](documentation/NavTitle.md)
* [NavTouchableIcon](documentation/NavTouchableIcon.md)
* [NavTouchableText](documentation/NavTouchableText.md)
* [SubNav](documentation/SubNav.md)

### Pages
* [ErrorPage](documentation/ErrorPage.md)
* [LoadingPage](documentation/LoadingPage.md)

### Buttons
* [Button](documentation/Button.md)
* [PrimaryButton](documentation/PrimaryButton.md)
* [WarningButton](documentation/WarningButton.md)
* [ErrorButton](documentation/ErrorButton.md)
* [SuccessButton](documentation/SuccessButton.md)
* [NakedButton](documentation/NakedButton.md)
* [VerticalButtonGroup](documentation/VerticalButtonGroup.md)

### Text
* [PrimaryText](documentation/PrimaryText.md)
* [SecondaryText](documentation/SecondaryText.md)
* [LargeText](documentation/LargeText.md)
* [SubtitleText](documentation/SubtitleText.md)
* [PrimaryTextInput](documentation/PrimaryTextInput.md)
* [SecondaryTextInput](documentation/SecondaryTextInput.md)

### Images
* [FadeImage](documentation/FadeImage.md)

### Icons
* [Icon](documentation/Icon.md)
* TouchableIcon
* PlusIcon
* ArrowRightIcon
* CloseIcon
* BackIcon
* SearchIcon
* MoreIcon

### Base Components
* [Base](documentation/Base.md)
* [TextBase](documentation/TextBase.md)


## Customize

You can override parts of the global configuration to provide custom colours, font sizes, scales, etc.

```javascript
import { config } from 'panza'

class App extends React.Component {

  static childContextTypes = {
    panza: PropTypes.object
  }

  getChildContext() {
    panza: this.state.styles
  }

  state = {
    styles: {
      colors: Object.assign(
        {},
        config.colors,
        { primary: config.colors.red } // change the primary color from blue to red
      )
    }
  }

  // ... render your app
}
```

## Example

You can install the example application contained within this repository.

```
$ git clone https://github.com/bmcmahen/panza.git
$ cd panza && npm install
$ react-native run-ios
$ react-native run-android
```

## License
MIT
