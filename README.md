# Instructions to configure cs2 properly.
 In short, the idea is to have a single file (autoexec.cfg) containing all possible keybuttons, settings, crosshair etc. 
 This file is then read each time cs2 is launched.
 The effect is the same as if the lines in the file 'autoexec.cfg' were manually copy-pasted to the console window.
 Therefore, all changes should be done in the file 'autoexec.cfg' and the file should be located in a place where cs2 can find it.


## Step 1: Make changes to the autoexec.cfg file
Begin by making changes to the file. For instance, if you want to bind the flash grenade to something other than the f-button, you would change line 16 from the autoexec.cfg file. Note that if there is an overlap in the bindings (f-button is used for flash grenade and reload, for example), the one specified later in the file will be used and the other will be left unbinded.


## Step 2: Create an "autoexec" file in correct path and and copy the contents of "autoexec.cfg" to the newly created file.

The best way to check the correct path is to open Steam, right click  Properties -> Local files -> Browse. This will open the  installation path. From there navigate back few times to the Steam installation folder and go to 
 
 ```
 Steam/steamapps/common/Counter-Strike Global Offensive/game/csgo/cfg
 ```

Right-click on one of the text files in there (for example, a file named "perftest") choose copy and press CTR + V. You should now have a file perftest-copy in that folder. Right click on that file and choose rename and type "autoexec". Open the newly created file by double left-clicking it and copy and paste the contents of the "autoexec.cfg" in this web page to the "autoexec" file you just created. Save the file.




## Step 3: Execute autoexec whenever  is launched

To execute the autoexec file during startup of cs2. Open Steam, right-click  and go to Properties -> General -> Launch options and type (at least)

```
+exec autoexec
```

Personally, I also like to specify the in-game resolution, update frequency etc. in the launch options

```
-w 1280 -h 960 -freq 144 -console -novid -tickrate 128 +exec autoexec
```

## Step 4: Ensure that the autoexec file works

Open cs2 and type 

```
exec autoexec
```
into console. You should now see a text "AUTOEXEC CONFIG LOADED" in the console output.

## Step 5 (Optional): Add the practice configs
To enable nice set of nade practice configs, make a copy of the "autoexec" file in the same path where you just created the "autoexec" file and copy the contents of "practice.cfg" to that file. Whenever you want to practice grenades, create an empty server with no bots and type

```
exec practice
```

to the console. You may also choose to copy the files mirage_s1, mirage_s2... to that folder. These allow you to practice insta t-side window smokes by spawning automatically to the correct location and placing the crosshair into right place. Note that some of the spawns require a "walkthrow bind" which is binded to keybutton "h" in autoexec.cfg. To spawn to spawn location 1 type 

```
exec mirage_s1
```
In a free server on mirage after you have executed the practice configs.


## FAQ
 
### Few of the bindings do not work. 
* You are likely using the same button for many operations. CTR + F the "KEY" from the autoexecand see how many times it is specified.
