---
description: 'base class : LocalizerObject'
---

# Dropdown Localizer Object

base class of the **Dropdown Localizer, TMP Dropdown Localizer**.

It uses **LocalizerOptionData** and **LocalizerOptionDataList** for compatibility because OptionData in Dropdown and TMP\_Dropdown is different. Also, it provides extension functions convert each types for convenience.

## Reference

{% code title="LocalizerObject.cs" %}
```csharp
public class LOptionDataList : LValue<LocalizerOptionDataList> { }

public DropdownLocalizerObject : LocalizerObject {
    public LOptionDataList LOptions { get; set; }
    
    public abstract LocalizerOptionDataList Options { get; }
    public abstract override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |  |
| :--- | :--- |
| LOptionDataList | [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper class of  [LocalizerOptionDataList ](localizer-option-data-list/)type. |

| **Properties** |  |
| :--- | :--- |
| LOptions | Get or set dropdown options each language of the component. |

| Abstract Properties |  |
| :--- | :--- |
| Options | Get dropdown options in component. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Inherited Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SetComponent ()</td>
      <td style="text-align:left">
        <p>Set component attached in current object.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

