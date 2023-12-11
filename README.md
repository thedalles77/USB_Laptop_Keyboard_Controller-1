# This was forked from Marcel Hillesheim's USB_Laptop_Keyboard_Controller repo and then the Teensy 4.1 and 2.0++ were added

1. Load the "Matrix_Decoder_LC, _3p2, 4p0, 4p1, or 2.0++" code into your Teensy.
2. Load the Keyboard_with_number_pad or Keyboard_without_number_pad text file into an editor like Notepad++.
3. Put the cursor to the right of the first key in the list.
4. Edit the text file if it's missing any of your keyboards keys. The key codes must be from [https://www.pjrc.com/teensy/td_keyboard.html](https://www.pjrc.com/teensy/td_keyboard.html)
5. Connect your keyboard FPC cable to the FPC connector.
6. Hook up the USB cable from your computer to the Teensy.
7. Use your mouse to set the cursor to the right of the very first key in the list. Wait about 20 seconds and make sure no pin numbers are displayed.
8. If numbers are displayed before pushing any keys, there is a short that must be fixed.
9. Push each key listed in the text file. You should see pin number pairs as you push a key.
10. If a listed key is not on your keyboard, use your computer mouse or arrow keys to jump down to the next line.
11. if you want to assign Media keys (a key event associated with the FN-key), push the media key (do not push the FN key). 
12. Save the finished key list text file.
13. Make sure the key list text file is in the same folder as the matrixgenerator.py program, then execute the Python 3 program.
14. The program will create a text file that gives the following:
    - The FPC connector pins that are inputs (columns) and the pins that are outputs (rows) in the key matrix.
    - The pins are translated to Teensy I/O numbers so you can copy and paste them into your USB keyboard code.
    - Copy and paste the 3 arrays into your USB keyboard code.
The detailed instructions for modifying the USB keyboard code can be [found here](https://github.com/thedalles77/USB_Laptop_Keyboard_Controller/blob/master/Example_Keyboards/Instructions%20for%20Marcels%20Code.pdf).
