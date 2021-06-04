---
description: Generic type value class in each language
---

# LValue&lt;T&gt;

Generic class that used when you want to use the value by each language such as specific value or object reference. It used in various Localizers likes **LString, LSprite, LOptionDataList** and **LString** is used in **Localized Dictionary, Tag Parameter**.

![LString example of Cube Collector](../.gitbook/assets/lstring_drawer.png)

The name of already defined **LValue&lt;T&gt;** Wrapper classes are start with "L" and It also applied custom property drawer, So it can be serialized in inspector if it is common displayed type. Localizer components are can be serialized by applied extra custom inspector.

## Defined Wrapper Class

Already defined **LValue&lt;T&gt;** Wrapper classes used in **Localized Dictionary** and Localizers.

| Class | Type | Serialize |
| :--- | :--- | :--- |
| LString | LValue&lt;string&gt; | Yes |
| LSprite | LValue&lt;Sprite&gt; | Yes |
| LOptionDataList | LValue&lt;LocalizerOptionDataList&gt; | No |
| LClipData | LValue&lt;AudioLocalizer.ClipData&gt; | No |
| LTexture | LValue&lt;Texture&gt; | Yes |
| LTextStyleData | LValue&lt;TextStyleLocalizer.StyleData&gt; | No |
| LTMPStyleData | LValue&lt;TMPStyleLocalizer.StyleData&gt; | No |

{% hint style="info" %}
Inspector serialize can be possible when the type of T is serialized and the height of line is a single height \(EditorGUIUtility.singleLineHeight\).

These serialize are about just inspector displayed. Actually values are saved normally.
{% endhint %}

## LStringTextArea Attribute

The role of string is important because localization is mainly consist of texts. And you can display it as text area with **LStringTextArea** attribute instead of the common text field.

{% code title="LValue.cs" %}
```csharp
public class LStringTextAreaAttribute : PropertyAttribute {
    public LStringTextAreaAttribute (int height) { }
}
```
{% endcode %}

| Constructor |  |
| :--- | :--- |
| LStringTextAreaAttribute | Draw text area with specific height. The range is 1 to 50. |

The follow example is a part of GameManager script and inspector in Cube Collector example.

{% code title="GameManager.cs" %}
```csharp
public class GameManager : MonoBehaviour {
    [SerializeField, LStringTextArea (2)] LString help_talk = null;
    [SerializeField, LStringTextArea (2)] LString help_continue = null;
    [SerializeField, LStringTextArea (2)] LString help_done = null;
}
```
{% endcode %}

![](../.gitbook/assets/lstring_textarea_drawer.png)

You can edit string values of each language in a combo box on the right side of Language Label.

## Reference

{% code title="LValue.cs" %}
```csharp
public class LValue<T> {
    public LValue () { }
    public LValue (LValue<T> value) { }
    public LValue (T[] value) { }

    public T this[string language] { get; set; }
    public T this[UnityEngine.SystemLanguage language] { get; set; }
    public T this[int index] { get; set; }

    public int Count { get; }
    public T Value { get; set; }

    public override string ToString () { }
}
```
{% endcode %}

| Constructor |  |
| :--- | :--- |
| LValue | Create empty LValue or create from LValue&lt;T&gt;, T array. |

| Indexer |  |
| :--- | :--- |
| this | Get or set the value by LanguageText, SystemLanguage or index. |

| Properties |  |
| :--- | :--- |
| Count | Get number of values. The count can be different if languages are not updated. |
| Value | Get or set the value of current applied language. |

| Inherits Functions |  |
| :--- | :--- |
| ToString | Get ToString value of current applied language. |

