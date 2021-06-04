---
description: Best choice to create Script file
---

# Script Writer Window

The editor window that can edit **Script Writer Node Collection**. It can export **Script** and **Compressed Script**. It also can edit and export the **Localized Dictionary**.

![swnc file used in Capsule Story example](../.gitbook/assets/script_writer_window.png)

## Toolbar

### File

Save or open **Script Writer Node Collection**. Or you can merge swnc file by import. And you can import **Localized Dictionary**, csv, tsv as Directory. Can export **Script**, **Compressed Scritpt**, Localized Dictionary as file.

{% hint style="info" %}
**Script** and **Compressed Script** can export only content of selected language. If language and swnc file increases, the work can be inconvenient. So recommended to use **Swnc Exporter** scriptable object when exporting files.
{% endhint %}

### Indexing

The id format that given automatically when content added. Area is range of **Directory** index decided. In Format, index replaces {index} and **Directory** name replaces {id}. Length is minimum length of index.

| Area |  |
| :--- | :--- |
| Local | Range of current Directory. |
| Top | Range of top Directory. |
| Global | Range of all Directories. |

### View

Display type of Viewer. Default is hierarchy. If you change it to explorer, It shows list has contents with full path. You can search keyword in this view mode.

### Language

Setting editor language. The language settings depend on project settings, and it's displayed as LanguageText.

## Viewer

Displays Directory and Content nodes as hierarchy. You can open the context menu with right click, and you can open or close the node with double click or more. If a node clicked, the content is displayed in the editor, if it is content, the editor will be enabled.

## Editor

The area that can edit id and content of the script. Use Edit in content menu if you want to edit **Directory**.

## External Program

The editor window has limitation, so it can be inconvenient for work. You can visit develop blog to download **Script Writer** program for free. It supports shortcut keys, advanced indexing and id modify, linear layout, preview contents, module system for encryption, register file extension, etc, It has various convenient functions. You can find it from External Links.

{% hint style="warning" %}
The program doesn't have malignant code, but it has not been unauthenticated. So it does not write in documentation. And developer blog is written in Korean.
{% endhint %}

