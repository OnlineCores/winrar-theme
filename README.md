# WINRAR-THEME-ONLINECORES
A simple theme for win-rar

_______________________________________________________________________________________________________________
# How yo create winrar theme file
## 1. INTRODUCTION
Theme file is RAR archive containing an alternative set of graphics and _winrar_theme_description.txt_ file.

## 2. NAME FORMAT
### Theme file must have **theme.rar** extension, its name format should be:  
`basename.anytext.theme.rar`

Name                  | Description
--------------------- | ---------------------
basename              | WinRAR creates a folder for theme graphics using '_basename_' name part, so you need to select something sensible and unique as basename to avoid overwriting already installed themes.
.anytext              | '_anytext_' part is optional and ignored by WinRAR. You may use it, for example, to include the version information.
.theme.rar            | File extension

***

### Here are two possible file names:

Name                  | Description
--------------------- | ---------------------
Snow.ver21.theme.rar  | it will be installed to '_Themes\Snow_' folder
Marine.theme.rar      | it will be installed to '_Themes\Marine_' folder


## 3. WINRAR_THEME_DESCRIPTION.TXT FILE
Theme file must contain `winrar_theme_description.txt` file in the root folder. It is a plain text ASCII file containing the following commands:  
### A) 'TITLE' COMMAND 
FORMAT:  
`title`=where is a text string displayed as a theme name in the "Options/Themes" menu? If you provide several themes with different toolbar sizes, it may be a good idea to include the toolbar size into the title text.  

__Examples:__  
+ title=Snow 32x32 
+ title=Snow 48x48 
+ title=Marine  

### B) 'ABOUT' COMMAND  

FORMAT:  
`about`=where is information to display in WinRAR "About" dialog. For example, it can be a copyright string or theme author name. You can use '\n' characters to split the theme description to two lines in the desired position. Do not use more than one '\n', because "About" dialog has enough space only for two description strings. Also, do not use too long string, otherwise it will not fit into the dialog.  

__Examples:__  
+ about=Marine by Peter 
+ about=© 2004 AlexDesignStudio.\nwww.AlexDesignStudio.com.  

### C) 'BACKGROUND' COMMAND 
Default color to define transparent areas in toolbar bitmaps is black, but if you wish to use the white color for this purpose, you can add: 
+ `background`=255 
command to winrar_theme_description.txt. This background color is important only if your bitmaps are not 32 bit and do not have the alpha channel.

## 4. GRAPHICS FILES
Theme file should contain the following graphics files. 
### In the root archive folder: 
Files                 | Description
--------------------- | ---------------------
AboutLogo.bmp         | 261x49 logo in "About" dialog
DiskOff.ico           | 16x16 "inactive disk" icon in the status bar
DiskOn.ico            | 16x16 "active disk" icon in the status bar
DragCopy.cur          | 32x32 "copy files" cursor for drag and drop
DragMove.cur          | 32x32 "move files" cursor for drag and drop
DragNo.cur            | 32x32 "drop prohibited" cursor for drag and drop
Estimate.bmp          | 48x48 "estimate compression" image for file "Info" dialog
File.ico              | 16x16 "unknown file type" icon
FolderUp.bmp          | 16x16 "go one folder up" toolbar button
PasswordOff.ico       | 16x16 "inactive password" icon in the status bar
PasswordOn.ico        | 16x16 "active password" icon in the status bar
RAR.ico               | 16x16,32x32,48x48 general RAR icon
RarSmall.bmp          | 13x13 image of RAR icon for shell extension menu
REV.ico               | 16x16,32x32 recovery volumes icon
Setup.ico             | 16x16 setup icon for "Add and remove programs" list
SFX.ico               | 16x16,32x32 or larger SFX module icon (see notes below)
SFXLogo.bmp           | 93x302 SFX module logo
SortDown.bmp          | 13x13 "sort down" file list column header image
SortUp.bmp            | 13x13 "sort up" file list column header image
Tray.ico              | 16x16 "WinRAR in the background" tray icon (16 colors only)
WizardLogo.bmp        | 64x64 logo for Wizard dialogs

### In the 'Toolbar' folder:
Files                 | Type                  | Description
--------------------- | --------------------- | ---------------------
Add.bmp               | "Add"                 | toolbar button
Benchmark.bmp         | "Benchmark"           | toolbar button
Comment.bmp           | "Comment"             | toolbar button
Convert.bmp           | "Convert"             | toolbar button
Delete.bmp            | "Delete"              | toolbar button
Exit.bmp              | "Exit"                | toolbar button
Extract.bmp           | "Extract"             | toolbar button
ExtractTo.bmp         | "Extract To"          | toolbar button
Find.bmp              | "Find"                | toolbar button
Info.bmp              | "Info"                | toolbar button
Lock.bmp              | "Lock"                | toolbar button
Print.bmp             | "Print"               | toolbar button
Protect.bmp           | "Protect"             | toolbar button
Repair.bmp            | "Repair"              | toolbar button
Report.bmp            | "Report"              | toolbar button
SFX.bmp               | "SFX"                 | toolbar button
Test.bmp              | "Test"                | toolbar button
View.bmp              | "View"                | toolbar button
VirusScan.bmp         | "VirusScan"           | toolbar button
Wizard.bmp            | "Wizard"              | toolbar button

## NOTES: 
A)  
Though it is better to keep original sizes, the size of many bitmaps can be slightly changed without hurting WinRAR look. You can check the outcome of such change experimentally if necessary. 

B)  
You can use any reasonable size for toolbar buttons. WinRAR will detect it automatically. 

C)  
You can use both 24-bit and 32-bit bitmaps with alpha channel for toolbar buttons and for FolderUp button. In case of 24-bit bitmaps use the black color to define transparent areas. 

D)  
One theme file can include only one set of toolbar buttons. If you wish to provide themes with buttons of different size, create several theme files. 

E)  
Use gray RGB (192,192,192) color in SortUp.bmp and SortDown.bmp to define transparent areas. 

F)  
SortUp.bmp and SortDown.bmp are used only in Windows XP and older. WinRAR uses standard Windows sort direction images in Windows Vista and newer. 

G)  
Color depth is not limited for most icons except Tray.ico, which must be 16 colors. WinRAR uses Tray.ico only for Windows 2000, where a usual 256 color icon is not displayed well. 

H)  
It’s allowed to omit most of graphics files. In this case WinRAR, will use the default graphics instead. The only exception is Add.bmp file. WinRAR uses it to detect toolbar button dimensions, it must be present. 

## 5. CONTACTS
Please send your questions and theme files to dev@rarxlab.com (Please remove x from the middle of 'rarxlab'. Sorry, spam protection). 
If your theme is based on someone's else graphics, we need to have a permission of original graphics copyright owner to use icons in WinRAR theme. Please send to us a copy of such permission by email.
