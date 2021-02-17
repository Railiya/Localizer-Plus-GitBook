# Tag Parameter

**Tag Formatter** 에서 사용되는 특정 값을 가진 태그입니다. 

{% hint style="info" %}
**Tag Parameter**는 생성될 때 **Tag Parameter Type**을 가지며 값을 가져오거나 설정할 때 형식과 일치해야만 정상적으로 동작합니다. 다만 String 값은 형식과 관계 없이 가져올 수 있습니다. 

값이 변경될 경우 참조되어 있는 **Tag Formatter** 들의 Refresh를 호출합니다.
{% endhint %}

{% hint style="warning" %}
String과 **LString**을 제외한 값을 가져오거나 설정할 때는 파싱과 ToString 을 통해 string으로 내부에 보관됩니다. 따라서 Update 내의 호출과 같이 잦은 호출은 GC에 영향을 줄 수 있습니다.
{% endhint %}

## 레퍼런스

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
| TagParameter | 파라미터 형식과 배열 여부로부터 TagParameter를 생성합니다. |

| Indexer |  |
| :--- | :--- |
| this | 인덱스를 통해 하위 TagParameter를 가져옵니다. 배열이 아닐 경우 null을 반환합니다. |

| Properties |  |
| :--- | :--- |
| Type | 보유중인 값의 형식입니다. |
| TagReference | 텍스트에서 사용되는 TagParameter의 참조 형식입니다. |
| IsArray | 배열의 여부입니다. |
| ArrayCapacity | 배열의 버퍼 크기입니다. 최대 크기는 [TagManager](../tag-manager/)의 MaximumTagParameterArraySize 입니다. |
| ArraySize | 배열의 크기입니다. 배열이 아닐 경우 -1을 반환합니다. |
| Int | int 값을 가져오거나 설정합니다. |
| Float | float 값을 가져오거나 설정합니다. |
| Bool | bool 값을 가져오거나 설정합니다. |
| String | 파라미터 형식과 상관없이 string 값을 가져오거나 설정합니다. |
| LString | [LString](../../lvalue/lvalue-type.md) 값을 가져오거나 설정합니다. |

{% hint style="info" %}
배열 형식의 **Tag Parameter**는 값을 가지지 않습니다. 인덱서를 통해 값을 가진 하위 **Tag Parameter**를 가져올 수 있습니다.

배열의 크기를 초과한 인덱스가 호출되거나 설정 할 경우 자동적으로 버퍼의 크기가 확장됩니다. 다만 이 크기는 **Tag Manager**의 MaximumTagParameterArraySize 를 초과하지 않습니다.
{% endhint %}

