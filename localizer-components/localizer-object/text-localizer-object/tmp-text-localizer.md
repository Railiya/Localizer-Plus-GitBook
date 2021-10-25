---
description: 'base class : TextLocalizerObject'
---

# TMP Text Localizer

TextMeshPro 및 TextMeshProUGUI 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/tmp\_text\_localizer\_inspector.PNG)

| Properties |                                                           |
| ---------- | --------------------------------------------------------- |
| LText      | 언어별 텍스트를 지정합니다. 언어가 변경될 경우 컴포넌트의 텍스트가 변경된 언어의 텍스트로 설정됩니다. |

## 레퍼런스

{% code title="TMPTextLocalizer.cs" %}
```csharp
public class TMPTextLocalizer : TextLocalizerObject {
    public TMPro.TMP_Text Component { get; }
    
    public override string Text { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |                        |
| ---------- | ---------------------- |
| Component  | TMP\_Text 컴포넌트를 가져옵니다. |

| Inherited Properties |                                |
| -------------------- | ------------------------------ |
| Text                 | TMP\_Text 컴포넌트의 text 값을 가져옵니다. |

| Inherited Functions |                                                                      |
| ------------------- | -------------------------------------------------------------------- |
| SetComponent        | <p>TMP_Text 컴포넌트를 찾아 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |

