# SwiftUIExtensions

## Presentation items

```swift
@State var alertItem: AlertItem? = nil
@State var sheetItem: SheetItem? = nil
@State var actionSheetItem: ActionSheetItem? = nil

currentView
    .alert(item: $alertItem, content: { $0.alert })
    .sheet(item: $sheetItem, content: { $0 })
    .actionSheet(item: $actionSheetItem, content: { $0.actionSheet })
```

## Fitting Image Scale

```swift
Image("img").fitting(width: 56, height: 32, contentMode: .fill)
Image("img").fitting(width: 45, height: 86, contentMode: .fit)
```

<img src="https://github.com/noppefoxwolf/SwiftUIExtensions/blob/master/.github/fitting.png" width="320">

## UIKit Wrapper

- ActivityIndicator
- SafariView

## TabBarView

Tab style view that able to keep view presentation state.

```swift
TabBarView {
    Text("1").tabBarItem(title: "item1", image: UIImage(systemName: "circle.fill"))
    
    Text("2").tabBarItem(title: "item2", image: UIImage(systemName: "circle.fill"))

    Text("3").tabBarItem(title: "item3", image: UIImage(systemName: "circle.fill"))
}
```

## SwiftUIExtensions.UIView

Easy to wrap UIView and optimizing differential update.

```swift
import UIKit
import SwiftUIExtensions
typealias UITextView = SwiftUIExtensions.UIView<UIKit.UITextView, String>
```

```swift
UITextView(text) { (textView, value, context) in
    // call only value changed
    uiView.attributedText = NSAttributedString(string: value, options: options)
}
```

# Other extensions

[noppefoxwolf/RefreshUI](https://github.com/noppefoxwolf/RefreshUI)
