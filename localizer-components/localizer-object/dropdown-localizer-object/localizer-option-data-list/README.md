# Localizer Option Data List

**LocalizerOptionData**를 관리하는 클래스입니다. List&lt;Dropdown.OptionData&gt; 와 List&lt;TMP\_Dropdown.OptionData&gt; 로 상호간에 변환이 가능합니다.

## 레퍼런스

{% code title="LocalizerObject.cs" %}
```csharp
public class LocalizerOptionDataList { 
    public List<LocalizerOptionData> Options { get; set; }
    public int Count { get; }
}

public static class LocalizerDropdownExtension {
    public static LocalizerOptionDataList ToLocalizerOptions (this List<Dropdown.OptionData> value) { }
    public static LocalizerOptionDataList ToLocalizerOptions (this List<TMP_Dropdown.OptionData> value) { }
    public static List<Dropdown.OptionData> ToDropdownOptions (this LocalizerOptionDataList value) { }
    public static List<TMP_Dropdown.OptionData> ToTMPDropdownOptions (this LocalizerOptionDataList value) { }
}
```
{% endcode %}

| **Properties** |  |
| :--- | :--- |
| Options | [LocalizerOptionData](localizer-option-data.md)를 가지는 리스트입니다. |
| Count | 보유중인 [LocalizerOptionData](localizer-option-data.md)의 수를 가져옵니다. |

| Extension Functions |  |
| :--- | :--- |
| ToLocalizerOptions | LocalizerOptionDataList로 변환합니다. |
| ToDropdownOptions | UGUI Dropdown의 List&lt;OptionData&gt; 로 변환합니다. |
| ToTMPDropdownOptions | TMP Dropdown의 List&lt;OptionData&gt;로 변환합니다. |

