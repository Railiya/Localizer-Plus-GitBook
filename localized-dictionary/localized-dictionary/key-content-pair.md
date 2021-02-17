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

| Indexer |  |
| :--- | :--- |
| this | 인덱스 또는 키를 통해 [LString](../../lvalue/lvalue-type.md)을 가져옵니다. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Properties</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">
        <p>KeyContentPair&#xC758; &#xC774;&#xB984;&#xC744; &#xAC00;&#xC838;&#xC624;&#xAC70;&#xB098;
          &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>(&#xCC38;&#xACE0; : <a href="./">Localized Dictionary</a>&#xC5D0;&#xC11C;
          &#xD0A4;&#xB85C; &#xC0AC;&#xC6A9;&#xB429;&#xB2C8;&#xB2E4;.)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Keys</td>
      <td style="text-align:left">&#xBCF4;&#xC720;&#xC911;&#xC778; key&#xB4E4;&#xC744; &#xB9AC;&#xC2A4;&#xD2B8;&#xB85C;
        &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">Count</td>
      <td style="text-align:left">&#xBCF4;&#xC720;&#xC911;&#xC778; key&#xC758; &#xC218;&#xB97C; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

| Functions |  |
| :--- | :--- |
| AddContent | [LString](../../lvalue/lvalue-type.md)을 추가합니다. |
| RefreshLStrings | 보유중인 [LString](../../lvalue/lvalue-type.md)들의 언어 설정을 갱신합니다. |
| Clear | 보유중인 [LString](../../lvalue/lvalue-type.md)들을 제거합니다. |

