[![](https://img.shields.io/cocoapods/v/KingfisherExtension.svg?style=flat)](http://cocoadocs.org/docsets/KingfisherExtension)

# KingfisherExtension

KingfisherExtension base on [Kingfisher](https://github.com/onevcat/Kingfisher). Remake image before caching by style.

![](http://ww4.sinaimg.cn/large/006tNc79jw1f5l757g4qoj30af0ijdie.jpg)

## Requirements

iOS 8.0

Swift 2.0

## Usage

1. Make your Transformer conform ImageReducible protocol.

	``` swift
  struct Transformer: ImageReducible {
    let URLString: String
    let style: ImageStyle
  }
	```

2. And, set transformer for your imageView

	``` swift

  let round: ImageStyle = .RoundedRectangle(size: CGSize(width: 60.0, height: 60.0), cornerRadius: 16.0, borderWidth: 0)
  let transformer = Transformer(URLString: URLString, style: round)

  imageView.kfe_setImage(byTransformer: transformer)

	```

Check the demo for more information.

## Installation

### CocoaPods

```ruby
pod 'KingfisherExtension', '~> 0.3.2'
```

## Contact

Contact me on [Twitter](https://twitter.com/Limon______) or [Weibo](http://weibo.com/u/1783821582) . If you find an issue, just open a ticket on it. Pull requests are warmly welcome as well.

## License

KingfisherExtension is available under the MIT license. See the LICENSE file for more info.


