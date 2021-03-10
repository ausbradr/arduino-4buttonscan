# arduino-4buttonscan
SIMPLE 4 button input test for Arduino. In two formats (stop everything and wait keypress, or wait for keypress while doing other stuff)


I wanted a nice simple solution to wait and check for keypresses before proceeding. Very handy for a menu driven system. Speaking of which, I have one I'm putting up to github when I get it working how I want. 

As someone with pretty basic coding experience, I find this easy to follow and it works how I want it to. I hope it serves you well too. 

When you put this code into your sketch from the main code file I'm providing, you can check for keypresses in two methods:

keypadcheckloop()
This is a self contained function that will do everything you need and pause your program until a key is pressed. Nothing else in void loop() will run until a key is pressed. Ideal for menus. Once a key is pressed, the loop exits, and you can test the value stored in keypadtotal to decide on how your program will flow onwards. 

keypadcheckonce()
I've included another demo that demonstrates this technique. It's simple. You call it, it checks the keypad once, then returns flow straight back to your program. Make a loop of your own that repeatedly calls this function. You can also do other stuff (such as updating neopixel LEDS or playing a chiptune). So this one is aimed at multitasking while also accepting user input. 

By default, we will be using 4 buttons, on pins 2,3,4,5 on an arduino uno. They will be pulled DOWN to ground with a 10k resistor. Buttons will be considered "HIGH" when those buttons are shorted to +5V. You can modify this easily to your needs, but a simple pulldown arrangement on a breadboard is all you need to get started and testing. 

CLEANING UP THE CODE:
If you're copying / pasting the demo in your code, I've been overzealous with the comments / Serial routines to help the absolute novice user. There's also a delay I've introduced before the scan begins just to make serial readout easier. These can all be removed for your project. I'll also include a barebones version that'll have minimal comment and no serial routines. You can drop it straight into your project. 

For complete newbies, it's good practice to use the code that has all the serial routines. It makes life easier when you can visually watch program flow. Learn to love the serial monitor. 


I hope this helps you as much as it will help me. Good luck with your project. I'm happy to help but bare in mind I'm pretty busy with my day job so replies may take a while. 
