# Clip Data

Getting audio clip and volume.

## Reference

{% code title="AudioLocalizer.cs" %}
```csharp
public class ClipData { 
    public UnityEngine.AudioClip clip;
    public float volume = 1f;
    
    public ClipData () { }
    public ClipData (UnityEngine.AudioClip clip, float volume = 1f) { }
}
```
{% endcode %}

| Variables |  |
| :--- | :--- |
| clip | Audio clip. |
| volume | Audio volume. |

| Constructors |  |
| :--- | :--- |
| ClipData | Create ClipData from audio clip and volume. |

