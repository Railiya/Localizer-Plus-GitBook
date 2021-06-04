---
description: 'base class : TextLocalizerObject'
---

# Text Localizer

The Localizer component used in UGUI Text component.

## Component

![](../../../.gitbook/assets/text_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LText | Edit text of each language. It changes its component text when language is changed. |

## Reference

{% code title="TextLocalizer.cs" %}
```csharp
public class TextLocalizer : TextLocalizerObject {
    public UnityEngine.UI.Text Component { get; }

    public override string Text { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get UGUI Text component. |

| Inherited Properties |  |
| :--- | :--- |
| Text | Get text of UGUI Text component. |

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
        <p>Fine and set UGUI Text component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

