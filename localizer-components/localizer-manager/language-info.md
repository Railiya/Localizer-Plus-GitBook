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

| Properties |  |
| :--- | :--- |
| LanguageText | 언어의 텍스트를 가져옵니다. |
| SystemLanguage | 언어의 SystemLanguage를 가져옵니다. |

| Constructors |  |
| :--- | :--- |
| LanguageInfo | LanguageText, SystemLanguage를 가진 LanguageInfo를 생성합니다. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Inherited Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">ToString</td>
      <td style="text-align:left">
        <p>&#xC5B8;&#xC5B4;&#xC758; &#xC815;&#xBCF4;&#xB97C; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
        <p>(&#xD615;&#xC2DD;: $&quot;{LanguageText} ({SystemLanguage})&quot;)</p>
      </td>
    </tr>
  </tbody>
</table>



