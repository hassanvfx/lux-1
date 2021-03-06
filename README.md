<img src="https://res.cloudinary.com/maxwelldesign/image/upload/v1591974050/static/maxwelldesign5_caeiey.jpg" alt="" />

MAXWELL **L U X** makes app development faster (and magic)! Craft customized UI Design Systems ready to be used in SwiftUI—even if you’re not a design expert!

#### ⚠️ **To use with Swift 5.x. Please ensure you are using >= 5.1.0** ⚠️

## Contents

- [Requirements](#requirements)
- [Communication](#communication)
- [Installation](#installation)
- [SPM](#spm)
- [Cocoapods](#cocoapods)
- [Usage](#usage)
- [LUX Specificaiton](#specification)
- [LUX Stream](#stream)
- [Credits](#credits)
- [License](#license)

## Requirements

- iOS 13.1+ / Mac OS X 10.15+
- Xcode 11.3+
- Swift 5.1+

## Communication

- If you **need help**, use [Discord](https://luxyfy.me/lnk/discord). (Tag 'lux')
- If you'd like to **ask a general question**, use [Stack Overflow](http://stackoverflow.com/questions/tagged/lux).
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.

## Installation

<img src="https://user-images.githubusercontent.com/66370095/84549297-468adc00-accd-11ea-9e20-d0cf91016f9c.png" alt="" />

### SPM
[Swift Package Manager](https://github.com/apple/swift-package-manager) is a dependency manager for Cocoa projects. 

You can install Lux by importing this repo's url into Xcode.

```
https://github.com/maxwelldesign/lux
```

----



### CocoaPods
>  Notice: There are some known issues with CocoaPods and Xcode-Canvas. Whenever possible, please prefer the SPM install option. Experimental LUX import as SPM package inside a CocoaPods project has been successful.


[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

> CocoaPods 1.1.0+ is required to build Lux 1.0.0+.


To integrate Lux into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '10.0'
use_frameworks!

target '<Your Target Name>' do
    pod 'Lux', '~> 1.0.0'
end
```

Then, run the following command:

```bash
$ pod install
```



## Usage

### Quick Start

```swift
import SwiftUI
import Lux

struct ContentView: View {

    var body: some View{
      Column{
        Row{
          Text("Hello World")
          .lux
          .trait(.title)
          .style(.paragraph)
          .view
        }
      }
      .lux
      .style(.panel)
      .feature(.padding, .shadow,)
      .card
      .view
    }

}
```
---

### Specification

<img src="https://res.cloudinary.com/maxwelldesign/image/upload/v1591974050/static/maxwelldesign_qhplxk.jpg" alt="" />

Install the Maxwell App to create LUX specifications. It's available for iOS and macOS from the MAXWELL DESIGN website:

- [Install](https://maxwell.design)

From the Maxwell App:

- From the Home select the LUX tab
- Tap on a look to enter the editor
- Tap on the paperplane icon
- At the bottom of the action sheet locate the "options"
- Tap the options button
- Select "Init Config"

Note: If you are in the simulator, use "Get Pasteboard" from the menu to transmit the data to macOS.

Once ready, open Xcode and paste the configuration code BEFORE attaching your views, ideally in the Scene Delegate, ie:

```swift
 func initializeLook(){
        do{
            try Look.set(data64:" SOME DATA")
        }catch{
            print("error")
        }
  }
```

### Stream

<img src="https://res.cloudinary.com/maxwelldesign/image/upload/v1591974050/static/maxwelldesign3_zpa2bd.jpg" alt="" />

You can tweak any LUX powered application in realtime from the MAXWELL APP.

- [Install](https://maxwell.design)

Add this to your launch code:

```swift
 func tuneLux(){
        Look.tunning()
  }
```

Then to dynamically update any view simple add this Observable definition for the global Look state:

```
struct ContentView: View {
    @ObservedObject var state = Look.state
    ...
```

> Note: You can name it in any way.

### Playground

You can try Lux in Playground.

**Note:**

> To try Lux in playground, open `Lux.xcworkspace` and build Lux.framework for any simulator first.

---

## Resources

- [Documentation (WIP)](https://luxyfy.me/lnk/docs)
- [Website](https://maxwell.design)
- [Press Release](https://luxyfy.me/lnk/PR)

### Learning

Install the Maxwell App and purchase a research license to its Full Source Code.  Some interesting features:

- All screens based in LUX DSL
- Firebase integration
- iOS + macCatalyst
- Sign in with Apple
- Push Notifications
- Local Storage
- Realtime Databse 
- Remote Configuration
- In-App Purchases
- Web Browsers
- Advanced Combine + SwiftUI
- way more!

The entire Maxwell App is based on a (flavored) MVVC pattern over Combine + SwiftUI. Don't miss the chance to look into one of the first large scale apps built on the SwiftUI era!

### Credits

- Mark Maxwell ([@eonfluxor](https://twitter.com/robertjpayne))
- Roots Rroy
- Van Jhazz
- Cosmos
- Adrian Juarez
- Humanized Robot

- [Multipeer Library by Wilson Ding](https://github.com/dingwilson/MultiPeer)

### License

LUX is released under the GNU GPL license. See LICENSE for details.

Contact `lux@maxwell.design` for flexible licensing options and other inqueries.
