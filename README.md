variants compilering source assembler:
    First variant:
    1.avra <file.hex>
    https://www.instructables.com/id/Command-Line-AVR-Tutorials/

    Second variant:
    1.avr-gcc -mmcu=atmega328p -o out_file.elf source_file.S     
    2.avr-objcopy -j .text -j .data -O ihex out_file.elf out_file.hex
    http://polprog.net/blog/asm/

    how to install var-gcc:
        http://www.linuxandubuntu.com/home/setting-up-avr-gcc-toolchain-and-avrdude-to-program-an-avr-development-board-in-ubuntu

Flesh microcontroller:
sudo avrdude -v -p m328p -c arduino -b 115200 -P /dev/ttyACM0 -C /home/georg/avr/tools/avrdude-6.3/avrdude.conf -D -Uflash:w:/home/georg/avr/hello.hex
http://microsin.net/programming/avr/starting-out-with-avrdude.html
