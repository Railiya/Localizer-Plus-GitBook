---
description: Tag Parameter 모음집
---

# Tag Parameter List

**Tag Parameter**를 관리하는 클래스 입니다. **Tag Parameter List**는 엑세스 키를 가지며 **Tag Manager**에서 엑세스 키를 통해 **Tag Parameter List**를 가져옵니다.&#x20;

{% hint style="info" %}
**Tag Parameter List**는 **Tag Manager**의 Tags에 등록해야 사용할 수 있습니다.
{% endhint %}

## 레퍼런스

{% code title="TagParameterList.cs" %}
```csharp
public enum TagParameterType { }

public class TagParameterList {
    public TagParameterList (string accessKey) { }
    
    public TagParameter this[string key] { get; }
    public string AccessKey { get; }
    
    public bool Add (string key, TagParameter parameter) { }
    public TagParameter Add (string key, int value) { }
    public TagParameter Add (string key, float value) { }
    public TagParameter Add (string key, bool value) { }
    public TagParameter Add (string key, string value) { }
    public TagParameter Add (string key, LString value) { }
    public TagParameter AddArray (string key, TagParameterType type, int capacity = 4) { }
    public void Remove (string key) { }
    public void Clear () { }  
}
```
{% endcode %}

| Constructor      |                                    |
| ---------------- | ---------------------------------- |
| TagParameterList | 엑세스 키를 가진 TagParameterList를 생성합니다. |

| Indexer |                                                 |
| ------- | ----------------------------------------------- |
| this    | 해당 key의 [TagPrameter](tag-parameter.md)를 가져옵니다. |

| Properties |                                                                               |
| ---------- | ----------------------------------------------------------------------------- |
| AccessKey  | [TagCollection](../tag-manager/tag-collection.md)의 TagParameterList 접근 키 입니다. |

| Functions |                                                                                              |
| --------- | -------------------------------------------------------------------------------------------- |
| Add       | [TagParameter](tag-parameter.md)를 추가합니다. key가 이미 있다면 false를 반환합니다.                           |
| Add       | [TagParameter](tag-parameter.md)를 추가합니다. 생성된 [TagPrameter](tag-parameter.md)를 반환합니다.         |
| AddArray  | 배열 형식의 [TagParameter](tag-parameter.md)를 추가합니다. 생성된 [TagParameter](tag-parameter.md)를 반환합니다. |
| Remove    | 특정 key의 [TagParameter](tag-parameter.md)를 제거합니다.                                             |
| Clear     | 보유중인 [TagParameter](tag-parameter.md)들을 제거합니다.                                               |
