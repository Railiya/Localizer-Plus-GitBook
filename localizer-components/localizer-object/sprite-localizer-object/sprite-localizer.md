---
description: 'base class : SpriteLocalizerObject'
---

# Sprite Localizer

SpriteRenderer 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/sprite\_localizer\_inspector.PNG)

| Properties |                                                                               |
| ---------- | ----------------------------------------------------------------------------- |
| LSprite    | <p>언어별 스프라이트를 지정합니다. </p><p>언어가 변경될 경우 컴포넌트의 스프라이트가 변경된 언어의 스프라이트로 설정됩니다.</p> |

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

| Properties |                             |
| ---------- | --------------------------- |
| Component  | SpriteRenderer 컴포넌트를 가져옵니다. |

| Inherited Properties |                                       |
| -------------------- | ------------------------------------- |
| Text                 | SpriteRenderer 컴포넌트의 sprite 값을 가져옵니다. |

| Inherited Functions |                                                                            |
| ------------------- | -------------------------------------------------------------------------- |
| SetComponent        | <p>SpriteRenderer 컴포넌트를 찾아 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |
