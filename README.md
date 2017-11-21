# SymmeTri-Keyboard-Layout

![A basic variant of SymmeTri for 104 US-standard keyboard](https://github.com/WesleyBlancoYuan/SymmeTri-Keyboard-Layout/blob/master/preview/preview-ANSI104-bigenter-deadkey-lights.png)
                              (A basic variant of SymmeTri for 104 US-standard keyboard)

This full view is created via [keyboard-layout-editor on Gist](http://www.keyboard-layout-editor.com).

**SymmeTri**, a symmetrical keyboard layout which supports the three most spoken languages in the world: **Chinese, English and Spanish**. The name "SymmeTri" combines **"Symme"** and **"Tri"**, the first part means "Symmetrical", and the second part "Tri", as prefix, meaning "Three".

### 1. Normal use vs. Programming friendly
It has two version: "Normal" and "Programming". The major difference between these two are in the position of keys on the first line of alphanumerical area: "Normal" has number keys 0-9 on the un-shift state, meaning that you enter numbers solely, and enter symbols with shift pressed; while "Programming" has it reversed: you enter symbols without press <kbd>Shift</kbd>, and numbers are typed with <kbd>Shift</kbd> press. This is to ease the input of these symbols, whose use is more than common in any programming language.

### 2. Symmetrical layout

#### 2.1 Number/Symbol keys line
About these symbols, another thing to stress is that they are all in pairs, and each pair is symmetrically organized, so that we can enter the left half with left hand, and the right half with right hand, with the same finger. These simbols include:
 - `{` and `}` (with little finger)
 - `[` and `]` (with ring finger)
 - `(` and `)` (with middle finger)
 - `<` and `>` (with index finger, normal position)
 - `/` and `\` (with index finger, extend to the middle)

And, the corresponding numbers: 
 - `1` and `0`
 - `2` and `9`
 - `3` and `8`
 - `4` and `7`
 - `5` and `6`

#### 2.2 Main alphanumeric area
And, other symbols are also symmetrically layouted to balance two hands' burden. We know that in legacy QWERTY layout, symbols are mainly located at the right side, where only the weakest finger can reach; so the right hand needs to handle more symbols than the left hand, plus manipulating the mouse if you are a right-hander. This layout tries to solve this problem partially by moving 3 heavily used keys to the middle, so that left hand can type them too, with the most strong finger, the index. Also, for Spanish typers, two dead keys are controlled by the left index finger, so it can ease more the work done by right hand.

#### 2.3 CapsLock, Enter and Shift
If you take a look into the legacy QWERTY layout, you may begin to see something ridiculous: on the home line where our fingers initially rest, the position at the both edge of main area are occupied by two different keys: on the left, <kbd>CapsLock</kbd>, and on the right side, <kbd>Enter</kbd>. <kbd>LShift</kbd> and <kbd>RShift</kbd>, <kbd>LCtrl</kbd> and <kbd>RCtrl</kbd>, on the other side, are located below. So, the little finger must lower to an unnatural position to press them, which are certainly more heavily used than <kbd>Enter</kbd> and <kbd>CapsLock</kbd>. So I decide to move <kbd>Shift</kbd> to the home line, by switching <kbd>LShift</kbd> with <kbd>CapsLock</kbd>, and <kbd>RShift</kbd> with <kbd>Enter</kbd>, and after that, all start to make sense again: you just extend both little fingers to press the common <kbd>Shift</kbd> key to the left/right side, symmetrically and without lowering, and you can type in upper case.
The reasons why I don't switch <kbd>CapsLock</kbd> and <kbd>Enter</kbd> with <kbd>Ctrl</kbd>, are two:
 - Keys at the corners are more likely to be pressed accidently by you or by others, e.g., by your kid or your cat, so they should not be crucial enough to do things solely. <kbd>Ctrl</kbd> do not trigger any input event when pressed alone, but <kbd>Enter</kbd> and <kbd>CapsLock</kbd> are more likely to trigger "bigger" things.
 - We get used to "<kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>Z</kbd>/<kbd>X</kbd>/<kbd>C</kbd>/..." combinations, and when doing it, we just reach for **the key at the corner** to do it by convention, without realizing what keys they are. No need to change this behaviour to make my keyboard layout harder to learn.

### 3. Language support
#### 3.1 English
It supports all English letters and the following punctuations in English:
```
{}[]()<>/\?!'"=+`^-_~&%@;:|$#*,.
```
#### 3.2 Spanish
With the help of MSKLC 1.4 in Windows(and `keymap` in Linux), apart from all regular letters in Spanish, we can type special characters with my keyboard layout, such as:
```
á ó é í ú Á Ó É Í Ú
(ä ö ë ï) ü (Ä Ö Ë Ï) Ü
ñ Ñ ç Ç
(ý Ý ÿ)
```
(those in parenthesis are not needed in Spanish, just defined for example)

Euro sign:
```
€
```
And other punctuations only in Spanish:
```
·¬¡¿ºª´¨«»
```
#### 3.3 Chinese
We can type Chinese with IMEs like *Microsoft Pinyin* or services like `ibus`, `fcinx`, etc. As long as we have all the 26 letters in English, Chinese input with Pinyin is not a problem. And, for punctuations, apart from the English ones, we have(all full-lengthed):
```
？！{［（《／‘’“”、》）］｝……——～％｜
```
In Windows, because these punctuations input event are mapped onto virtual keys, they can be obtained directly by pressing the corresponding virtual keys. For example, `……` was mapped to `VK_OEM6`, and in my keyboard layout, this VK code corresponds to the key between `T` and `Y`. The VK code mapping can be changed directly in the `.klc` files used by MSKLC. In Linux this is controlled by key-mapping and IME. Check the `.klc` file under `Windows` to learn more.

### 4. Adaptality: more of a framework than a layout
People may have learn a non-legacy layout like Dvorak, and when they see this, they may think: "Why do I have to learn a new one?" No, you really don't have to. 

If you just don't want to learn a new keyboard layout other than QWERTY, you just move your right hand one column to the right, and you are done: no more learning needed! And a little more time to remember the symbol keys' position, but that's easy: it took me 2 hours to get familiar to all keys. No more.

Those who are already masters of Dvorak/Colemak, etc., what I want to say is: **you can adapt my keyboard layout to create one of yourself, because SymmeTri allows you to seamless transfer from your favourite layout to it, as long as yours only changes the letter keys' position**. For example, Dvorak puts `{` and `}` on the QWERTY line, so it is a little harder, but Colemak does not change as much symbols' positions, so we can easily combine Colemak into SymmeTri. For example, it took me 5 minutes to complete this:
![SymmeTri-with-Colemak](https://github.com/WesleyBlancoYuan/SymmeTri-Keyboard-Layout/blob/master/preview/preview-104-smallenter-deadkey-lights-COLEMAK.png)

I think the idea of 1) symmetry and 2) including the most spoken languages in the world are the keys of my keyboard layout. I invent it to express my idea about languages and symbols:
 - Symmetry is one of the most used ways to layout elements in the design of everything, and, maybe the most natural one, because all parts of our body are symmetrical, at least judging from outside. So it is easy to remember. Now, using this layout, it has become hard for me to go back to the QWERTY layout: why `/` is at the right lower corner while `\` is at the right most, on the home line? 
 - Chinese, English and Spanish are the three languages I speak, and they are the top 3 languages most spoken of the world(judging from the number of speakers, the number of countries and influence in real life and on Internet). In the 21st century, I think we will have more and more people speaking more than one, two or even three languages; so current keyboard layouts are not for them: switching from one to another every now and then are far from satisfying.

So here I only establish one example and two principles: 1) it is better to be symmetrical regarding to symbols; 2) it should contain common symbols in English and other composing languages, as many as possible. Based on the principles, we can:
 - Rearrange existent layouts in the symmetrical way, like Dvorak, Colemak, or AZERTY, or even JCUKEN.
 - Invent more keyboard layout to include more than one language, like a Russian-Polish-English JCUKEN layout, or French-Italian-German AZERTY layout.



### 5. Implementation and configuration

 With different software/registry tweak, it can be used in Windows/Linux/MacOX. 
  - Windows: Microsoft Keyboard Layout Controller 1.4 (aka [MSKLC 1.4](https://www.microsoft.com/en-us/download/details.aspx?id=22339)) and Registry Tricks to swap Function keys. MSKLC 1.4 stays compatible with Windows 10 with 2017 Autumn Creator Update. 
  - Linux: change files
  - MacOX: [Ukelele](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=ukelele) or [Karabiner](https://pqrs.org/osx/karabiner/index.html). For problems of not seeing the newly created keyboard layout of Ukelele, refer to [this link](https://superuser.com/questions/665494/how-to-make-a-custom-keyboard-layout-in-os-x).
 
 
WesternGun, 13/11/2017

