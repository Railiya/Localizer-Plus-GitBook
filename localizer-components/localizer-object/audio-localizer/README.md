---
description: 'base class : LocalizerObject'
---

# Audio Localizer

AudioSource 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/audio_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| LClipData | 언어별 오디오 클립 및 볼륨을 지정합니다. 언어가 변경될 경우 컴포넌트의 오디오 클립 및 볼륨이 변경된 언어의 것으로 설정됩니다. |

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

| Inner Class |  |
| :--- | :--- |
| [ClipData](clip-data.md) | 오디오 클립 및 볼륨의 정보를 가집니다. |

| Value Definition |  |
| :--- | :--- |
| LClipData | [ClipData](clip-data.md) 타입의 LValue&lt;T&gt; Wrapper 클래스입니다. |

| Properties |  |
| :--- | :--- |
| Component | AudioSource 컴포넌트를 가져옵니다. |
| LClipData | 컴포넌트의 언어별 [ClipData](clip-data.md)를 가져오거나 변경합니다. |
| Clip | 컴포넌트의 clip 값을 가져옵니다. |
| Volume | 컴포넌트의 volume 값을 가져옵니다. |

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
        <p>AudioSource &#xCEF4;&#xD3EC;&#xB10C;&#xD2B8;&#xB97C; &#xCC3E;&#xC544;
          &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>&#xC131;&#xACF5;&#xD558;&#xBA74; true, &#xADF8;&#xB807;&#xC9C0; &#xC54A;&#xC73C;&#xBA74;
          false &#xC785;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

