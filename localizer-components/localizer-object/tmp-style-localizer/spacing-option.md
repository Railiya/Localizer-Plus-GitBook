# Spacing Option

Getting spacing option values of Text Mesh Pro Text.‌

## Reference <a id="undefined"></a>

{% code title="TMPStyleLocalizer.cs" %}
```csharp
public struct SpacingOption {
    public float character;
    public float word;
    public float line;
    public float paragraph;
    
    public SpacingOption (float character, float word, float line, float paragraph) { }
    
    public static SpacingOption FromVector4 (UnityEngine.Vector4 vector) { }
}
```
{% endcode %}

| Variables | ​Title |
| :--- | :--- |
| character | Distance of between each characters in text. |
| word | Distance of between each words in text. |
| line | Distance of between lines in text. |
| paragraph | Distance of between paragraphs in text. |

| Constructor |  |
| :--- | :--- |
| SpacingOption | Create SpacingOption from each spacing option values. |

| Static Functions |  |
| :--- | :--- |
| FromVector4 | Create SpacingOption from Vector4. |



