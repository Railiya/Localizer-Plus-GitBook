---
description: Core of asset
---

# Localizer Manager

The static class that change languages and manage **Localizer Object**.

To change the language of **Localizer Object**, you have to call **SetLanguage** in **Localizer Manager**. If you want to get language information, you can get it from **SelectedLanguage** or **SelectedLanguageIndex**. If you need the event language changed, use **OnLanguageChganed**.

## Reference

{% code title="LocalizerManager.cs" %}
```csharp
public static class LocalizerManager {
    public static LanguageInfo[] Languages { get; }
    public static LanguageInfo SelectedLanguage { get; }
    public static int SelectedLanguageIndex { get; }
    
    public static event System.Action<LanguageInfo> OnLanguageChange;
    
    public static void SetLanguage (string language) { }
    public static void SetLanguage (UnityEngine.SystemLanguage language) { }
    public static void SetLanguageToDefault () { }
    
    public static void RemoveNullObjects () { }
    public static T[] GetLocalizersOfType<T> () where T : LocalizerObject { }
    
    public static int IndexOfLanguage (LanguageInfo language) { }
    public static int IndexOfLanguage (string language { }
    public static int IndexOfLanguage (UnityEngine.SystemLanguage language) { }
}
```
{% endcode %}

| Static Properties |  |
| :--- | :--- |
| Languages | Get languages of project |
| SelectedLanguage | Get current applied [LanguageInfo](language-info.md). |
| SelectedLanguageIndex | Get current applied language index. |

| Static Events |  |
| :--- | :--- |
| OnLanguageChanged | Event called after SetLanguage. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Static Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SetLanguage</td>
      <td style="text-align:left">Change language.</td>
    </tr>
    <tr>
      <td style="text-align:left">SetLanguageToDefault</td>
      <td style="text-align:left">Change to default (first) language.</td>
    </tr>
    <tr>
      <td style="text-align:left">RemoveNullObjects</td>
      <td style="text-align:left">
        <p>Remove null <a href="../localizer-object/">LocalizerObject</a> in object
          list</p>
        <p>(Refer : It removed OnDestroy basically)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetLocalizersOfType</td>
      <td style="text-align:left">Get <a href="../localizer-object/">LocalizerObject </a> type objects from
        list.</td>
    </tr>
    <tr>
      <td style="text-align:left">IndexOfLanguage</td>
      <td style="text-align:left">Get index of language.</td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
The languages used in the game is decided base on **SelectLanguage** and **SelectedLanguageIndex**. Default is always language in 0 index, and it changed only through **SetLanguage**. Scene language change with **Localizer Manager Window** does not affect to it. For change the language normally, recommend to set language to 0 index language after language test of scene.
{% endhint %}

