# Language Info

Displays language information

## Reference

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
| LanguageText | Get text of language. |
| SystemLanguage | Get SystemLanguage of language. |

| Constructors |  |
| :--- | :--- |
| LanguageInfo | Create LanguageInfo contains LanguageText and SystemLanguage. |

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
        <p>Get information of language.</p>
        <p>(Format : $&quot;{LanguageText} ({SystemLanguage})&quot;)</p>
      </td>
    </tr>
  </tbody>
</table>

