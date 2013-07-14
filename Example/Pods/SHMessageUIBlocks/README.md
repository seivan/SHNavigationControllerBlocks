SHMessageUIBlocks
==========

Overview
--------
The blocks are automatically removed once the alert is gone, so it isn't necessary to clean up - Swizzle Free(™)

### API

#### [Init Mail](https://github.com/seivan/SHMessageUIBlocks#init-mail-1)

#### [Init Message](https://github.com/seivan/SHMessageUIBlocks#init-message-1)

#### [Properties Mail](https://github.com/seivan/SHMessageUIBlocks#properties-mail-1)

#### [Properties Message](https://github.com/seivan/SHMessageUIBlocks#properties-mail-1)


Installation
------------

```ruby
pod 'SHMessageUIBlocks'
```

***

Setup
-----

Put this either in specific files or your project prefix file

For all controllers

```objective-c
#import "SHMessageUIBlocks.h"
```

For just Mail

```objective-c
#import "MFMailComposeViewController+SHMessageUIBlocks.h"
```

For just Message

```objective-c
#import "MFMessageComposeViewController+SHMessageUIBlocks.h"
```

API
-----

### Init Mail

```objective-c
#pragma mark -
#pragma mark Init
+(instancetype)SH_mailComposeViewController;

```

### Init Message

```objective-c
#pragma mark -
#pragma mark Init
+(instancetype)SH_mailComposeViewController;

```


### Properties Mail

```objective-c
#pragma mark -
#pragma mark Block Defs

typedef void (^SHMailComposerBlock)(MFMailComposeViewController * theController,
                                    MFMailComposeResult theResults,
                                    NSError * theError);

#pragma mark -
#pragma mark Properties

#pragma mark -
#pragma mark Setters
-(void)SH_setComposerCompletionBlock:(SHMailComposerBlock)theBlock;


#pragma mark -
#pragma mark Getters
@property(nonatomic,readonly) SHMailComposerBlock SH_blockComposerCompletion;

```

### Block Definition Mail


### Properties Message

```objective-c
#pragma mark -
#pragma mark Block Defs

typedef void (^SHMessageComposerBlock)(MFMessageComposeViewController * theController,
                                       MessageComposeResult theResults);


#pragma mark -
#pragma mark Properties

#pragma mark -
#pragma mark Setters
-(void)SH_setComposerCompletionBlock:(SHMessageComposerBlock)theBlock;


#pragma mark -
#pragma mark Getters
@property(nonatomic,readonly) SHMessageComposerBlock SH_blockComposerCompletion;

```



Contact
-------

If you end up using SHMessageUIBlocks in a project, I'd love to hear about it.

email: [seivan.heidari@icloud.com](mailto:seivan.heidari@icloud.com)  
twitter: [@seivanheidari](https://twitter.com/seivanheidari)

## License

SHMessageUIBlocks is © 2013 [Seivan](http://www.github.com/seivan) and may be freely
distributed under the [MIT license](http://opensource.org/licenses/MIT).
See the [`LICENSE.md`](https://github.com/seivan/SHMessageUIBlocks/blob/master/LICENSE.md) file.
