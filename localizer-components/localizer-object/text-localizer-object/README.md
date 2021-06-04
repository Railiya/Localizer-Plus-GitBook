---
description: 'base class : LocalizerObject'
---

# Text Localizer Object

**Text Localizer, Text Mesh Localizer, TMP Text Localizer, Text Custom Localizer**의 베이스 클래스입니다.

## 레퍼런스

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
| LString | string 타입의 [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| **Properties** |  |
| :--- | :--- |
| LText | 컴포넌트의 언어별 텍스트를 가져오거나 변경합니다. |

| Abstract Properties |  |
| :--- | :--- |
| Text | 컴포넌트의 text 값을 가져옵니다. |

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
        <p>&#xD604;&#xC7AC; &#xC624;&#xBE0C;&#xC81D;&#xD2B8;&#xC5D0; &#xBD80;&#xCC29;&#xB41C;
          &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>



