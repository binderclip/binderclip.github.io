---
title: 微信“网络出错，轻触屏幕重新加载:-xxxx”错误码含义
permalink: wechat-webview-error-code
date: 2018-05-02 20:51:19
categories: 💻dev
tags:
---

微信 iOS 客户端有时候打开网页会提示“网络出错，轻触屏幕重新加载:-xxxx”，比如下面的 -1007

![wechat error](https://qn.cdn.cliiip.com/imgs/u/b22f6db5-e899-41b4-bdbe-a8cc01f5543a.png)

错误码实际是微信客户端把 CFNetworkErrors 的错误显示码出来了，错误码的含义如下，知道了之后方便 debug

```
kCFURLErrorUnknown   = -998,
kCFURLErrorCancelled = -999,
kCFURLErrorBadURL    = -1000,
kCFURLErrorTimedOut  = -1001,
kCFURLErrorUnsupportedURL = -1002,
kCFURLErrorCannotFindHost = -1003,
kCFURLErrorCannotConnectToHost    = -1004,
kCFURLErrorNetworkConnectionLost  = -1005,
kCFURLErrorDNSLookupFailed        = -1006,
kCFURLErrorHTTPTooManyRedirects   = -1007,
kCFURLErrorResourceUnavailable    = -1008,
kCFURLErrorNotConnectedToInternet = -1009,
kCFURLErrorRedirectToNonExistentLocation = -1010,
kCFURLErrorBadServerResponse             = -1011,
kCFURLErrorUserCancelledAuthentication   = -1012,
kCFURLErrorUserAuthenticationRequired    = -1013,
kCFURLErrorZeroByteResource        = -1014,
kCFURLErrorCannotDecodeRawData     = -1015,
kCFURLErrorCannotDecodeContentData = -1016,
kCFURLErrorCannotParseResponse     = -1017,
kCFURLErrorInternationalRoamingOff = -1018,
kCFURLErrorCallIsActive               = -1019,
kCFURLErrorDataNotAllowed             = -1020,
kCFURLErrorRequestBodyStreamExhausted = -1021,
kCFURLErrorFileDoesNotExist           = -1100,
kCFURLErrorFileIsDirectory            = -1101,
kCFURLErrorNoPermissionsToReadFile    = -1102,
kCFURLErrorDataLengthExceedsMaximum   = -1103,
```

## refs

- [ios - Undocumented NSURLErrorDomain error codes (-1001, -1003 and -1004) using StoreKit - Stack Overflow](https://stackoverflow.com/questions/6778167/undocumented-nsurlerrordomain-error-codes-1001-1003-and-1004-using-storeki/7492235)
