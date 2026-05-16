# How to Use Ore UI Customizer <!-- {docsify-ignore-all} -->

---
Here i will show you a step-by-step guide. and of course, prerequisites to get started.

> ## What you Need
> - **An ability to access Bedrock's Installation Files** - i would prefer to say this is the engine folder of bedrock because this is not `📁 com.mojang` folder, read more through [Minecraft Wiki](https://minecraft.wiki/w/Bedrock_Edition_installation_files).
> - **Ore UI Customizer** - it has three platforms: Windows app with node.js **required**, Website, and CLI (a fancy word for command prompt)
> - **WinRAR/any type of archiver** - required to extract/archive the zip file.
> - **Bedrock GUI Docs** - the website you visit right now

## 1. Open Ore UI Customizer Website
[https://www.8crafter.com/utilities/ore-ui-customizer](https://www.8crafter.com/utilities/ore-ui-customizer)<br>
when you load the page, you will be greet with this:

<img src="/images/howtouse/step1.jpeg" style="width:50%;">

on top, there's more detailed instructions on how to use the Website and access Bedrock Installation Files. in this demonstration i will use 
LeviLauncher

## 2. Navigate Bedrock Installation Files (not com.mojang)
Unfortunately, you can't do this on iOS. this could be done by using custom launcher, IObit unlocker, or you can also access through this powershell command if you download from microsoft store:<br>
```
& "$ENV:SystemRoot\explorer.exe" "$((Get-AppxPackage "Microsoft.MinecraftUWP").InstallLocation)"
```
In Custom Launcher. it usually located inside `.../version/your-version` folder. on LeviLauncher, you just click on gear icon besides the instance, and click on **Open Game Installation Directory**

<img src="/images/howtouse/levi-launcher-open.jpeg" style="width:50%;">

congrats, you're inside the installation folder

<img src="/images/howtouse/bedrock-installation-file.jpeg" style="width:50%;">

## 3. Find the gui folder
click on data folder

<img src="/images/howtouse/inside-data-folder.jpeg" style="width:50%;">

## 4. Archive the gui folder
right click on gui: WinRAR > Add to Archive > ZIP

<img src="/images/howtouse/convert-to-zip.jpeg" style="width:50%;">

## 5. Drag the ZIP into the Website
<img src="/images/howtouse/drag-to-web.jpeg" style="width:50%;">

## 6. Go to 'Show Options' Button
<img src="/images/howtouse/show-option.jpeg" style="width:50%;">

You will be welcomed with 3 tab sections:
- **General** - an extra modification
- **Colors** - list of colors you can replace
- **Plugins** - List of plugins applied, you can only import them with `import plugins` on the main page

## 7. Click on 'Colors' section to start customizing
<img src="/images/howtouse/color-tab.jpeg" style="width:50%;">

## 8. find the color name for certain part of ui
let's customize **disabled button**. in "this" website, go to buttons section on the left sidebar, and you will see something like this

<img src="/images/howtouse/bgdocs-demo.jpeg" style="width:50%;">

now go back to the website, and match the color name

<img src="/images/howtouse/color-shown.jpeg" style="width:50%;">

## 9. Click on 'Apply Mods'
after you're done customizing, close the option screen and click `apply mods`

<img src="/images/howtouse/apply-mods.jpeg" style="width:50%;">

## 10. Download the Modded 'gui.zip'

<img src="/images/howtouse/download.jpeg" style="width:50%;">

## 11. extract the zip file

<img src="/images/howtouse/extract.jpeg" style="width:50%;">

## 12. drag and replace the gui folder
drag the modded gui folder into data folder, make sure to backup the old one

<img src="/images/howtouse/replace-gui.jpeg" style="width:50%;">

> **That's it, Congratulation!** Now you've made your first Ore UI Customization