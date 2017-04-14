<img src="http://snapkit.io/images/banner.jpg" alt="" />

SnapKit is a DSL to make Auto Layout easy on both iOS and OS X.

[![Build Status](https://travis-ci.org/SnapKit/SnapKit.svg)](https://travis-ci.org/SnapKit/SnapKit)
[![Platform](https://img.shields.io/cocoapods/p/SnapKit.svg?style=flat)](https://github.com/SnapKit/SnapKit)
[![Cocoapods Compatible](https://img.shields.io/cocoapods/v/SnapKit.svg)](https://cocoapods.org/pods/SnapKit)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Platform](https://img.shields.io/cocoapods/p/Alamofire.svg?style=flat)](http://cocoadocs.org/docsets/Alamofire)

## Features

- [x] Simple & Expressive
- [x] Type Safe
- [x] Compatible for both iOS and OS X apps
- [x] Free to use in all projects and licensed under the flexible MIT license
- [x] [Complete Documentation](http://snapkit.io/docs/)

## Requirements

- iOS 7.0+ / Mac OS X 10.9+ 
- Xcode 7.0+
- Swift 2.0

## Communication

- If you **need help**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/snapkit). (Tag 'snapkit')
- If you'd like to **ask a general question**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/snapkit).
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.

## Installation

### CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

> CocoaPods 0.39.0+ is required to build Alamofire 3.0.0+.

To integrate Snapkit into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'
use_frameworks!

pod 'SnapKit', '~> 0.15.0'
end
```

Then, run the following command:

```bash
$ pod install
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that builds your dependencies and provides you with binary frameworks.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate Snapkit into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "SnapKit/SnapKit" >= 0.15.0
```

Add SnapKit as a submodule by opening the Terminal, cd-ing into your top-level project directory, and entering the following command:

```bash
$ git submodule add https://github.com/SnapKit/SnapKit.git
```

Open the SnapKit folder, and drag `SnapKit.xcodeproj` into the file navigator of your app project.
In Xcode, navigate to the target configuration window by clicking on the blue project icon, and selecting the application target under the `Targets` heading in the sidebar.

Ensure that the deployment target of `SnapKit.framework` matches that of the application target.
In the tab bar at the top of that window, open the "Build Phases" panel.
Expand the "Target Dependencies" group, and add `SnapKit.framework`.

Click on the + button at the top left of the panel and select "New Copy Files Phase". Rename this new phase to "Copy
Frameworks", set the "Destination" to "Frameworks", and add `SnapKit.framework`.

## Usage

#### ⚠️ **To use with Swift 2.x please ensure you are using == 0.22.0** ⚠️ 
#### ⚠️ **To use with Swift 3.x please ensure you are using >= 3.0.0** ⚠️ 

## Contents

- [Requirements](#requirements)
- [Migration Guides](#migration-guides)
- [Communication](#communication)
- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Requirements

- iOS 8.0+ / Mac OS X 10.11+ / tvOS 9.0+
- Xcode 8.0+
- Swift 3.0+

## Migration Guides

- [SnapKit 3.0 Migration Guide](https://github.com/SnapKit/SnapKit/blob/master/Documentation/SnapKit%203.0%20Migration%20Guide.md)

## Communication

- If you **need help**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/snapkit). (Tag 'snapkit')
- If you'd like to **ask a general question**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/snapkit).
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.


## Installation

### CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

> CocoaPods 1.1.0+ is required to build SnapKit 3.0.0+.

To integrate SnapKit into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '10.0'
use_frameworks!

target '<Your Target Name>' do
    pod 'SnapKit', '~> 3.2.0'
end
```

Then, run the following command:

```bash
$ pod install
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that builds your dependencies and provides you with binary frameworks.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate SnapKit into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "SnapKit/SnapKit" ~> 3.2.0
```

Run `carthage update` to build the framework and drag the built `SnapKit.framework` into your Xcode project.

### Manually

If you prefer not to use either of the aforementioned dependency managers, you can integrate SnapKit into your project manually.

---

## Usage

### Quick Start

```swift
import SnapKit

class MyViewController: UIViewController {

    lazy var box = UIView()

    override func viewDidLoad() {
        super.viewDidLoad()

        self.view.addSubview(box)
        box.snp.makeConstraints { (make) -> Void in
           make.width.height.equalTo(50)
           make.center.equalTo(self.view)
        }
    }

}
```

### Resources

- [Documentation](http://snapkit.io/docs/)
- [F.A.Q.](http://snapkit.io/faq/)

## Credits

- Robert Payne ([@robertjpayne](https://twitter.com/robertjpayne))
- Many other contributors

## License

SnapKit is released under the MIT license. See LICENSE for details.
