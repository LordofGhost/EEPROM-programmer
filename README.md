# Arduino Nano EEPROM programmer for 28c256

<figure>
    <img src="/images/EEPROM-PROGRAMMER.jpg"
         alt="EEPROM-PROGRAMMER">
    <figcaption>**my selfmade EEPROM programmer**</figcaption>
</figure>

## The process

### Why I built it?

- I want to build a [6502](https://de.wikipedia.org/wiki/MOS_Technology_6502) computer and for this I need an EEPROM programmer. 

### Problems

- The [EEPROM](https://de.wikipedia.org/wiki/Electrically_Erasable_Programmable_Read-Only_Memory) I bought had SDP enabled. 

### Problem fixing (that did not work)

- I have tried to disable the SDP using the [datasheet](https://www.mouser.de/datasheet/2/268/doc0006-1108095.pdf) and direct port writes on the arduino nano. But I did not get the timing right.

- After that I found the project [TommyPROM](https://github.com/TomNisbet/TommyPROM/tree/master/unlock-ben-eater-hardware) in which the same is done as I tried myself, but I had no success with it either. Probably the [EEPROM](https://de.wikipedia.org/wiki/Electrically_Erasable_Programmable_Read-Only_Memory) was the problem.

### Conclusion

**Disabling SDP can be very annoying.**

To continue my [6502 project](https://github.com/LordofGhost/AB65G23) anyway I bought a [T46](https://de.aliexpress.com/item/1005004419320060.html?spm=a2g0o.order_list.order_list_main.5.bb4c5c5f8sayIM&gatewayAdapt=glo2deu) with which everything worked fine. When I deactivated SPD with the [T46](https://de.aliexpress.com/item/1005004419320060.html?spm=a2g0o.order_list.order_list_main.5.bb4c5c5f8sayIM&gatewayAdapt=glo2deu), my self-built EEPROM programmer also worked.

## Credits
This EEPROM programmer was developed by [Ben Eater](https://www.youtube.com/beneater) and all files can be found in [his repository](https://github.com/beneater/eeprom-programmer).