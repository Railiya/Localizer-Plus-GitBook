---
description: Loaded script class
---

# Script

The class that loaded from scrt or cscrt by **Script Reader**.

**Script** is mean background **Directory**. You can get background **Directory** via Root and get top **Directories** via SubDirectories.

## Reference

{% code title="ScriptReader.cs" %}
```csharp
public class Script {
    public Directory this[string path] { get; }

    public Directory Root { get; }
    public int DirectoryCount { get; }
    public Directory[] SubDirectories { get; }
    
    public Directory GetSubDirectory (string name) { }
    public bool HasSubDirectory (string name) { }
    public void Clear () { }
}
```
{% endcode %}

| Indexer |  |
| :--- | :--- |
| this | Get [Directory](directory.md) by path. |

| Properties |  |
| :--- | :--- |
| Root | Get background [Directory](directory.md). |
| DirectoryCount | Get number of top [Directories](directory.md). |
| SubDirectories | Get top [Directories](directory.md). |

| Functions |  |
| :--- | :--- |
| GetSubDirectory | Get sub [Directory](directory.md) from name. |
| HasSubDirectory | Get existence of [Directory](directory.md) from name. |
| Clear | Clear Script. |

## Get content from Script

The indexer of **Script** is return **Directory** from path. You can get content by returned **Directory** or access to Root.

The example is to get content from path "First/Second/script001".

```csharp
private Script script;

private void Start () {
    string fromIndexer = script["First/Second"]["script001"];
    string fromRoot = script.Root["First/Second/script001"];
}
```

{% hint style="info" %}
More **Directory** in path, it spends a little more time to get content. Recommend getting content from cached **Directory** using frequently.
{% endhint %}

