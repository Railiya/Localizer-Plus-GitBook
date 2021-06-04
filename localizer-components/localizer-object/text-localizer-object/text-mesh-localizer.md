---
description: 'base class : TextLocalizerObject'
---

# Text Mesh Localizer

The Localizer component used in TextMesh component.

## Component

![](../../../.gitbook/assets/text_mesh_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LText | Edit text of each language. It changes its component text when language is changed. |

## Reference

{% code title="TextMeshLocalizer.cs" %}
```csharp
public class TextMeshLocalizer : TextLocalizerObject {
    public UnityEngine.TextMesh Component { get; }

    public override string Text { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | Get TextMesh component. |

| Inherited Properties |  |
| :--- | :--- |
| Text | Get text of TextMesh component. |

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
        <p>Fine and set TextMesh component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

