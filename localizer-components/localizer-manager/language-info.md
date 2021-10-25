# Language Info

언어의 정보를 나타냅니다.

## 레퍼런스

{% code title="LocalizerManager.cs" %}
```csharp
public class LanguageInfo {
    public string LanguageText { get; }
    public UnityEngine.SystemLanguage SystemLanguage { get; }
    
    public LanguageInfo (string languageText, UnityEngine.SystemLanguage systemLanguage) { }
    
    public override string ToString () { }
}
```
{% endcode %}

| Properties     |                            |
| -------------- | -------------------------- |
| LanguageText   | 언어의 텍스트를 가져옵니다.            |
| SystemLanguage | 언어의 SystemLanguage를 가져옵니다. |

| Constructors |                                                       |
| ------------ | ----------------------------------------------------- |
| LanguageInfo | LanguageText, SystemLanguage를 가진 LanguageInfo를 생성합니다. |

| Inherited Functions |                                                                         |
| ------------------- | ----------------------------------------------------------------------- |
| ToString            | <p>언어의 정보를 가져옵니다. </p><p>(형식: $"{LanguageText} ({SystemLanguage})")</p> |

