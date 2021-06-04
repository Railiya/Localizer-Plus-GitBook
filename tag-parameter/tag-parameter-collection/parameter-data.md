# Parameter Data

The class that has defined values of **Tag Parameter**. It used only in **Tag Parameter Collection**.

## Reference

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
| key | The key used to refer. |
| isArray | Whether is array or not. |
| type | Type of parameter. |
| value | Value of parameter. |
| arraySize | Size of array. |

| Functions |  |
| :--- | :--- |
| GetExpectedType | Get expected parameter type from value. |

