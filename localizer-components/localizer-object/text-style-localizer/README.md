---
description: 'base class : LocalizerObject'
---

# Text Style Localizer

The Localizer Style component used in UGUI Text, TextMesh, UGUI Dropdown component.

## Component

![](../../../.gitbook/assets/text_style_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OverrideFont | It changes its font when language is changed. Use existing font if it's not set. It displays a font field in each language if it's enabled. |
| OverrideLineSpacing | It changes its line spacing when language is changed. Default is 1. It displays a line spacing field in each language if it's enabled. |
| LStyleData | Edit style of each language. It change it's component font and line spacing when language is changed. |

## Reference

{% code title="TextStyleLocalizer.cs" %}
```csharp
public class TextStyleLocalizer : LocalizerObject {    
    public class StyleData { }

    public LTextStyleData LStyleData { get; set; }
    public bool OverrideFont { get; set; }
    public bool OverrideLineSpacing { get; set; }

    public UnityEngine.Font Font { get; }
    public float LineSpacing { get; }

    public override bool SetComponent () { }
}
```
{% endcode %}

| Inner Class |  |
| :--- | :--- |
| [StyleData](style-data.md) | Getting information of font and line spacing. |

| Value Definition |  |
| :--- | :--- |
| LTextStyleData | [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper class of  [TextStyleLocalizer.StyleData](style-data.md) type. |

| Properties |  |
| :--- | :--- |
| LStyleData | Get or set each language [StyleData](style-data.md) of the component. |
| OverrideFont | It change it's font when language is changed. Use existing font if it's not set. |
| OverrideLineSpacing | It change it's line spacing when language is changed. Default is 1. |
| Font | Get font value of component. |
| LineSpacing | Get lineSpacing value of component. It's not applied to Dropdown. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Inherited Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SetComponent</td>
      <td style="text-align:left">
        <p>Fine and set related UGUI Text, TextMesh component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

