# Tag Collection

**Tag Manager**의 Tags 를 통해 참조 가능한 **Tag Parameter List** 컬렉션 클래스 입니다. 

## 레퍼런스

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
| this | 엑세스 키를 통해 [TagParameterList](../tag-parameter-list/)를 가져옵니다. |

| Properties |  |
| :--- | :--- |
| Count | 보유중인 [TagParameterList ](../tag-parameter-list/)수를 가져옵니다. |
| AccessibleList | 보유중인 [TagParameterList ](../tag-parameter-list/)컬렉션을 가져옵니다. |

| Functions |  |
| :--- | :--- |
| AddList | [TagParameterList](../tag-parameter-list/)를 추가합니다. 엑세스 키가 이미 있다면 false를 반환합니다. |
| RemoveList | [TagParameterList](../tag-parameter-list/)의 내용을 초기화하고 제거합니다.  |
| ContainsList | [TagParameterList](../tag-parameter-list/)의 존재 여부를 반환합니다. |



