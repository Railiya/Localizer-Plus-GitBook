---
description: 'base class : LocalizerObject'
---

# TMP Style Localizer

The Localizer Style component used in TextMeshPro, TextMeshProUGUI, TMP\_Dropdown component.

## Component

![](../../../.gitbook/assets/tmp_style_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| OverrideFontAsset | It changes its font asset when language is changed. Use existing font asset and material preset if it's not set. It displays a Font Asset and Material Preset field in each language if it's enabled. \(Refer : If Material Preset is empty, It uses main material preset in font asset.\) |
| OverrideSpacingOptions | It changes its spacing options when language is changed. It displays a spacing options field in each language if it's enabled. |
| LStyleData | Edit style of each language. It change it's component font and line spacing when language is changed. |

## Reference

{% code title="TMPStyleLocalizer.cs" %}
```csharp
public class TMPStyleLocalizer : LocalizerObject {
    public struct SpacingOption { }
    public class StyleData { }

    public LTMPStyleData LStyleData { get; set; }
    public bool OverrideFontAsset { get; set; }
    public bool OverrideSpacingOptions { get; set; }

    public TMPro.TMP_FontAsset FontAsset { get; }
    public UnityEngine.Material FontSharedMaterial { get; }
    public SpacingOption SpacingOptions { get; }

    public override bool SetComponent () { }
}
```
{% endcode %}

| Inner Struct |  |
| :--- | :--- |
| [SpacingOption](spacing-option.md) | Getting spacing option values of Text Mesh Pro Text. |

| Inner Class |  |
| :--- | :--- |
| [StyleData](style-data.md) | Getting information of font asset, material preset and spacing options. |

| Value Definition |  |
| :--- | :--- |
| LTMPStyleData | [LValue&lt;T&gt;](../../../lvalue/lvalue-type.md) Wrapper class of [TMPStyleLocalizer.StyleData](style-data.md) type. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Properties</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">LStyleData</td>
      <td style="text-align:left">Get or set each language <a href="style-data.md">StyleData</a> of the component.</td>
    </tr>
    <tr>
      <td style="text-align:left">OverrideFontAsset</td>
      <td style="text-align:left">It changes its font asset when language is changed. Use existing font
        asset and material preset if it&apos;s not set. (Refer : If Material Preset
        is empty, It uses main material preset in font asset.)</td>
    </tr>
    <tr>
      <td style="text-align:left">OverrideSpacingOptions</td>
      <td style="text-align:left">It changes its spacing options when language is changed.</td>
    </tr>
    <tr>
      <td style="text-align:left">FontAsset</td>
      <td style="text-align:left">Get font value of component.</td>
    </tr>
    <tr>
      <td style="text-align:left">FontSharedMaterial</td>
      <td style="text-align:left">Get fontSharedMaterial value of component.</td>
    </tr>
    <tr>
      <td style="text-align:left">SpacingOptions</td>
      <td style="text-align:left">
        <p>Get <a href="spacing-option.md">SpacingOption</a> struct from each spacing
          option values of component.</p>
        <p>It&apos;s not applied to TMP_Dropdown.</p>
      </td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Inherited Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SetComponent</td>
      <td style="text-align:left">
        <p>Fine and set related Text Mesh Pro component.</p>
        <p>If it success, it&apos;s true and false it&apos;s not.</p>
      </td>
    </tr>
  </tbody>
</table>

