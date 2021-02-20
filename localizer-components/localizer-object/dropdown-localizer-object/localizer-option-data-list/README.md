# Localizer Option Data List

**Localizer Option Data** management class. It can convert into List&lt;Dropdown.OptionData&gt;, List&lt;TMP\_Dropdown.OptionData&gt; or vice versa.

## Reference

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
| Options | A list contains [LocalizerOptionData](localizer-option-data.md). |
| Count | Get number of  [LocalizerOptionData](localizer-option-data.md) has. |

| Extension Functions |  |
| :--- | :--- |
| ToLocalizerOptions | Convert to LocalizerOptionDataList. |
| ToDropdownOptions | Convert to List&lt;OptionData&gt; in UGUI Dropdown. |
| ToTMPDropdownOptions | Convert to List&lt;OptionData&gt; in TMP Dropdown. |

