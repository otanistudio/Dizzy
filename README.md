# Dizzy

I was way late on reading-up about [`IBInspectable`](https://developer.apple.com/library/ios/recipes/xcode_help-IB_objects_media/Chapters/CreatingaLiveViewofaCustomObject.html) and [`IBDesignable`](https://developer.apple.com/library/ios/recipes/xcode_help-IB_objects_media/Chapters/CreatingaLiveViewofaCustomObject.html), so I started playing around with them. One thing led to another, which led to this thing. Turns out they are pretty awesome time savers and I/we/you/me should use them more often! So, for those of you who want to learn, or are looking for a `UIActivityIndicatorView` that can take a custom image, here is…

### A Dizzying Custom Activity Indicator, Configurable through Interface Builder

A [`UIActivityIndicatorView`](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityIndicatorView_Class/) -inspired [`UIView`](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIView_Class/index.html#//apple_ref/occ/cl/UIView) that allows you to __set a custom image for the indicator__. It takes advantage of[`IBInspectable`](https://developer.apple.com/library/ios/recipes/xcode_help-IB_objects_media/Chapters/CreatingaLiveViewofaCustomObject.html) and [`IBDesignable`](https://developer.apple.com/library/ios/recipes/xcode_help-IB_objects_media/Chapters/CreatingaLiveViewofaCustomObject.html) attributes (available since XCode 6,) which allows you to configure this indicator with your custom image and preview it in Interface Builder — _including color changes_ —  without having to first compile and run the app.

## Using DizzyActivityIndicatorView

1. Drop a `UIView` into your storyboard and then change its class to `DizzyActivityIndicatorView`
2. You can then configure its image and `UIActivityIndicatorView`style attributes, like `isAnimating` and `hidesWhenStopped` 
    ![Dizzy Interface Builder Demo](https://cloud.githubusercontent.com/assets/517428/16718279/6fad2020-46d3-11e6-84be-8f5e5ca374ff.gif)

3. You can even change the color, and see it change in Interface Builder!

    ![Changing the Color](https://cloud.githubusercontent.com/assets/517428/16721667/dd9e3048-46f5-11e6-96e4-77193eaff904.gif)

4. The __DizzySample__ application target provides a concrete example of how to use this class.

    ![Dizzy Sample Application Demo](https://cloud.githubusercontent.com/assets/517428/16718482/4d6d981c-46d5-11e6-8bc5-78161ec476ab.gif)

## Installation

It's one file, so it's easiest to just drop `DizzyActivityIndicatorView.swift` into your XCode project via a clone+copy or even a submodule reference (but if you're really hunkering for some kind of dependency manager support, then file an issue and let's work together on it!)

## Thanks

Thanks to [@fabb](https://github.com/fabb) for this gist: <https://gist.github.com/fabb/007d30ba0759de9be8a3>, which helped to make adding color support an easy task.
