# Guidelines for taking good screenshots for technical documentation

## Resolution and file size

* Take screenshots on a machine with at least a 4k or Retina monitor
* Screenshots should not be larger than 200 KB, and preferably under 100 KB each. You can use TinyPNG or similar to reduce file size without reducing perceived quality

## Zooming and cropping

* Show a full window whenever possible - this keeps sizing consistent and helps the reader locate the correct portion of the UI to interact with
* If you're focusing on a smaller area and need to add more detail, then it's OK to zoom in on a specific element by using cropping. But keep in mind that often it might be harder for the user to orient themselves when you do this.

## Annotations and callouts

* Use red callouts unless the content of the screenshot contains too much red for the callout to be noticed (e.g. you need to outline a button that is also red.) Then pick one other colour that contrasts well (often Black or Blue), and consistently use that one wherever Red doesn't work.
* Generally use rectangles to call the readers attention to specific inputs or buttons
* If showing three or more separate steps in a single screenshot, add numbered callouts (1), (2), (3), etc to indicate the order steps should be taken in
* If interacting with a smaller part of the screen, add a red arrow to direct the reader's attention to the correct place in the screen
* Do not use too many annotations on a single screenshot (a matter of judgement, but often around 3-4 is the maximum before the shot starts looking very messy and over crowded)
* Be consistent where you put the annotations. E.g. if you are adding the numbered callouts inside and to the right of a rectangle, then try to do that for all screenshots in a project. Don't switch between adding them above/below/left/right of the thing you are indicating.

### Examples

* Do not leave space between a rectangle and what it is outlining. Generally 'hug' the thing you are outlining as tightly as possible.

![](https://i.ritzastatic.com/images/32cf92bd546c4d4e8b77fb6c94f5173e/correct-annotation-bounding.png)

### CleanshotX-specific recommendations

* If you are using CleanshotX, use the second thinnest line size for rectangles, arrows, and numbers

## Gifs and videos

* Gifs have problems regarding file size, but are the most portable and easiest to work with, as generally anywhere you can add an image you can also add a gif
* For long gifs, use mp4 or webm instead
* Generally avoid including sound in technical documentation (either system sounds, or microphone)

## Combining screenshots with text

* Put the text first, followed by the screenshot
* Do not put two screenshots in a row without text between them

## Finishing touches

* Add a browser frame and background colour with a tool like BrowserFrame
* Optimize the filesize with a tool like TinyPNG

## Captions

* Don't add captions unless there is a good reason too.
* If adding captions, you should try to convey more information than is obvious. For example, don't say "A graph showing language popularity over time"; rather say "Python has grown faster in popularity than other languages".

