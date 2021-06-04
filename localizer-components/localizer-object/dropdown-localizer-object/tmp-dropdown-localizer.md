---
description: 'base class : DropdownLocalizerObject'
---

# TMP Dropdown Localizer

The Localizer component used in TMP\_Dropdown component.

## Component

![](../../../.gitbook/assets/tmp_dropdown_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OptionSize | Set element count. |
| LOptions | Edit options of each language. It changes its component options when language is changed. |

## Reference

{% code title="TMPDropdownLocalizer.cs" %}
```csharp
public class TMPDropdownLocalizer : DropdownLocalizerObject {
    public TMPro.TMP_Dropdown Component { get; }

    public override LocalizerOptionDataList Options { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get TMP\_Dropdown component. |

| Inherited Properties |  |
| :--- | :--- |
| Options | Get converted LocalizerOptionDataList from options in TMP\_Dropdown. |

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
        <p>Fine and set TMP_Dropdown component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

