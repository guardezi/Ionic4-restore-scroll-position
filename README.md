# [Ionic 4 beta] Restore scroll position

After returning to previous page in the lastest Ionic 4.0.0-beta.8, the page loses scroll position as explained here:
https://github.com/ionic-team/ionic/issues/14737

This simple example saves the scroll position in the page, and after returning into it the scroll is restored. 

<p align="center">
  <img src ="https://i.imgur.com/p5nCrfM.gif" />
</p>

## Save scroll position

```
this.content.getScrollElement().then(data => {
  console.log(data.scrollTop);
  this.scrollPosition = data.scrollTop;
});
```

## Restore scroll position

```
this.content.scrollToPoint(0, this.scrollPosition);
```

## Navigation forward and back in Ionic 4

You can find some navigation examples, like router.navigateByUrl, navCtrl.navigateForward, by HTML routerLink, etc.

## Copyright

Copyright © 2018 Joan Roig.
