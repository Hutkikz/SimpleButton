# SimpleButton
Return a 1 once every time a button becomes pressed

 I'm an old button masher and I found that many of the button libraries did not react quickly or reliably enough for me. The ones that did utilized hysteresis but had other features or issues I didn't care for.

This simply returns a 1 every time the button becomes pressed. It reads the button at a set interval and uses a ring buffer to record the last 8 reads giving a maximum of 7 intervals. the debounce time for both press and release is determined by the number of intervals desired for each.

The default constructor is set for a 10ms interval and uses 1 interval(10ms) for the press debounce and 5 intervals(50ms) for the release debounce. This seems to work reliably for as fast as I can press a button.

There is also an overloaded constructor where you can set all 3 of these parameters. This is demonstrated in the example sketch.
