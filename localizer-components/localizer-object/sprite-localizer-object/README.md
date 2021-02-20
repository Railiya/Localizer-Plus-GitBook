---
description: 'base class : LocalizerObject'
---

# Sprite Localizer Object

base class of the **Sprite Localizer, Image Localizer**.

## Reference

{% code title="LocalizerObject.cs" %}
```csharp
public class LSprite : LValue<UnityEngine.Sprite> { }

public SpriteLocalizerObject : LocalizerObject {
    public LSprite LSprite { get; set; }
    
    public abstract UnityEngine.Sprite Sprite { get; }
    public abstract override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |  |
| :--- | :--- |
| LSprite | [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper class of Sprite type. |

| **Properties** |  |
| :--- | :--- |
| LSprite | Get or set sprite each language of the component. |

| Abstract Properties |  |
| :--- | :--- |
| Sprite | Get sprite of component. |

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



