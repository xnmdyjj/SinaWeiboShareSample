This project based on https://github.com/doubleencore/DETweetComposeViewController

##What is it?
DESinaWeiboComposeViewController is a sina weio share controller. Looks like as the tweet share Sheet in iOS 5.

##How to use it?

1.Add your sina weibo appkey and secret in Constants.h

```
#import "DESinaWeiboComposeViewController.h"
...
DESinaWeiboComposeViewControllerCompletionHandler completionHandler = ^(DESinaWeiboComposeViewControllerResult result) {
           switch (result) {
               case DESinaWeiboComposeViewControllerResultCancelled:
                   NSLog(@"Sina Weibo: Cancelled");
                   break;
               case DESinaWeiboComposeViewControllerResultDone:
                   NSLog(@"Sina Weibo: Sent");
                   break;
           }
           
           [self dismissModalViewControllerAnimated:YES];
       };
DESinaWeiboComposeViewController *sinaWeiboViewComposer = [[DESinaWeiboComposeViewController alloc] init];
self.modalPresentationStyle = UIModalPresentationCurrentContext;
[sinaWeiboViewComposer setInitialText:@"Look on this"];
[sinaWeiboViewComposer addImage:[UIImage imageNamed:@"share.png"]];
sinaWeiboViewComposer.completionHandler = completionHandler;
[self presentViewController:sinaWeiboViewComposer animated:YES completion:^{ }];

[sinaWeiboViewComposer release];
```

## What does it look like?
![DESinaWeiboComposeViewController](https://raw.github.com/xnmdyjj/SinaWeiboShareSample/master/SinaWeiboShareSample/share.png) 
