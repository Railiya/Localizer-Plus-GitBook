---
description: 'base class : LocalizerObject'
---

# Texture Localizer

The Localizer component used in MeshRenderer component.

## Component

![](../../.gitbook/assets/texture_localizer_inspector.png)

| Properties |  |
| :--- | :--- |
| UseSharedMaterial | Change mainTexture in sharedMaterial. This work affect to every renderers sharing the materials. Default is true. If it's disabled, It will change the texture of instance materials. **This work doesn't occur in editor state, and it's not recommended.** |
| LTexture | Edit texture of each language. It changes its component texture when language is changed. |

## Reference

{% code title="TextureLocalizer.cs" %}
```csharp
public class TextureLocalizer : LocalizerObject {    
    public UnityEngine.MeshRenderer Component { get; }

    public LTexture LTexture { get; set; }
    public UnityEngine.Texture Texture { get; }
    public bool UseSharedMaterial { get; set; }

    public override bool SetComponent () { }
}
```
{% endcode %}

| Value Definition |  |
| :--- | :--- |
| LTexture | [LValue&lt;T&gt;](../../lvalue/lvalue-type.md) Wrapper class of Texture type. |

| Properties |  |
| :--- | :--- |
| Component | Get MeshRenderer component. |
| LTexture | Get or set texture each language of the component. |
| Texture | Get mainTexture value in material  of component. |
| UseSharedMaterial | Change mainTexture in sharedMaterial. If it's disabled, It will change the texture of instance materials. Default is true. |

| Inherited Functions |  |
| :--- | :--- |
| SetComponent | Fine and set MeshRenderer component. If it success, it's true and false it's not. |

