---
description: 'base class : SpriteLocalizerObject'
---

# Sprite Localizer

The Localizer component used in SpriteRenderer component.

## Component

![](../../../.gitbook/assets/sprite_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LSprite | Edit sprite of each language. It changes its component sprite when language is changed. |

## Reference

{% code title="SpriteLocalizer.cs" %}
```csharp
public class SpriteLocalizer : SpriteLocalizerObject {
    public UnityEngine.SpriteRenderer Component { get; }

    public override UnityEngine.Sprite Sprite { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get SpriteRenderer component. |

| Inherited Properties |  |
| :--- | :--- |
| Text | Get sprite value of SpriteRenderer component. |

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
        <p>Fine and set SpriteRenderer component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

