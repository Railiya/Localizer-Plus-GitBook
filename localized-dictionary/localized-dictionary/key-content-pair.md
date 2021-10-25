---
description: LString 모음집
---

# Key Content Pair

**LString** 들을 가지는 클래스입니다. 키와 인덱스로부터 **LString**을 가져올 수 있습니다.

## 레퍼런스

{% code title="LocalizedDictionary.cs" %}
```csharp
public class KeyContentPair {
    public LString this[int index] { get; }
    public LString this[string key] { get; }

    public string Name { get; set; }
    public List<string> Keys { get; }
    public int Count { get; }
    
    public void AddContent (string key, LString content) { }
    public void RefreshLStrings () { }
    public void Clear () { }
}
```
{% endcode %}

| Indexer |                                                             |
| ------- | ----------------------------------------------------------- |
| this    | 인덱스 또는 키를 통해 [LString](../../lvalue/lvalue-type.md)을 가져옵니다. |

| Properties |                                                                                                         |
| ---------- | ------------------------------------------------------------------------------------------------------- |
| Name       | <p>KeyContentPair의 이름을 가져오거나 설정합니다. </p><p>(참고 : <a href="./">Localized Dictionary</a>에서 키로 사용됩니다.)</p> |
| Keys       | 보유중인 key들을 리스트로 가져옵니다.                                                                                  |
| Count      | 보유중인 key의 수를 가져옵니다.                                                                                     |

| Functions       |                                                             |
| --------------- | ----------------------------------------------------------- |
| AddContent      | [LString](../../lvalue/lvalue-type.md)을 추가합니다.              |
| RefreshLStrings | 보유중인 [LString](../../lvalue/lvalue-type.md)들의 언어 설정을 갱신합니다. |
| Clear           | 보유중인 [LString](../../lvalue/lvalue-type.md)들을 제거합니다.        |
