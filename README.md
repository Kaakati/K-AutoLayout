## K-AutoLayout
#### An Autolayout Extension for iOS written in Swift

An AutoLayout Extension for iOS written in Swift that is very easy to use, I found this extension online and I just wanted to document it.


### Example
Add yourView as Subview
```swift
var yourView : UILabel = {
    let label = UILabel()
    label.text = "Your UILabel Text"
    label.textAlignment = .center
    label.translatesAutoresizingMaskIntoConstraints = false // Don't Forget to add this line.
    return label
}()

view.addSubview(yourView)
```

#### Assign AutoLayout as follow `anchorToTop` if you don't want to set margins:

```swift
yourView.anchorToTop(top: view.topAnchor, left: view.leftAnchor, bottom: nil, right: view.rightAnchor)
```

##### OR

#### Assign AutoLayout as follow `anchorWithConstantsToTop` if you want to set margins:

```swift
yourView.anchorWithConstantsToTop(top: view.topAnchor, left: view.leftAnchor, bottom: nil, right: view.rightAnchor, topConstant: 0, leftConstant: 0, bottomConstant: 0, rightConstant: 0)
```

If you want your view to connect to superview bottom edge set `bottom: view.bottomAnchor`

##### OR

To add a `secondView` below `yourView` set it's top: as `yourView.bottomAnchor` 

```swift
secondView.anchorWithConstantsToTop(top: yourView.bottomAnchor, left: view.leftAnchor, bottom: nil, right: view.rightAnchor, topConstant: 0, leftConstant: 0, bottomConstant: 0, rightConstant: 0)
```
