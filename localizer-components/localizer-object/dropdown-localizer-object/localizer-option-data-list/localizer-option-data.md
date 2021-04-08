# Localizer Option Data

Elements displays in dropdown component.

## Reference

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
| text | Displayed text in element. |
| image | Displayed image in element. |

| Constructors |  |
| :--- | :--- |
| LocalizerOptionData | Create element from text and image. |



