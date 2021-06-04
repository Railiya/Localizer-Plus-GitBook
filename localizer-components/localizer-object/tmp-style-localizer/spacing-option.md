# Spacing Option

Text Mesh Pro Text의 각 스페이싱 옵션 값들을 가집니다.‌

## 레퍼런스 <a id="undefined"></a>

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
| character | 텍스트의 각 문자 사이의 간격입니다. |
| word | 텍스트의 각 단어 사이의 간격입니다. |
| line | 텍스트의 라인 사이의 간격입니다. |
| paragraph | 텍스트의 문단 사이의 간격입니다. |

| Constructor |  |
| :--- | :--- |
| SpacingOption | 각 스페이싱 옵션 값들로부터 SpacingOption을 생성합니다. |

| Static Functions |  |
| :--- | :--- |
| FromVector4 | Vector4 값들로부터 SpacingOption을 생성합니다. |



