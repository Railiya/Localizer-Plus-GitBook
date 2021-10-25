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

| Value Definition |                                                                         |
| ---------------- | ----------------------------------------------------------------------- |
| LString          | string 타입의 [LValue\<T>](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| **Properties** |                             |
| -------------- | --------------------------- |
| LText          | 컴포넌트의 언어별 텍스트를 가져오거나 변경합니다. |

| Abstract Properties |                      |
| ------------------- | -------------------- |
| Text                | 컴포넌트의 text 값을 가져옵니다. |

| Inherited Functions |                                                                       |
| ------------------- | --------------------------------------------------------------------- |
| SetComponent ()     | <p>현재 오브젝트에 부착된 컴포넌트를 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |

