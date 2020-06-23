# ALRadioButtons

**iOS RadioButtons with native style.**  Simple to use, inherited from UIControl, fully customizable.

## Navigation

- [Requirements](#requirements)
- [Installation](#installation)
  - [Swift Package Manager](#Swift-Package-Manager)
  - [CocoaPods](#CocoaPods)
  - [Manually](#Manually)
- [Usage](#usage)
  - [Quick Start](#Quick-Start)
  - [Customization](#Customization)
- [License](https://github.com/SnapKit/SnapKit#license)

## 

## Requirements

- iOS 10.0 + 
- Swift 4.2 +



## Installation

#### Swift Package Manager

The [Swift Package Manager](https://swift.org/package-manager/) is a tool for managing the distribution of Swift code. It’s integrated with the Swift build system to automate the process of downloading, compiling, and linking dependencies.

To integrate **ALRadioButtons** click `File -> Swift Package -> Add Package Dependency` and insert:

```ogdl
https://github.com/alxrguz/ALRadioButtons
```

#### CocoaPods

**ALRadioButtons** is available through [CocoaPods](http://cocoapods.org/). To install it, simply add the following line to your Podfile:

```ruby
pod 'ALRadioButtons'
```

#### Manually

If you prefer not to use either of the aforementioned dependency managers, you can integrate SnapKit into your project manually. Put `Source/ALRadioButtons` folder in your Xcode project. 



## Usage

#### Quick Start

```swift
import ALRadioButtons

class MyViewController: UIViewController {

    lazy var radioGroup = ALRadioGroup(items: [
        .init(title: "title1", subtitle: "subtitle1"),
        .init(title: "title2", subtitle: "subtitle2"),
        .init(title: "title3"),
    ], style: .grouped)

    override func viewDidLoad() {
        super.viewDidLoad()

        self.view.addSubview(radioGroup)
        // ... Setup layout
        
        radioGroup.selectedIndex = 0
				radioGroup.addTarget(self, action: #selector(radioGroupSelected(_:)), for: .valueChanged)
    }
    
    @objc private func radioGroupSelected(_ sender: ALRadioGroup) {
        print(sender.selectedIndex)
    }
}
```



#### Customization

In progress....

## License

**ALRadioButtons** is under MIT license. See the [LICENSE](https://github.com/alxrguz/ALRadioButtons/blob/master/LICENSE) file for more info.

