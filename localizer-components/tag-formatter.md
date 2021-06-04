---
description: Core of core of asset for someone
---

# Tag Formatter

The component used in **Text Localizer Object**, UGUI Text, TextMesh, TextMeshPro, TextMeshProUGUI. It replaces specific tags to string in text.

{% hint style="info" %}
Using with **Text Localizer Object** component, You can just use existing LText editing method. It does not need extra works. If you're not, you have to use it by set Format in **Tag Formatter**.

To use **Tag Parameter** function, **Tag Parameter List** is register to **Tag Manager**. **Tag Formatter** will refer to **Tag Parameter** from **Tag Parameter List** and replace tags of text into value of **Tag Parameter**. If **Tag Parameter** is not exist, It will not be replaced.
{% endhint %}

## Component

![](../.gitbook/assets/tag_formatter_inspector.png)

No editable variables.

{% hint style="info" %}
When LText or Text value is changed, It refers to tags from text and caching **Tag Parameters** inside. If **Tag Parameter** value is changed, It calls Refresh automatically.
{% endhint %}

## Tag Typing Format

![Cube Collector &#xC608;&#xC81C;&#xC758; &#xC608;&#xC2DC;](../.gitbook/assets/tag_typing_example.png)

A Common tag writing method is writing tag reference inside {}. The tag reference is writing access key of List and attach : finally write key of Tag Parameter. If **Tag Parameter** is array type, attach indexer with index additionally.

* Tag Reference Format
* Common Type : {accessKey:parameterKey}
* Array Type : {accessKey:parameterKey\[index\]}

For instance of tag typing, there is a **Tag Parameter List** with has Access Key for "quest". And there are "current" and "left" key of **Tag Parameters** in List, You can use it like upper example.

## Reference

{% code title="TagFormatter.cs" %}
```csharp
public class TagFormatter : MonoBehaviour {    
    public string Text { get; set; }
    public Format { get; set; }

    public void SetTextComponent () { }
    public void Refresh () { }

    public static string FormatToText (string format) { }
    public static string FormatToText (List<TagParameter> tags, string format) { }
}
```
{% endcode %}

| Properties |  |
| :--- | :--- |
| Text | Get or set text value of component. |
| Format | Get or set tag format applied text of component. |

| Functions |  |
| :--- | :--- |
| SetTextComponent | Find and set Localizer or Text related component. |
| Refresh | Update text of component with current has format. \(Refer : It called automatically if tag value has changed.\) |

| Static Functions |  |
| :--- | :--- |
| FormatToText | Get text replaced tags to string from input format. |

