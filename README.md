NSMutableAttributedString+HTML
=============

A category on NSMutableAttributedString to add HTML features for UIKit that normally only available in AppKit
The OSX documentation is [here](https://developer.apple.com/library/mac/documentation/Cocoa/Reference/ApplicationKit/Classes/NSAttributedString_AppKitAdditions/)

Originally extracted from [Push](https://github.com/PushOCCRP/)

Usage
------------

```Objective-C
#import "NSMutableAttributedString+HTML.h"
```

```Objective-C
NSString * htmlString = @"This is a <a href=\"http://www.example.com\">sample</a> html file";
NSMutableAttributedString * bodyAttributedText = [[NSMutableAttributedString alloc]
                                                   initWithHTML:[htmlString dataUsingEncoding:NSUTF8StringEncoding]
                                                   documentAttributes:nil];

NSString * htmlStringWithoutBaseURL = @"This is a <a href=\"/test/url\">sample</a> html file";
NSMutableAttributedString * bodyAttributedText = [[NSMutableAttributedString alloc]
                                                   initWithHTML:[htmlStringWithoutBaseURL dataUsingEncoding:NSUTF8StringEncoding]
                                                   baseURL:@"http://www.example.com"
                                                   documentAttributes:nil];
```

Contact
--------------
Christopher Guess [cguess@gmail.com](mailto:cguess@gmail.com)