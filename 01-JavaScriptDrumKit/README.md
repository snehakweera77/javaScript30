#01 - Drum Kit
The exercise was to make a page that has a range of keyboard keys displayed and when a keyboard key was pressed, a sound was to be played and a visual effect was to take place to notify which key was pressed. The name of the sound played also had to be written underneath each displayed keyboard key
##Notes

We make use of two new concepts of HTML5:

    The HTML data-* attribute allows us to store custom data on any HTML element. Each div.key and audio element have a data-key attribute that binds them together.
    The audio tag offers an API that makes simpler to reproduce audio files in the browser.

##Pseudocode:

````
    if keyboard key is pressed
        initialize audio variable to audio element from html with same keycode as pressed key on keyboard
        initialize key variable to div element from html with same keycode as pressed key on keyboard
        initialize keys variable to all div elements from html that have class of 'key'

    if variable 'audio' doesn't contain an html audio element
        stop the program

    reset audio element's time to 0 to allow successive audio play when same keyboard key is pressed repeatedly
    play audio

    change background color of page to any random color

    add class of 'playing' to div element contained in variable 'key' for CSS transition(animation) of that element
    for each value in array of div elements contained in variable 'keys'
        add an event listener to remove transition class of 'playing' when transition ends

    add an event listener to browser window to execute the above steps when akeyboard key is pressed
    ```

````
