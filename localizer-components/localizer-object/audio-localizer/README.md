---
description: 'base class : LocalizerObject'
---

# Audio Localizer

AudioSource 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/audio\_localizer\_inspector.PNG)

| Properties |                                                                          |
| ---------- | ------------------------------------------------------------------------ |
| LClipData  | 언어별 오디오 클립 및 볼륨을 지정합니다. 언어가 변경될 경우 컴포넌트의 오디오 클립 및 볼륨이 변경된 언어의 것으로 설정됩니다. |

## 레퍼런스

{% code title="AudioLocalizer.cs" %}
```csharp
public class AudioLocalizer : LocalizerObject {    
    public class ClipData { }

    public UnityEngine.AudioSource Component { get; }
    
    public LClipData LClipData { get; set; }
    public UnityEngine.AudioClip Clip { get; }
    public float Volume { get; }
 
    public override bool SetComponent () { }
}
```
{% endcode %}

| Inner Class              |                        |
| ------------------------ | ---------------------- |
| [ClipData](clip-data.md) | 오디오 클립 및 볼륨의 정보를 가집니다. |

| Value Definition |                                                                                           |
| ---------------- | ----------------------------------------------------------------------------------------- |
| LClipData        | [ClipData](clip-data.md) 타입의 [LValue\<T>](../../../lvalue/lvalue-type.md) Wrapper 클래스입니다. |

| Properties |                                                  |
| ---------- | ------------------------------------------------ |
| Component  | AudioSource 컴포넌트를 가져옵니다.                         |
| LClipData  | 컴포넌트의 언어별 [ClipData](clip-data.md)를 가져오거나 변경합니다. |
| Clip       | 컴포넌트의 clip 값을 가져옵니다.                             |
| Volume     | 컴포넌트의 volume 값을 가져옵니다.                           |

| Inherited Functions |                                                                         |
| ------------------- | ----------------------------------------------------------------------- |
| SetComponent        | <p>AudioSource 컴포넌트를 찾아 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |
