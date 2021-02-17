---
description: Tag Parameter 모음집 모음집 스토어
---

# Tag Manager

**Tag Parameter List**를 관리하는 정적 클래스입니다. Tags에 등록된 **Tag Parameter List** 들을 통해 **Tag Formatter** 에서 **Tag Parameter**를 참조합니다. 등록되지 않은 경우 사용할 수 없습니다.

{% hint style="info" %}
**Tag Parameter List** 들은 저 마다 엑세스 키를 가지고 있으며 엑세스 키를 통해 Tags 에서 **Tag Parameter List**를 가져옵니다. 사용이 끝난 **Tag Parameter List** 들은 Tags 에서 제거하여 메모리를 아낄 수 있습니다.
{% endhint %}

## 레퍼런스

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
| [TagCollection](tag-collection.md) | [TagParameterList](../tag-parameter-list/) 컬렉션 입니다. |

| Static Properties |  |
| :--- | :--- |
| Tags | [TagCollection](tag-collection.md) 입니다. |
| MaximumTagParameterArraySize | [TagParameter](../tag-parameter-list/tag-parameter.md)의 최대 배열 크기 입니다. |



