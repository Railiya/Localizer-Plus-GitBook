# Clip Data

오디오 클립 및 볼륨의 정보를 가집니다.

## 레퍼런스

{% code title="AudioLocalizer.cs" %}
```csharp
public class ClipData { 
    public UnityEngine.AudioClip clip;
    public float volume;
    
    public ClipData () { }
    public ClipData (UnityEngine.AudioClip clip, float volume = 1f) { }
}
```
{% endcode %}

| Variables |  |
| :--- | :--- |
| clip | 오디오 클립입니다. |
| volume | 오디오 볼륨입니다. |

| Constructors |  |
| :--- | :--- |
| ClipData | 오디오 클립과 볼륨으로부터 ClipData를 생성합니다. |

