# Random Color Swift

Inspired by David Merfield's [randomColor.js](https://github.com/davidmerfield/randomColor). It is a ported version to Swift. You can use the library to generate attractive random colors on iOS or macOS.

See the [demo and site](http://llllll.li/randomColor/) to know why does this exist.

![](https://raw.githubusercontent.com/onevcat/RandomColorSwift/master/demo.png)

## Install

This framework supports Swift 3.0 / Xcode 8 and above. If you need an earlier version for Swift 2, use [version 0.1.0](https://github.com/onevcat/RandomColorSwift/releases/tag/0.1.0) instead.

### CocoaPods

The easiest way to use `RandomColor` is installing it by [CocoaPods](http://cocoapods.org). Add these lines to your Podfile:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'
# platform :osx, '10.10'
use_frameworks!

pod 'RandomColorSwift'
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is also supported:

```ogdl
github "onevcat/RandomColorSwift"
```

### Manually

If you need to support iOS 7.x, you will need to add the library manually into your project since dynamic framework is not supported for iOS 7.

Clone this repo and throw the source files under `RandomColor` folder into your project to use it. 

## Example

```swift
import RandomColorSwift

// Returns a UIColor or NSColor object for an attractive color
let color = randomColor()

// Returns an array of ten green colors
let greenColors = randomColors(count: 10, hue: .green)

// Returns a color for light blue
let lightBlurColor = randomColor(hue: .blue, luminosity: .light)

// Returns a color for a 'truly random' color
let randomColor = randomColor(hue: .random, luminosity: .random)

// Returns an array of ten dark pink colors
let darkPinkColors = randomColors(count: 10, hue: .pink, luminosity: .dark)

// Returns an array of twenty colors at hue of 120
let colors = randomColors(count: 20, hue: .value(120), luminosity: .random)

```

There is also a demo project in this repo.

## Options

You can pass an options object to influence the type of color it produces. The options object accepts the following properties:

**Hue** – Controls the hue of the generated color. Possible hue values for colors are `.monochrome`, `.red`, `.orange`, `.yellow`, `.green`, `.blue`, `.purple`, `.pink`, `.random` or `.value(Int)`. If you use `.value(Int)`, you should pass an `Int` between 0 and 360.

**Luminosity** – Controls the luminosity of the generated color. You can pass `.bright`, `.light`, `.dark` or `.random`.

**Count** – An `Int` which specifies the number of colors to generate.

## Acknowledgements

Thanks for David Merfield bringing us randomColor.js, which is a great utility.

The demo project is using Chirag Mehta's [Name the Color](http://chir.ag/projects/name-that-color) JavaScript library to extract name of color.

## License

This project is licensed under the terms of the MIT license.


