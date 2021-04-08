# Tag Parameter

The tag with has a specific value used in **Tag Formatter**.

{% hint style="info" %}
When **Tag Parameter** created, It has **Tag Parameter Type**. Only can get or set the value if type is matched. But you can get String value regardless of type.

When value is changed, It calls Refresh of referred **Tag Formatter**.
{% endhint %}

{% hint style="warning" %}
When get or set the value that not String or **LString** type, It saves value as string by parse or use ToString. So it can be affect to GC if you call frequently likes Update.
{% endhint %}

## Reference

{% code title="TagParameterList.cs" %}
```csharp
public class TagParameter {
    public TagParameter (TagParameterType type, bool isArray = false) { }

    public TagParameter this[int index] { get; }

    public TagParameterType Type { get; }
    public string TagReference { get; }
    public bool IsArray { get; }
    public int ArrayCapacity { get; set; }
    public int ArraySize { get; }  
    public int Int { get; set; }
    public float Float { get; set; }
    public bool Bool { get; set; }
    public string String { get; set; }
    public LString LString { get; set; }
}
```
{% endcode %}

| Constructor |  |
| :--- | :--- |
| TagParameter | Create TagParameter from parameter type and array. |

| Indexer |  |
| :--- | :--- |
| this | Get sub TagParameter by index. Return null if it's not array. |

| Properties |  |
| :--- | :--- |
| Type | Parameter type of value. |
| TagReference | Reference format of TagParameter used in text. |
| IsArray | Return whether Its array or not. |
| ArrayCapacity | Capacity size of the array. Maximum is MaximumTagParameterArraySize in [TagManager](../tag-manager/). |
| ArraySize | Size of array. Return -1 if it's not array. |
| Int | Get or set int value. |
| Float | Get or set float value. |
| Bool | Get or set bool value. |
| String | Get string value regardless of parameter type or set string value. |
| LString | Get or set [LString](../../lvalue/lvalue-type.md). |

{% hint style="info" %}
Array type **Tag Parameter** doesn't have value. You can get sub Tag Parameter by indexer.

If index that over the array size called or set, buffer size will be expanded automatically. The size doesn't exceed the MaximumTagParameterArraySize in **Tag Manager**.
{% endhint %}

