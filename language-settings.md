---
description: Must have virtue before getting started
---

# Language Settings

Before the localization, you have to set language settings. You can define languages in **Localizer Project Settings**. The **Localizer Project Settings** is in _LocalizerPlus_ folder when the package is imported.

{% hint style="info" %}
Language setting must be Korean for 0 index, English for 1 index to play example games normally. If you want to play example games, you need to change language settings after play example games.
{% endhint %}

## Localizer Project Settings

Save and use language settings and editor only default values in project. You can change language settings and default values are can be changed in **Localizer Manager** editor window.

You can create asset in **Localizer Manager** editor window if asset is not in project. If multiple assets are exists, you can set actually used main project settings in **Localizer Manager** editor window. Only change language settings can be changed in main project settings and editor default values saved as well.

## Edit Languages

![](.gitbook/assets/language_settings_projectsettings.png)

Basically language edit is enabled for prevent mistakes. You can press "Enable Edit" to activate language edit. Press "Add New" or "Remove Last" to add or remove languages an "Apply Languages" to change languages. This work doing compile, update assets and Localizer components, so it can be takes time a while.

{% hint style="info" %}
Changing language setting is modifying content of **Languages.cs** script in _Runtime_ script folder and recompile. If you edit script via scripting, It asks you to select what you will use between current language settings or restore project setting languages. This method can not update language settings of components and assets. So you have to press "Update Project Language Settings" in **Localizer Manager** editor window to update.

Language settings apply is update language settings of **Localizer Project Settings**, **Localized Dictionaries** in project and **Localizer Objects** in current scene. Only current scene has updated and other scenes are listed on project settings, updated and excluded from the list when the scene is opened.
{% endhint %}

{% hint style="warning" %}
The functions used in this asset are based on language settings in **Languages.cs**. Most functions are worked based on index, so you should not swap or delete the languages.
{% endhint %}

