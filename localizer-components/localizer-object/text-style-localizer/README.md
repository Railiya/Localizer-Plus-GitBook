---
description: 'base class : LocalizerObject'
---

# Text Style Localizer

UGUI Text, TextMesh, UGUI Dropdown 컴포넌트에 사용되는 Localizer Style 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/text_style_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OverrideFont | 언어가 변경될 때 해당 언어에 지정된 폰트로 변경합니다. 폰트가 지정되어 있지 않을 경우 기존의 폰트를 계속 사용합니다. 이 기능을 사용면 각 언어마다 Font 설정이 표시됩니다. |
| OverrideLineSpacing | 언어가 변경될 때 해당 언어에 지정된 라인 스페이싱으로 변경합니다. 기본값은 1입니다. 이 기능을 사용면 각 언어마다 라인 스페이싱 설정이 표시됩니다. |
| LStyleData | 언어별 스타일을 지정합니다. 언어가 변경될 경우 컴포넌트의 폰트 및 라인 스페이싱이 변경된 언어의 스타일로 설정됩니다. |

## 레퍼런스

{% code title="TextStyleLocalizer.cs" %}
```csharp
public class TextStyleLocalizer : LocalizerObject {    
    public class StyleData { }

    public LTextStyleData LStyleData { get; set; }
    public bool OverrideFont { get; set; }
    public bool OverrideLineSpacing { get; set; }
    
    public UnityEngine.Font Font { get; }
    public float LineSpacing { get; }
 
    public override bool SetComponent () { }
}
```
{% endcode %}

| Inner Class |  |
| :--- | :--- |
| [StyleData](style-data.md) | 폰트 및 라인 스페이싱 정보를 가집니다. |

| Value Definition |  |
| :--- | :--- |
| LTextStyleData | [TextStyleLocalizer.StyleData](style-data.md) 타입의 [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| Properties |  |
| :--- | :--- |
| LStyleData | 컴포넌트의 언어별 [StyleData](style-data.md)를 가져오거나 변경합니다. |
| OverrideFont | 언어가 변경될 때 해당 언어에 지정된 폰트로 변경합니다. 폰트가 지정되어 있지 않을 경우 기존의 폰트를 계속 사용합니다. |
| OverrideLineSpacing | 언어가 변경될 때 해당 언어에 지정된 라인 스페이싱으로 변경합니다. 기본값은 1입니다. |
| Font | 컴포넌트의 font 값을 가져옵니다. |
| LineSpacing | 컴포넌트의 lineSpacing 값을 찾아옵니다. Dropdown 에는 해당되지 않습니다. |

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
        <p>UGUI Text, TextMesh &#xAD00;&#xB828; &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C;
          &#xCC3E;&#xC544; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

