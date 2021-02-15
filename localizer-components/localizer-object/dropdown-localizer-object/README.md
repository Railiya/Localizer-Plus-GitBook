---
description: 'base class : LocalizerObject'
---

# Dropdown Localizer Object

**Dropdown Localizer, TMP Dropdown Localizer**의 베이스 클래스입니다.

Dropdown 과 TMP\_Dropdown에서 사용되는 OptionData 형식이 다르기 때문에 이 둘을 호환시켜주기 위해 **LocalizerOptionData**와 **LocalizerOptionDataList**를 사용합니다. 또한 편의성을 위해 상호간 변환 확장 함수가 제공됩니다.

## 레퍼런스

{% code title="LocalizerObject.cs" %}
```csharp
public class LOptionDataList : LValue<LocalizerOptionDataList> { }

public DropdownLocalizerObject : LocalizerObject {
    public LOptionDataList LOptions { get; set; }
    
    public abstract LocalizerOptionDataList Options { get; }
    public abstract override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |  |
| :--- | :--- |
| LOptionDataList | [LocalizerOptionDataList ](localizer-option-data-list.md)타입의 LValue&lt;T&gt; Wrapper 클래스입니다. |

| **Properties** |  |
| :--- | :--- |
| LOptions | 컴포넌트의 언어별 드롭다운 옵션들을 가져오거나 변경합니다. |

| Abstract Properties |  |
| :--- | :--- |
| Options | 컴포넌트의 드롭다운 옵션들을 가져옵니다. |

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

