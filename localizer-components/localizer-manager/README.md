---
description: 에셋의 핵심
---

# Localizer Manager

언어 설정 및 **Localizer Object** 를 관리하는 static class입니다.

**Localizer Object**의 언어를 변경하기 위해서는 **Localizer Manager**의 **SetLanguage** 를 호출합니다. 현재 언어의 정보를 가져오려면 **SelectedLanguage **혹은 **SelectedLanguageIndex**를 통해 가져올 수 있습니다. 언어가 변경되었을 때 호출되는 이벤트가 필요하다면 **OnLanguageChagned**를 사용합니다.

## 레퍼런스

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

| Static Properties     |                                                     |
| --------------------- | --------------------------------------------------- |
| Languages             | 프로젝트의 언어 목록을 가져옵니다.                                 |
| SelectedLanguage      | 현재 적용된 언어의 [LanguageInfo](language-info.md)를 가져옵니다. |
| SelectedLanguageIndex | 현재 적용된 언어의 인덱스를 가져옵니다.                              |

| Static Events     |                                  |
| ----------------- | -------------------------------- |
| OnLanguageChanged | SetLanguage가 호출될 경우 실행되는 이벤트입니다. |

| Static Functions     |                                                                                                                            |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| SetLanguage          | 언어를 변경합니다.                                                                                                                 |
| SetLanguageToDefault | 기본 (첫 번째) 언어로 변경합니다.                                                                                                       |
| RemoveNullObjects    | <p>object 리스트에서 null인 <a href="../localizer-object/">LocalizerObject</a>를 제거합니다. </p><p>(참고: OnDestroy에서 기본적으로 제거됩니다.)</p> |
| GetLocalizersOfType  | 해당 [LocalizerObject ](../localizer-object/)타입의 object들을 리스트에서 가져옵니다.                                                       |
| IndexOfLanguage      | 언어의 인덱스를 가져옵니다.                                                                                                            |

{% hint style="warning" %}
게임 내에서 사용되는 언어의 값들은 **SelectedLanguage** 및 **SelectedLanguageIndex** 를 기반으로 결정됩니다. 기본값은 항상 0번 인덱스의 언어이며 이는 **SetLanguage**를 통해서만 변경됩니다. **Localizer Manager Window**를 통한 씬의 언어 변경은 이에 영향을 주지 않습니다. 정상적인 언어 변경을 위해 언어 테스트 이후 반드시 0번 인덱스의 언어로 변경하길 권장합니다.
{% endhint %}
