---
description: 미리 만들어 쓰는 Tag Parameter 모음집
---

# Tag Parameter Collection

**Tag Parameter**를 정의하는 **Parameter Data**를 가지는 컬렉션 스크립터블 오브젝트 입니다. 이는 에디터 단계에서 미리 **Tag Parameter**들을 정의하고 런타임에서 **Tag Parameter List**를 로드하여 **Tag Manager**에 등록하고 본 에셋의 메모리를 해제하는 방식으로 사용됩니다.

## 스크립터블 오브젝트

![Cube Collector &#xC608;&#xC81C;&#xC758; &#xC608;&#xC2DC; \(unused&#xB294; &#xC608;&#xC81C;&#xC5D0; &#xC5C6;&#xC74C;\)](../../.gitbook/assets/tag_parameter_collection_inspector.png)

| Management |  |
| :--- | :--- |
| Fold All | [ParameterData](parameter-data.md) 항목들을 모두 접습니다. |
| Unfold All | [ParameterData](parameter-data.md) 항목들을 모두 펼칩니다. |
| Sort Keys | [ParameterData](parameter-data.md) 항목들을 Key 기준으로 정렬합니다. |

| Filters |  |
| :--- | :--- |
| Keys | 특정 키워드를 포함한 항목들만 표시합니다. |
| Filter | 해당 형식의 항목들을 표시합니다. |
| Clear Filters | 필터를 모두 초기화합니다. |

| Access |  |
| :--- | :--- |
| Access Key | [TagParameterList](../tag-parameter-list/)의 엑세스 키 입니다. |

| Parameter Data |  |
| :--- | :--- |
| Expected Type | 항목이 로드될 때 정해지는 파라미터 형식입니다. |
| Key | [TagParameter](../tag-parameter-list/tag-parameter.md)에 접근할 때 사용되는 key 입니다. |
| Value | [TagParameter](../tag-parameter-list/tag-parameter.md)의 값 입니다. |
| Is Array | [TagParameter](../tag-parameter-list/tag-parameter.md)의 배열 여부입니다. |
| Type | [TagParameter ](../tag-parameter-list/tag-parameter.md)배열의 파라미터 형식입니다. |
| Size | [TagParameter](../tag-parameter-list/tag-parameter.md) 배열의 크기입니다.  |

{% hint style="info" %}
**Parameter Data의 Expected Type**은 Foldout Label의 우측에 표시되며 Value, Is Array, Type에 영향을 받아 표시됩니다. **Tag Parameter Collection** 에서는 **LString** 형식을 사용할 수 없습니다.
{% endhint %}

## 레퍼런스

{% code title="TagParameterCollection.cs" %}
```csharp
public class TagParameterCollection : ScriptableObject {
    public string accessKey;
    public List<ParameterData> datas;
    
    public TagParameterList void Load (bool unloadOnComplete = true) { }
}
```
{% endcode %}

| Variables |  |
| :--- | :--- |
| accessKey | 로드되는 [TagParameterList](../tag-parameter-list/)의 엑세스 키 입니다. |
| datas | [ParameterData](parameter-data.md) 리스트 입니다. |

| Functions |  |
| :--- | :--- |
| Load | [ParameterData](parameter-data.md)들을 [TagParameter](../tag-parameter-list/tag-parameter.md)로 변환하여 엑세스 키를 가진 [TagParameterList](../tag-parameter-list/)를 생성한 후  [TagManager](../tag-manager/)에 등록합니다. unloadOnComplete가 true라면 로드가 끝난 뒤 Resources.UnloadAsset을 호출하여 에셋을 메모리에서 해제합니다. 로드된 TagParameterList를 반환합니다. 엑세스 키가 이미 있거나 비었다면 null을 반환합니다. |

