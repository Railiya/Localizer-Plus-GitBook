---
description: Tag Parameter collection collection store
---

# Tag Manager

The static class that manage **Tag Parameter List**. **Tag Formatter** can refer to **Tag Parameter** by registered **Tag Parameter List** in Tags. It can't be used if it's not registered.

{% hint style="info" %}
Every **Tag Parameter Lists** are has access key and can get **Tag Parameter** from Tags by key. You can remove **Tag Parameter** List from Tags to release the memory.
{% endhint %}

## Reference

{% code title="TagManager.cs" %}
```csharp
public static class TagManager {
    public class TagCollection { }
    
    public static TagCollection Tags { get; }
    public static int MaximumTagParameterArraySize { get; set; }
}
```
{% endcode %}

| Inner Class |  |
| :--- | :--- |
| [TagCollection](tag-collection.md) | [TagParameterList](../tag-parameter-list/) collection. |

| Static Properties |  |
| :--- | :--- |
| Tags | This is [TagCollection](tag-collection.md). |
| MaximumTagParameterArraySize | Maximum array size of [TagParameter](../tag-parameter-list/tag-parameter.md). |



