# Localizer Option Data

드롭다운 컴포넌트에서 표시되는 항목입니다.

## 레퍼런스

{% code title="LocalizerObject.cs" %}
```csharp
public class LocalizerOptionData { 
    public string text;
    public UnityEngine.Sprite image;
    
    public LocalizerOptionData () { }
    public LocalizerOptionData (string text) { }
    public LocalizerOptionData (string text, Sprite image) { }
}
```
{% endcode %}

| Variables |  |
| :--- | :--- |
| text | 항목에 표시되는 텍스트 입니다. |
| image | 항목에 표시되는 이미지 입니다. |

| Constructors |  |
| :--- | :--- |
| LocalizerOptionData | 텍스트와 이미지로부터 항목을 만듭니다. |



