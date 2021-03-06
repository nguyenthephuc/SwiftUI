## CheckBox Swift
*Drag & drop file NTPCheckBox.swift to your project*

*go to images.xcassets add two image with name* **Checked** *and* **unChecked**
```swift
// init NTPCheckBox
let checkbox = NTPCheckBox(frame: CGRectMake(20, 100, 200, 15), name: "name-of-checkbox", text: "text display for check box", value: "1", checked: true)
   
// add checkbox to viewController
self.view.addSubview(checkbox)

// get value after checked
let checked = NTPCheckBox.getAllChecked("name-of-checkbox") // return array value
// Besides you can adjust color for text display in checkbox with `titleColor` in step init NTPCheckBox

```

## Radio Swift
*Drag & drop file NTPRadio.swift to your project*

*go to images.xcassets add two image with name* **Selected** *and* **unSelected**
```swift
// init NTPRadio
let radio = NTPRadio(frame: CGRectMake(20, 100, 200, 15), name: "name-of-radio", text: "text display for radio", value: "1", selected: true)

// add radio to viewController
self.view.addSubview(radio)

// get value after selected
let selected = NTPRadio.getSelected("name-of-radio") // return string value
// Besides you can adjust color for text display in radio with `titleColor` in step init NTPRadio
```

## Popup Select List
*Drag & drop file NTPListPopup.swift to your project*

```swift
// from your viewController extend `NTPListPopupDelegate`
// data must be a array Array<Dictionary<String,String>>
let data = [["key": "1", "value": "iphone"], ["key": "2", "value": "samsung"]]
// init NTPListPopup
let dialog = NTPListPopup(view: self, title: "your title", options: data)
dialog.delegate = self
// set selected @param: key
dialog.setSelected(key)
// show dialog
dialog.show()
// get value when tap to cell in list popup
func NTPListPopupClickedAtButtonIndex(index: String){
   // index is the key in array `data`
}
```

## Card
*Drag & drop file NTPCard.swift to your project*

```swift
let card: NTPCard = NTPCard(frame: CGRect(0, 0, 0, 0))
self.view.addSubview(card)
```

## Show Alert
*Drag & drop file NTPAlert.swift to your project*

```swift
NTPAlert(win: self, message: "put your message here", type: .Warning, delay: 3).show()
```

## Show Loading
*Drag & drop file NTPLoading.swift to your project*

```swift
NTPLoading().show()
NTPLoading().hide()
```

awesome :+1:
