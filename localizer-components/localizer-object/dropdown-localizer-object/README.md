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

| Value Definition |                                                                                                                         |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------- |
| LOptionDataList  | [LocalizerOptionDataList ](localizer-option-data-list/)타입의 [LValue\<T>](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| **Properties** |                                  |
| -------------- | -------------------------------- |
| LOptions       | 컴포넌트의 언어별 드롭다운 옵션들을 가져오거나 변경합니다. |

| Abstract Properties |                        |
| ------------------- | ---------------------- |
| Options             | 컴포넌트의 드롭다운 옵션들을 가져옵니다. |

| Inherited Functions |                                                                       |
| ------------------- | --------------------------------------------------------------------- |
| SetComponent ()     | <p>현재 오브젝트에 부착된 컴포넌트를 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |
