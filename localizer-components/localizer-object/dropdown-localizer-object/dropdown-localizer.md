---
description: 'base class : DropdownLocalizerObject'
---

# Dropdown Localizer

UGUI Dropdown 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/dropdown_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OptionSize | 항목의 수를 설정합니다. |
| LOptions | 언어별 드롭다운 옵션들을 지정합니다. 언어가 변경될 경우 컴포넌트의 옵션들이 변경된 언어의 옵션들로 설정됩니다. |

## 레퍼런스

{% code title="DropdownLocalizer.cs" %}
```csharp
public class DropdownLocalizer : DropdownLocalizerObject {
    public UnityEngine.UI.Dropdown Component { get; }
    
    public override LocalizerOptionDataList Options { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Component | UGUI Dropdown 컴포넌트를 가져옵니다. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Inherited Properties</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Options</td>
      <td style="text-align:left">
        <p>UGUI Dropdown&#xC758; options &#xAC12;&#xC744; LocalizerOptionDataList&#xB85C;</p>
        <p>&#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

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
        <p>UGUI Dropdown &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C; &#xCC3E;&#xC544;
          &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

