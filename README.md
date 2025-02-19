# react-native-select2

## Component like [Select2](https://select2.org/) on web for React Native

![Single select](https://raw.githubusercontent.com/xuho/demo-images/master/react-native-select2-single-select.gif)

## Add it to your project
  - Using NPM
    `npm i @marcelodiegues/react-native-select2`


## Install dependencies

1. [react-native-modal](https://github.com/react-native-community/react-native-modal)
2. [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons)


## Usage

```javascript
import React, { Component } from "react"
import { View, Text, StyleSheet } from "react-native"
import Select2 from "react-native-select2"

const mockData = [
  { id: 1, name: "React Native Developer", checked: true }, // set default checked for render option item
  { id: 2, name: "Android Developer" },
  { id: 3, name: "iOS Developer" }
]

// create a component
class CreateNewAppointment extends Component {
  render() {
    return (
      <View style={styles.container}>
        <Select2
          isSelectSingle
          style={{ borderRadius: 5 }}
          colorTheme="blue"
          popupTitle="Select item"
          title="Select item"
          data={mockData}
          onSelect={data => {
            this.setState({ data })
          }}
          onRemoveItem={data => {
            this.setState({ data })
          }}
        />
      </View>
    )
  }
}
```

### Multiple select

![Multiple select](https://raw.githubusercontent.com/xuho/demo-images/master/react-native-select2-multipe-select.gif)

## Properties

| Property name             | Type           | Default                         | Description                                                                                 |
| ------------------------- | -------------- | ------------------------------- | ------------------------------------------------------------------------------------------- |
| **style**                 | _Object_       | none                            | Custom style for component                                                                  |
| **modalStyle**            | _Object_       | none                            | Custom style for modal                                                                      |
| **title**                 | _String_       | none                            | String display when you don't select any item                                               |
| **data**                  | _Array_        | \*required                      | Datasource of list options: an array of objects (each object have `name` and `id` property) |
| **onSelect**              | _Function_     | none                            | The callback function trigger after you press select button                                 |
| **onRemoveItem**          | _Function_     | none                            | The callback function trigger after you press tags to remove them                           |
| **popupTitle**            | _String_       | none                            | Title of modal select item                                                                  |
| **colorTheme**            | _string/color_ | #16a45f                         | Color for componet                                                                          |
| **isSelectSingle**        | _Bool_         | false                           | Selelect only one option                                                                    |
| **showSearchBox**         | _Bool_         | true                            | Show or hide search field                                                                   |
| **cancelButtonText**      | _string_       | Cancel                             | Cancel button text title                                                                    |
| **selectButtonText**      | _String_       | Select                            | Select button text title                                                                    |
| **searchPlaceHolderText** | _String_       | Search...                | Placeholder text for search field                                                           |
| **listEmptyTitle**        | _String_       | No matches found | Title to show when there's no item to be render                                             |
| **defaultFontName**       | _String_       | none                            | Set custom font for all component                                                           |
| **selectedTitleStyle**    | _Object_       | none                            | Set custom style for display selected title text                                            |
| **buttonTextStyle**       | _Object_       | none                            | Set custom button text style                                                                |
| **buttonStyle**           | _Object_       | none                            | Set custom button style                                                                     |
| **disabledSelect**       | _Bool_       | none                            | Disable Select

**MIT Licensed**
