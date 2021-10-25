---
description: 'base class : LocalizerObject'
---

# Sprite Localizer Object

**Sprite Localizer, Image Localizer**의 베이스 클래스입니다.

## 레퍼런스

{% code title="LocalizerObject.cs" %}
```csharp
public class LSprite : LValue<UnityEngine.Sprite> { }

public SpriteLocalizerObject : LocalizerObject {
    public LSprite LSprite { get; set; }
    
    public abstract UnityEngine.Sprite Sprite { get; }
    public abstract override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |                                                                         |
| ---------------- | ----------------------------------------------------------------------- |
| LSprite          | Sprite 타입의 [LValue\<T>](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| **Properties** |                               |
| -------------- | ----------------------------- |
| LSprite        | 컴포넌트의 언어별 스프라이트를 가져오거나 변경합니다. |

| Abstract Properties |                     |
| ------------------- | ------------------- |
| Sprite              | 컴포넌트의 스프라이트를 가져옵니다. |

| Inherited Functions |                                                                       |
| ------------------- | --------------------------------------------------------------------- |
| SetComponent ()     | <p>현재 오브젝트에 부착된 컴포넌트를 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |

