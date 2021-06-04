---
description: 'base class : DropdownLocalizerObject'
---

# Dropdown Localizer

The Localizer component used in UGUI Dropdown component.

## Component

![](../../../.gitbook/assets/dropdown_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OptionSize | Set element count. |
| LOptions | Edit options of each language. It changes its component options when language is changed. |

## Reference

{% code title="DropdownLocalizer.cs" %}
```csharp
public class DropdownLocalizer : DropdownLocalizerObject {
    public UnityEngine.UI.Dropdown Component { get; }

    public override LocalizerOptionDataList Options { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get UGUI Dropdown component. |

| Inherited Properties |  |
| :--- | :--- |
| Options | Get converted LocalizerOptionDataList from options in UGUI Dropdown. |

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
        <p>Fine and set UGUI Dropdown component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

