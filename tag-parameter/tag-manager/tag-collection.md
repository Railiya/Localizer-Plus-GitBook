# Tag Collection

The **Tag Parameter List** collection class. Can get from Tags in **Tag Manager**.

## Reference

{% code title="TagManager.cs" %}
```csharp
public class TagCollection {
    public TagParameterList this[string accessKey] { get; }
    
    public int Count { get; }
    public Dictionary<string, TagParameterList>.ValueCollection AccessibleList { get; }
    
    public bool AddList (string accessKey) { }
    public bool AddList (TagParameterList list) { }
    public void RemoveList (string accessKey) { }
    public void RemoveList (TagParameterList list) { }
    public bool ContainsList (string accessKey) { }
    public bool ContainsList (TagParameterList list) { }
}
```
{% endcode %}

| Indexer |  |
| :--- | :--- |
| this | Get [TagParameterList](../tag-parameter-list/) by access key. |

| Properties |  |
| :--- | :--- |
| Count | Get number of [TagParameterList ](../tag-parameter-list/)has. |
| AccessibleList | Get [TagParameterList ](../tag-parameter-list/)collection. |

| Functions |  |
| :--- | :--- |
| AddList | Add [TagParameterList](../tag-parameter-list/). Return false if access key already exists. |
| RemoveList | Clear contents of [TagParameterList](../tag-parameter-list/) and remove. |
| ContainsList | Return existence of [TagParameterList](../tag-parameter-list/). |



