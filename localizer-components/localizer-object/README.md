---
description: Core of core of asset
---

# Localizer Object

Supports localization as component of the game objects that actually rendered or playing sounds likes Text, Image, Audio. These components are change it's content when called **SetLanguage** in **Localizer Manager**.

Each component have Wrapper class of **LValue&lt;T&gt;**. For instance, **Text Localizer Object** has **LString** which wrapped with **LValue&lt;string&gt;** and contains contents by this value. You can change it freely in inspector or script.

Some components are inherits base class for required component. For instance, **Text Localizer, Text Mesh Localizer, TMP Text Localizer** these are inherits **Text Localizer Object**. It's for use RequireComponent attribute, and **Style Localizers** are doesn't have it because of support multiple components.

{% hint style="info" %}
If language settings apply goes abnormally, so that **Localizer Objects** doesn't update language settings, It displays warning that language count doesn't match in inspector. You can update by press "Update Project Language Settings" in **Localizer Manager** editor window.
{% endhint %}

> ## Q. How do I add a component?

You can add component by _"Add Component - Localizer"_ in inspector or _"Component - Localizer"_ in editor upper menu. If you're using **Localizer Manager** editor window, "Add Localizer" button will be enabled when select object doesn't have Localizer component and press it to add the component automatically by attached component of object.

{% hint style="info" %}
By clicking "Add Verified Localizer" or "Add Verified Style Localizer" in Component menu, You can add Localizer or Style Localizer component to all selected game objects in hierarchy. It adds an estimated component by component of game object. It does not add a component if the game object doesn't have a proper component.
{% endhint %}

> ## Q. When I use it?

Component are proper method localizing directly without extra works. You can edit each language content in inspector, and change content comfortably by **Localized Dictionary** or **LValue&lt;T&gt;** in script.

But it's effective when the amount of text is small or less language count in the project. If the amount of text is big, the memory management goes to be difficult. So it does, recommended to use **Script** or use it together.

You can find information about each Localizer in sub list.

