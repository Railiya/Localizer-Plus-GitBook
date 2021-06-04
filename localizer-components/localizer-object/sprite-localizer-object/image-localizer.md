---
description: 'base class : SpriteLocalizerObject'
---

# Image Localizer

The Localizer component used in UGUI Image component.

## Component

![](../../../.gitbook/assets/image_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LSprite | Edit sprite of each language. It changes its component sprite when language is changed. |

## Reference

{% code title="ImageLocalizer.cs" %}
```csharp
public class ImageLocalizer : SpriteLocalizerObject {
    public UnityEngine.UI.Image Component { get; }

    public override UnityEngine.Sprite Sprite { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get UGUI Image component. |

| Inherited Properties |  |
| :--- | :--- |
| Text | Get sprite value of UGUI Image component. |

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
        <p>Fine and set UGUI Image component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

