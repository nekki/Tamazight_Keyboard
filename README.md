Tamazight_keyboard:
===================
this project is a fork from [ekki/Tamazight_Keyboard](https://github.com/nekki/Tamazight_Keyboard) for adding (amazigh) latin keyboard layout for linux.
**Tifinaghe** is added by the project [l'IRCAM (Institut Royal de la Culture Amazighe du Maroc)](http://www.ircam.ma/)

Installing:
-----------
1. You have to download the archive file from [here](https://github.com/n-louahedj/Tamazight_Keyboard/archive/master.zip)
2. Unzip the archive file using this command:
  ```bash
  unzip Tamazight_Keyboard-master.zip
  ```
**The following steps need to be done as a root**
3. Copy the file symboles/dz to /usr/share/X11/xkb/symbols/
```bash
sudo cp Tamazight_Keyboard-master/symbols/dz /usr/share/X11/xkb/symbols/
```
4. Add this line `dz              Amazigh (Tamazgha)` in /usr/share/X11/xkb/base.lst just after `! layout`.
5. Do the same as in step 4 but for this file /usr/share/X11/xkb/evdev.lst
6. And add the following lines in /usr/share/X11/xkb/base.xml  after `<layoutList>` tag
```xml
    <layout>
      <configItem>
        <name>dz</name>
        
        <shortDescription>dz</shortDescription>
        <description>Amazigh (Tamazgha)</description>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>french</name>
            
            <shortDescription>fr</shortDescription>
            <description>French (Tamazgha)</description>
            <languageList>
              <iso639Id>fra</iso639Id>
            </languageList>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>amazigh-latin</name>
            
            <shortDescription>dz</shortDescription>
            <description>Amazigh (Tamazgha, Amazigh latin caracters)</description>
            <languageList>
            <iso639Id>fra</iso639Id>
            </languageList>
          </configItem>
        </variant>
      </variantList>
    </layout>
```
7. And add the following lines in /usr/share/X11/xkb/evdev.xml  after `<layoutList>` opening tag
```xml
<layout>
      <configItem>
        <name>dz</name>        
        <shortDescription>dz</shortDescription>
        <description>Amazigh (Tamazgha)</description>        
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>french</name>
            <description>French (Tamazgha)</description>
	          <languageList>
              <iso639Id>fra</iso639Id>
            </languageList>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>amazigh-latin</name>
            <description>Amazigh (Algeria, Amazigh latin caracters)</description>
          </configItem>
        </variant>
      </variantList>
    </layout>
```
8. Now you can go to the layout setting in your desktop manager and add or change your layout to `Algeria, Amazigh latin caracters`, and enjoy.

Recommandations:
----------------
Copy the files that we mofitied befor doing any modifications.
