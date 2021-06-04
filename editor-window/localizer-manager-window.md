---
description: Best choice to manage Localizer Component
---

# Localizer Manager Window

The editor window that supports functions such as setting the main **Localizer Project Settings**, language preview, and **Style Localizer** batch settings used in the editor.

![Localizer list of Cube Collector example](../.gitbook/assets/localizer_manager_window%20%281%29.png)

## Localizer Object List

Game Object list that has **Localizer Object** component. It doesn't contain **Tag Formatter**. It selected in hierarchy If select object in list and vice versa.

## Localizer Information

Displays information of selected **Localizer Object** in list. It shows game object, component type and content. If you select game object that not **Localizer Object** in hierarchy, "Add Localizer" button will be enabled. It adds localizer component automatically by component of game object if "Add Localizer" button clicked.

## Localizer Project Settings

Setting actually used **Localizer Project Settings** in project. The language settings and values of default override options are applied by main project settings.

## Localizer Management

| Management |  |
| :--- | :--- |
| Language | Language setting used in editor. |
| Override Contents | Content that selected language applied to Localizer component in realtime. |
| Apply Language to Selected Localizer | Set selected component language to Language. |
| Apply Language to Scene Localizers | Set all component's language to Language. |
| Update Project Language Settings | Update language settings of components in all scenes. |
| Add Localizer to All Scene Texts | Add component to all Text, TextMesh, TMP Text in scene. |

{% hint style="info" %}
After setting Language and press "Apply Language to Scene Localizers", All Localizer component's language is changed. This is for preview work in the editor, you have to back to the default language when you build the game. \(Refer : Only applied to current scene.\)

When language settings are changed and script recompiled, the Localizer component's language settings are changed as well. If it is not properly processed, you can update it by press "Update Project Language Settings".
{% endhint %}

## Style Localizer Default Override Option

The function that when **Style Localizer** component added, It enables Override options and set values automatically. Enable by checking override options and set default values by setting values of each language on bottom.

| Options |  |
| :--- | :--- |
| Override Font | Enable font of Text Style. |
| Override Line Spacing | Enable line spacing of Text Style. |
| Override Font Asset | Enable font asset and material preset of TMP Style. |
| Override Spacing Options | Enable spacing options of TMP Style. |
| Override Selected Style Localizer | Override settings of selected Style component in list. |
| Override All Style Localizers | Override settings of all Style components in scene. |

{% hint style="info" %}
Change override settings and default values of all **Style Localizers** in scene as settings of editor window by clicking "Override All Style Localizers" button.
{% endhint %}

