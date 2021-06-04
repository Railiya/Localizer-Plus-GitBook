---
description: 'base class : TextLocalizerObject'
---

# Text Localizer

UGUI Text 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/text_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LText | 언어별 텍스트를 지정합니다. 언어가 변경될 경우 컴포넌트의 텍스트가 변경된 언어의 텍스트로 설정됩니다. |

## 레퍼런스

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
| Component | UGUI Text 컴포넌트를 가져옵니다. |

| Inherited Properties |  |
| :--- | :--- |
| Text | UGUI Text 컴포넌트의 text 값을 가져옵니다. |

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
        <p>UGUI Text &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C; &#xCC3E;&#xC544; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>



