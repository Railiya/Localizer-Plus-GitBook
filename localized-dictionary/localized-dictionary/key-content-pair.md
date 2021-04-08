---
description: LString collection
---

# Key Content Pair

The class has **LString** list. You can get **LString** by key or index.

## Reference

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
| this | Get [LString](../../lvalue/lvalue-type.md) by index or key. |

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
        <p>Get or set name of KeyContentPair.</p>
        <p>(Refer : It used as key in <a href="./">Localized Dictionary</a>.)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Keys</td>
      <td style="text-align:left">Get keys from list.</td>
    </tr>
    <tr>
      <td style="text-align:left">Count</td>
      <td style="text-align:left">Get number of keys.</td>
    </tr>
  </tbody>
</table>

| Functions |  |
| :--- | :--- |
| AddContent | Add [LString](../../lvalue/lvalue-type.md). |
| RefreshLStrings | Update [LString](../../lvalue/lvalue-type.md) language settings in list. |
| Clear | Remove all [LString](../../lvalue/lvalue-type.md) in list. |

