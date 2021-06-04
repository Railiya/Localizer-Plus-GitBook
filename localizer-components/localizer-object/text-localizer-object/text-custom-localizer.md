---
description: 'base class : TextLocalizerObject'
---

# Text Custom Localizer

사용자 지정 텍스트 Localizer 컴포넌트 입니다. 요구 컴포넌트가 없습니다. 언어가 변경될 경우 실제 텍스트가 변경되지 않고 **OnTextChanged** 이벤트가 호출됩니다.

## 컴포넌트

![](../../../.gitbook/assets/text_custom_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LText | 언어별 텍스트를 지정합니다. |
| OnTextChanged | 언어가 변경될 경우 변경된 언어의 텍스트를 인수로 받으며 호출됩니다. |

## 레퍼런스

{% code title="TextCustomLocalizer.cs" %}
```csharp
public class TextCustomLocalizer : TextLocalizerObject {
    public class TextChangeEvent : UnityEvent<string> { }
    
    public TextChangeEvent OnTextChanged { get; }
    
    public override string Text { get }
    public override bool SetComponent () { }
}
```
{% endcode %}

| Inner Class |  |
| :--- | :--- |
| TextChangeEvent | string 타입의 UnityEvent&lt;T&gt; Wrapper 클래스입니다. |

| Properties |  |
| :--- | :--- |
| OnTextChanged | 언어가 변경될 때 변경된 언어의 텍스트와 함께 호출되는 이벤트 입니다. |

| Inherited Properties |  |
| :--- | :--- |
| Text | 마지막으로 설정된 text 값을 가져옵니다. |

| Inherited Functions |  |
| :--- | :--- |
| SetComponent | 별도의 컴포넌트가 필요치 않기에 항상 false를 반환합니다. |

