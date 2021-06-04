# Parameter Data

**Tag Parameter**를 정의하는 값들을 가진 클래스 입니다. **Tag Parameter Collection** 에서만 사용됩니다.

## 레퍼런스

{% code title="TagParameterCollection.cs" %}
```csharp
public class ParameterData {
    public string key;
    public bool isArray;
    public TagParameterType type;
    public string value;
    public int arraySize;
    
    public TagParameterType GetExpectedType () { }
}
```
{% endcode %}

| Variables |  |
| :--- | :--- |
| key | 참조에 사용되는 key 입니다. |
| isArray | 배열 여부입니다. |
| type | 파라미터 형식입니다. |
| value | 파라미터의 값 입니다. |
| arraySize | 배열의 크기 입니다. |

| Functions |  |
| :--- | :--- |
| GetExpectedType | value에 의한 추측 파라미터 형식을 가져옵니다. |

