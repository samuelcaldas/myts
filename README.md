# kindle-myts

This is a terminal for Kindle devices based on [myts](http://info.iet.unipi.it/~luigi/kindle/). It contains various fixes and preferences so that it is convenient to use as a primary display device.

This fork uses statically linked musl as libc. This way, the development is very easy: just compile it on a Raspberry Pi and then copy the resulting binary to the device.

The tree also contains a prebuilt binary so you don't need to compile it yourself if you don't want to hack the code.

## Features

- Supports up to three terminals that can be opened with Launchpad
- Supports UTF8 and 8bit encodings
- Configurable keyboard mapping and symbols
- Customizable fonts and colors

## Installation

To install kindle-myts, you need to have Launchpad installed on your Kindle device. Then, follow these steps:

1. Download or clone this repository to your computer.
2. Copy the `myts` folder to your Kindle's `launchpad` folder.
3. Copy the `myts` binary file from `linux` folder to your Kindle's `/mnt/us/myts` folder (create it if it doesn't exist).
4. Restart Launchpad by pressing Shift Shift Space on your Kindle keyboard.

## Usage

To open a terminal, press Shift T followed by one of these keys:

- T: opens terminal 1, or returns to it if already open
- Y: opens terminal 2, or returns to it if already open
- U: opens terminal 3, or returns to it if already open
- A: kills myts

To exit from a terminal, press "Left<" (page back on the top left; this is configurable).

The keyboard is mapped as follows:

Menu:
F1 F2 F3 F4 F5 F6 F7 F8 F9  F10
`  %  ^  <  >  [  ]  =  F11 F12
\t ;  ,  (  )  {  }

Back:
!  @  #  $  %  ^  &  *  (   )
'  +  #  -  _  (  )  &  !   ?
~  $  |  /  \  "  '  :

The mapping of the Symbols keyboard (Back), can be configured by the option Symbols in myts.ini

## Configuration

You can customize various aspects of kindle-myts by editing the `myts.ini` file in `/mnt/us/myts` folder. Some of the options are:

- FontFile: specifies the font file for regular text (in hex format)
- BoldFontFile: specifies the font file for bold text (in hex format)
- Encoding: specifies the character encoding for input and output (UTF8 or an iconv format)
- Colors: specifies the foreground and background colors for normal and inverted text
- ExitKey: specifies which key exits from a terminal session

For more details, see `config.h` file in `linux` folder.

## Credits

This program is based on kiterm by Luigi Rizzo, with work by mobileread users PoP, Xqtftqx and dsmid.

The regular font is GNU unifont (with characters of width 16 removed) and the bold font is the 8x13B font from http://www.cl.cam.ac.uk/~mgk25/ucs-fonts.html Fonts can be converted from bdf to hex format by using bdf2hex perl script included in this repository.

## License

This program is licensed under GNU General Public License v3.0. See `LICENSE` file for more information.

Origem: conversa com o Bing, 19/03/2023(1) Getting started with writing and formatting on GitHub. https://docs.github.com/articles/markdown-basics Acessado 19/03/2023.
(2) Basic writing and formatting syntax - GitHub Docs. https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax Acessado 19/03/2023.
(3) About READMEs - GitHub Docs. https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes Acessado 19/03/2023.
