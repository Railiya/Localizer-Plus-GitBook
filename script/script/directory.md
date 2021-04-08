# Directory

Folder class that has actually contents and sub **Directories**. You can get content by indexer and GetContent function.

You can get content by index if indexing is true when **Script** loaded.

## Reference

{% code title="ScriptReader.cs" %}
```csharp
public class Directory {
    public string this[string path] { get; }
    public string this[int index] { get; }
    
    public Directory Parent { get; }
    public string Name { get; }
    public string Path { get; }
    public int ScriptCount { get; }
    public int DirectoryCount { get; }
    public Directory[] SubDirectories { get; }
    public string[] ScriptKeys { get; }
    public string[] ScriptValues { get; }
    
    public string GetContent (string id) { }
    public Directory GetSubDirectory (string name) { }
    public bool Contains (string id) { }
    public bool HasIndex (int index) { }
    public bool HasSubDirectory (string name) { }
}
```
{% endcode %}

| Indexer |  |
| :--- | :--- |
| this | Get content from path or index. |

| Properties |  |
| :--- | :--- |
| Parent | Get parent Directory. |
| Name | The name of Directory. |
| Path | The full path of Directory. |
| ScriptCount | Get number of contents has. |
| DirectoryCount | Get number of sub Directories. |
| SubDirectories | Get sub directories. |
| ScriptKeys | Get id of contents |
| ScriptValues | Get contents. |

| Functions |  |
| :--- | :--- |
| GetContent | Get content by id. |
| GetSubDirectory | Get Directory by name. |
| Contains | Get existence of content from id. |
| HasIndex | Get existence of content from index. |
| HasSubDirectory | Get existence of Directory from name. |

## Get content from Directory

The indexer of **Directory** is return content. The string indexer return content from relative path and int indexer return content from current **Directory** by index.

The example is to get content from path "First/Second/script001".

```csharp
private Script script;

private void Start () {
    Directory first = script["First"];
    string fromIndexerString = first["Second/script001"];
    
    Directory second = first.GetSubDirectory ("Second");
    string fromSecondIndexer = second["script001"];
    string fromSecondIndex = second[0];
    string fromSecondFunction = second.GetContent ("script001");
}
```

{% hint style="info" %}
GetContent is function that get content of current **Directory** unlike indexer. Get content by indexer is needed extra work and GetContent is not. However, there is no significant difference in performance, so you can use it in a convenient way.
{% endhint %}

