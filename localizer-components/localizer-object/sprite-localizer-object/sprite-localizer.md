---
description: 'base class : SpriteLocalizerObject'
---

# Sprite Localizer

SpriteRenderer 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/sprite_localizer_inspector.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Properties</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">LSprite</td>
      <td style="text-align:left">
        <p>&#xC5B8;&#xC5B4;&#xBCC4; &#xC2A4;&#xD504;&#xB77C;&#xC774;&#xD2B8;&#xB97C;
          &#xC9C0;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC5B8;&#xC5B4;&#xAC00; &#xBCC0;&#xACBD;&#xB420; &#xACBD;&#xC6B0; &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xC758;
          &#xC2A4;&#xD504;&#xB77C;&#xC774;&#xD2B8;&#xAC00; &#xBCC0;&#xACBD;&#xB41C;
          &#xC5B8;&#xC5B4;&#xC758; &#xC2A4;&#xD504;&#xB77C;&#xC774;&#xD2B8;&#xB85C;
          &#xC124;&#xC815;&#xB429;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

## 레퍼런스

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
| Component | SpriteRenderer 컴포넌트를 가져옵니다. |

| Inherited Properties |  |
| :--- | :--- |
| Text | SpriteRenderer 컴포넌트의 sprite 값을 가져옵니다. |

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
        <p>SpriteRenderer &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C; &#xCC3E;&#xC544;
          &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

