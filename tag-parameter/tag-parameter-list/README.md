---
description: Tag Parameter collection
---

# Tag Parameter List

The class that manage the **Tag Parameter**. **Tag Parameter List** has an access key, and can get **Tag Parameter List** from **Tag Manager** by access key.

{% hint style="info" %}
**Tag Parameter List** can be used when registered in Tags of **Tag Manager**.
{% endhint %}

## Reference

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

| Constructor |  |
| :--- | :--- |
| TagParameterList | Create TagParameterList with access key. |

| Indexer |  |
| :--- | :--- |
| this | Get [TagPrameter](tag-parameter.md) by key. |

| Properties |  |
| :--- | :--- |
| AccessKey | The access key of TagParameterList in [TagCollection](../tag-manager/tag-collection.md). |

| Functions |  |
| :--- | :--- |
| Add | Add [TagParameter](tag-parameter.md). Return false if key exists. |
| Add | Add [TagParameter](tag-parameter.md). Return created [TagPrameter](tag-parameter.md). |
| AddArray | Add array type [TagParameter](tag-parameter.md). Return created [TagParameter](tag-parameter.md). |
| Remove | Remove [TagParameter](tag-parameter.md) by key. |
| Clear | Remove all [TagParameter](tag-parameter.md) in list. |

