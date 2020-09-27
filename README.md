# Uppsala Makerspace Wanhao Duplicator i3 Firmware

Detta är mjukvaran som kör på vår 3D-skrivare av märket Wanhao Duplicator i3 (inte plus). Det är en fork av Marlin Firmware, med en egen konfiguration. För att uppgradera till en senare version, merga in senaste ändringarna från Marlin repot och anpassa konfiguration efter eventuella förändringar.

**OBS:** Bootloader är redan installerat (med hjälp av en Arduino as ISP), så man behöver bara koppla skrivaren via USB för att flasha nytt firmware.

1. Checka ut eller ladda ner github-projektet.
1. Installera och öppna Visual Studio Code
1. Installera extension PlatformIO IDE
1. Installera extension Auto Build Marlin
1. I VS Code, File/Open Folder. Peka på github-projektet (roten, inte Marlin-mappen)
1. Öppna extension Auto Build Marlin i vänstermenyn. Tryck ikonen "Marlin: Build"
1. Tryck Build bredvid "sanguino1284p".<br />
**OBS:** Om du får errors på grund av för långt filnamn, kan du behöva flytta github-mappen högre upp i mappstrukturen, typ till roten. Kanske behöver du ändra temp-mapp på din användare till en kortare sökväg också.
1. Koppla in 3D-skrivaren med ström och koppla till datorn via USB. Starta 3D-skrivaren med strömbrytaren.
1. I VS Code, Tryck Marlin: Upload i Auto Build Marlin.
Koden kommer att kompileras igen, och sedan laddas upp till skrivaren via USB. När allt är uppladdat kommer den läsa allt från skrivaren för att verifiera att skrivningen blev korrekt.
1. När firmware är flashat, så kan du behöva köra "Initialize EEPROM" på skrivaren för att ersätta sparade inställningar i skrivaren från default-inställningarna i firmware (annars kommer gamla värden/inställningar ofta gälla, t.ex e-steps). Detta gör du genom att i skrivarens meny välja "Configuration/Advanced Settings/Initialize EEPROM", tryck sedan "Init". 

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
