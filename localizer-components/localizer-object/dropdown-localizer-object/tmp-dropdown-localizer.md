---
description: 'base class : DropdownLocalizerObject'
---

# TMP Dropdown Localizer

TMP\_Dropdown 컴포넌트에 사용되는 Localizer 컴포넌트 입니다.

## 컴포넌트

![](../../../.gitbook/assets/tmp\_dropdown\_localizer\_inspector.PNG)

| Properties |                                                                |
| ---------- | -------------------------------------------------------------- |
| OptionSize | 항목의 수를 설정합니다.                                                  |
| LOptions   | 언어별 드롭다운 옵션들을 지정합니다. 언어가 변경될 경우 컴포넌트의 옵션들이 변경된 언어의 옵션들로 설정됩니다. |

## 레퍼런스

{% code title="TMPDropdownLocalizer.cs" %}
```csharp
public class TMPDropdownLocalizer : DropdownLocalizerObject {
    public TMPro.TMP_Dropdown Component { get; }
    
    public override LocalizerOptionDataList Options { get }  
    public override bool SetComponent () { }
}
```
{% endcode %}

| Properties |                           |
| ---------- | ------------------------- |
| Component  | TMP Dropdown 컴포넌트를 가져옵니다. |

| Inherited Properties |                                                                             |
| -------------------- | --------------------------------------------------------------------------- |
| Options              | <p>TMP Dropdown의 options 값을 LocalizerOptionDataList로 </p><p>변환하여 가져옵니다.</p> |

| Inherited Functions |                                                                          |
| ------------------- | ------------------------------------------------------------------------ |
| SetComponent        | <p>TMP Dropdown 컴포넌트를 찾아 설정합니다. </p><p>성공하면 true, 그렇지 않으면 false 입니다.</p> |
