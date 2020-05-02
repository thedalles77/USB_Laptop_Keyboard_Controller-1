# USB_Laptop_Keyboard_Controller
This was forked from Marcel's repo so that I could add support for the Teensy 3.2 and 4.0. I don't know how to modify the program to eliminate the single quotes around every key code. If anyone can help with this, let me know at thedalles77@gmail.com


1. Load the "Matrix_Decoder_LC, _3p2, or 4p0" Arduino code into your Teensy. 
2. Load the Keyboard_with_number_pad or Keyboard_without_number_pad text file into an editor like Notepad++. 
3. Put the cursor to the right of the first key in the list.
4. Edit the text file if it's missing any of your keyboards keys. The key codes must be from https://www.pjrc.com/teensy/td_keyboard.html  
5. Connect your keyboard FPC cable to the FPC connector.
6. Hook up the USB cable from your computer to the Teensy.
7. Wait about 20 seconds, then push each key listed in the text file. You should see pin number pairs as you push a key.
8. If a listed key is not on your keyboard, use your computer mouse or arrow keys to jump down to the next line.
9. if you want to assign Media keys (a key event associated with the FN-key), push the media key (do not push the FN key). Add "FN" between the media keyname and the pins. Make sure that there is whitespace between the values. 
7. Save the finished key list text file.
8. Make sure the key list text file is in the same folder as the matrixgenerator.py program, then execute the .py program.
9. The program will create a text file that gives the following:
    - The FPC connector pins that are inputs (columns) and the pins that are outputs (rows) in the key matrix.
    - The pins are translated to Teensy I/O numbers so you can add them to your USB keyboard code.
    - Unfortunately the Python program puts single quotes around every item in the Normal, Modifier, and Media arrays.
    - Use an editor to remove all single quotes, then copy these 3 arrays to your USB keyboard code.
The detailed instructions for modifying the USB keyboard code can be found here: https://github.com/thedalles77/USB_Laptop_Keyboard_Controller/blob/master/Example_Keyboards/Instructions%20for%20modifying%20the%20Teensyduino%20LC%20code.pdf
 
