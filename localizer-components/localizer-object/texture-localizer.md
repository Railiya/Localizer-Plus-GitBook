---
description: 'base class : LocalizerObject'
---

# Texture Localizer

MeshRenderer 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../.gitbook/assets/texture\_localizer\_inspector.PNG)

| Properties        |                                                                                                                                                                                   |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UseSharedMaterial | sharedMaterial의 mainTexture를 변경합니다. 이 작업은 매트리얼을 공유하는 모든 렌더러들에게 영향을 줍니다. 기본값은 true 입니다. 비활성화 시 렌더러의 인스턴스 material 의 texture를 변경합니다. **이 작업은 에디터 상태에서는 이루어지지 않으며 비활성화를 권장하지 않습니다.** |
| LTexture          | 언어별 텍스처를 지정합니다. 언어가 변경될 경우 컴포넌트의 매트리얼 메인 텍스처가 변경된 언어의 텍스처로 설정됩니다.                                                                                                                 |

## 레퍼런스

{% code title="TextureLocalizer.cs" %}
```csharp
public class TextureLocalizer : LocalizerObject {    
    public UnityEngine.MeshRenderer Component { get; }
    
    public LTexture LTexture { get; set; }
    public UnityEngine.Texture Texture { get; }
    public bool UseSharedMaterial { get; set; }
 
    public override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |                                                                       |
| ---------------- | --------------------------------------------------------------------- |
| LTexture         | Texture 타입의 [LValue\<T>](../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| Properties        |                                                                                                |
| ----------------- | ---------------------------------------------------------------------------------------------- |
| Component         | MeshRenderer 컴포넌트를 가져옵니다.                                                                      |
| LTexture          | 컴포넌트의 언어별 텍스처를 가져오거나 변경합니다.                                                                    |
| Texture           | 컴포넌트의 매트리얼 mainTexture 값을 가져옵니다.                                                               |
| UseSharedMaterial | sharedMaterial의 mainTexture를 변경합니다. 비활성화 시 렌더러의 인스턴스 material 의 texture를 변경합니다. 기본값은 true 입니다. |

| Inherited Functions |                                                                          |
| ------------------- | ------------------------------------------------------------------------ |
| SetComponent        | <p>MeshRenderer 컴포넌트를 찾아 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |
