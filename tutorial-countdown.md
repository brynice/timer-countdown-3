# START- Title
## Section 1
Go to the BASIC (blue squares)" section and drag the "on start" block. 
Next, go to the VARIABLES  (four red lines) and click on the "make a variable" button.
Name your variable "countdown" and click enter. Then drag the "set countdown to 0" block to the inside of the 
" on start" block. Change the number 0 to a 10.
```blocks
let countdown = 0
countdown = 10
```
## Section 2 
Go to the INPUT (pink circle) section and drag an "on button A" block.
```blocks
input.onButtonPressed(Button.A, function () {
```
## Section 3
Go to the LOOPS (green arrow) section and drag a "repeat" block to the inside of the pink "on button A" block. 
Change the number from a 4 to a 12.
  ```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 12; index++) {
    ```
## Section 4
Go to the BASIC (blue) section, click on the "show number" block and dragg it 
to the inside of the green "repeat" block. From the VARIABLES section 
click on the red "countdown" block and drag it to the "0" on the "show number" block.
Go back to the BASIC section, click on the "pause (ms)" section and drag it 
below the "show number" block. Change the 100 to 1000. 
 ```blocks
 input.onButtonPressed(Button.A, function () {
     for (let index = 0; index < 12; index++) {
        basic.showNumber(countdown)
        // 1000 milliseconds = 1 second
        basic.pause(1000)
        ```
## Section 5
Go to the MUSIC (red headphones) section and click on the
"Play tone 'Middle C". Change the beat to 1/2 a beat. 
```blocks
input.onButtonPressed(Button.A, function () {
     for (let index = 0; index < 12; index++) {
        basic.showNumber(countdown)
        // 1000 milliseconds = 1 second
        basic.pause(1000)
        // Play a beep sound (frequency 262Hz) for half a beat
        music.playTone(262, music.beat(BeatFraction.Half))
        ```
## Section 6
Go the VARIABLES section and click on the "change countdown" block. 
Drag the "change countdown" block below the "play tone" block. Change the count 
from 1 to -1 (we are counting down).
```blocks
input.onButtonPressed(Button.A, function () {
     for (let index = 0; index < 12; index++) {
        basic.showNumber(countdown)
        // 1000 milliseconds = 1 second
        basic.pause(1000)
        // Play a beep sound (frequency 262Hz) for half a beat
        music.playTone(262, music.beat(BeatFraction.Half))
        countdown += -1
        ```
## Section 7
Go to the LOGIC (teal arrows) section, click on the "if true.. then" block.
Dragg the block under 
```blocks
input.onButtonPressed(Button.A, function () {
     for (let index = 0; index < 12; index++) {
        basic.showNumber(countdown)
        // 1000 milliseconds = 1 second
        basic.pause(1000)
        // Play a beep sound (frequency 262Hz) for half a beat
        music.playTone(262, music.beat(BeatFraction.Half))
        countdown += -1
        if (countdown < 0) {
        ```
```blocks
input.onButtonPressed(Button.A, function () {
     for (let index = 0; index < 12; index++) {
        basic.showNumber(countdown)
        // 1000 milliseconds = 1 second
        basic.pause(1000)
        // Play a beep sound (frequency 262Hz) for half a beat
        music.playTone(262, music.beat(BeatFraction.Half))
        countdown += -1
        if (countdown < 0) {
            // Reset the countdown to 10 after reaching 0
            countdown = 10
            ```
