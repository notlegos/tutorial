# Invention Lab Tutorial #1

```package
pxt-nezha=github:elecfreaks/pxt-nezha
pxt-PlanetX=github:elecfreaks/pxt-planetx
```

## Case 6: The Dancing Robot
After turning on Microbit, show a picture of your choice :)<br>
When button A is pressed, set motor speed percentage somewhere between 0-100 (hint: start low such as 10% in case things go wrong) <br>
When button B is pressed, stop all motors! (it is a common mistake to forget to program a "stop" condition)<br>

```blocks
input.onButtonPressed(Button.A, function () {
    neZha.setMotorSpeed(neZha.MotorList.M1, 100)
})
input.onButtonPressed(Button.AB, function () {
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.Entertainer), music.PlaybackMode.InBackground)
})
input.onButtonPressed(Button.B, function () {
    neZha.stopMotor(neZha.MotorList.M1)
})
```


```ghost
input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 4; index++) {
        neZha.setServoAngel(neZha.ServoTypeList._180, neZha.ServoList.S1, 90)
    }
```

## EXIT CONFIRMATION
Are you sure you're done? 
Make sure to double check your code for mistakes!

## Don't press "Done" unless you're truly done! @showdialog
