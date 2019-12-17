# iPhone Safari Fullscreen Softlock - PoC

Proof of Concept for fullscreen video softlock in iPhone Safari.

### The Bug:

When listening on video pause, we can automatically start playing the video again, and at the same time request fullscreen. When a user tries to exit video fullscreen, the video is automatically paused, but we automatically start playing the video again, and also put the video back into fullscreen. This makes it almost impossible to close or leave the page and only reliable way of leaving the page or closing the tab is by force quiting Safari from the App Switcher.

It is worth noting that this does not work without starting to play the video while you make the video go fullscreen, nor can you cancel the exit fullscreen event.

### Proof of Concept:

Visit [index.html](https://kristianvld.github.io/iphone-safari-fulscreen-softlock/) on an iPhone and click anywere on the page to start the video, then try to exit or close the tab. You can

### Example Recording:

![Demo GIF](example.gif)

---

This has been tested on iPhone 7 and iPhone 10 using iOS 13.3.

Similar behaviour exists on other iOS browsers such as Firefox for iPhone.
