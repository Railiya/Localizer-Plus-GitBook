---
description: 'base class : LocalizerObject'
---

# Text Localizer Object

base class of the **Text Localizer, Text Mesh Localizer, TMP Text Localizer, Text Custom Localizer**.

## Reference

{% code title="LocalizerObject.cs" %}
```csharp
public class LString : LValue<string> { }

public TextLocalizerObject : LocalizerObject {
    public LString LText { get; set; }
    
    public abstract string Text { get; }
    public abstract override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |  |
| :--- | :--- |
| LString | [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper class of string type. |

| **Properties** |  |
| :--- | :--- |
| LText | Get or set text each language of the component. |

| Abstract Properties |  |
| :--- | :--- |
| Text | Get text value of the component. |

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



