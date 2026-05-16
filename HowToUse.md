# How to Use Bedrock GUI Docs

> Read this page before diving into the content of this document, it'll save you a lot of confusion later.

## 1. How this doc helps you?
<br><br>
This Wiki(doc) documents each GUI textures with:

- **What it's called** — A generic name by me for easier recognition
- **Where it actually appears in game** — because the name doesn't always make it obvious
- **What's the name** — the internal texture name you'll customize in your pack.

<br><br>

For Ore UI:
- **What it's called** — A generic name by me for easier recognition
- **Mindmap** — the visual guide to point the user which parts exactly the color does change
- **Color List** — a list of colors required to edit the color in certain parts of the ui

<br><br>
This is important because Ore UI Customizer website previews is very limited than actually seeing in-game. The notes in this doc are based on real in-game testing.

---

## 2. How to Navigate This Doc

### Sidebar sections <!-- {docsify-ignore} -->

The sidebar is split into a few sections and used to quicken your action:

| Entries/Categories | What you'll find |
| :--- | :--- |
| **Home** | Project intro and overview |
| **How to use** | This page |
| **Quick Browse** | *(Hint for Content below — not a link)* |
| **UI** | Texture names for the `textures/ui/` folder *(coming soon)* |
| **GUI** | Texture names for the `textures/gui/` folder *(coming soon)* |
| **Global Variables** | Color and value names from `_global_variables.json` *(partially done )* |
| **Ore UI Colors** | Color variable list for Ore UI Customizer |

## 3. Finding a texture or color name

> it all could be done in just 4 steps:

1. **First, Know what you want to change** — start with the thing you see on screen (e.g. "the background color of the settings panel").
2. **Second, Go to the relevant section** — if it's an Ore UI screen, check Ore UI Colors. If it's a classic GUI texture, check UI or GUI. If it's a the GUI text color, check Global Variables. everything is already sorted in certain categories.
3. **Third, Look up the name** — each page lists names alongside screenshots or descriptions so you can match them to what you see in game.
4. **Fourth, Use it in your project** — copy the name and find the texture in your resource pack. color variable name in global variables, and color name in Ore UI Customizer

---
> # Cool Facts Corner

## 1. UI and GUI

UI stands for User Interface while GUI stands for Graphical User Interface. When you customize Minecraft Bedrock's GUI, you're working inside a **resource pack**. Here's the folder layout you'll run into across this documentation:

```
📦 Your Resource Pack
 ┣ 📂 ui/
 ┃  └─ 📄 _global_variables.json
 ┣ 📂 textures/
 ┃  ┣ 📂 gui/
 ┃  └─ (texture files used in the interface)
 ┃  ┣ 📂 ui/
 ┃  ┃  └─ (EVERYTHING for the interface)
 ┃  └─ ...
```

**What each piece does:**

| File / Folder | What it is |
| :--- | :--- |
| `📂 ui/` | Contains `.json` files that define every on-screen element — buttons, panels, text labels, etc. |
| `📂 textures/gui/` `📂 textures/ui/` | Holds the actual image files (`.png`) that the UI references. changing these is what most texture packs do. |
| `📄 _global_variables.json` | A single file that stores shared values — colors, sizes, and flags — referenced across many UI files at once. Changing one value here can affect dozens of elements. |

> **Note:** The `ui/` and `textures/ui/` are separate things, even though both relate to the game's interface.

The goal of this wiki - which i refer as doc - is to tell you exactly *which* texture or variable name controls *which* thing you see on screen, so you don't have to guess.

---
## 2. Global Variables

as previously explained, `_global_variables.json` is a single JSON file that handles variable configuration referred to certain UI parts.

The file itself located behind the `ui/` folder, the first time you open will see bunch of configurations below:
```
{
//////// Text colors ////////
"$generic_button_text_color": [ 1.0, 1.0, 1.0 ], // for those times you find a button that's kind of used but shouldn't...

"$light_button_default_text_color": [ 0.3, 0.3, 0.3 ],
"$light_button_hover_text_color": [ 1.0, 1.0, 1.0 ],
"$light_button_pressed_text_color": [ 1.0, 1.0, 1.0 ],
"$light_button_locked_text_color": [ 0.3, 0.3, 0.3 ],
...
```
a good way to mention, the configuration `[ 0.3, 0.3, 0.3 ]` you just see right now is a color code named RGB 0-1, it's similar to website's RGB code, but they were divided by 255, sitting inside a square-bracket array.

the best way to customize these colors is by going through a website called [RGB 0-1 Color Picker](https://rgbcolorpicker.com/0-1) and copy and paste bunch of numbers inside the bracket.

the intent of this doc is solely focuses on checking every purposes of each functional variables. more update will come

> **Fun Fact:** Global Variables doesn't only configure the interface text color, but also every ui elements with property values denoted to it. for example, the screen animation speed.

---
## 3. Ore UI Customizer

### What is Ore UI? <!-- {docsify-ignore} -->

Minecraft Bedrock's interface has been partially rebuilt using a system called **Ore UI** — a React-facet-based layer that runs on top of the old JSON UI. Ore UI handles many of the bedrock screens in the current version (like the new world menu, settings, etc.).

A little thing to know about Ore UI, the source code of it were stored inside the game installation files, under the folder `gui`. technically, you CAN modify the source code and change the color. but the color was hardcoded, means it cannot be edited by changing one variable like global variables.

it was believed you couldn't customize it. Until April 2025, `@8Crafter` proved otherwise with his [Ore UI Customizer](https://www.8crafter.com/utilities/ore-ui-customizer) tool — it customizes the color variables that Ore UI use, and lets you override them through [**minecraft bedrock installation file.**](https://minecraft.wiki/w/Bedrock_Edition_installation_files)

this doc accompanies your journey to spot the exact color for customizing ore ui using Ore UI Customizer