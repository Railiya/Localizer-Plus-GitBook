# Directory

실제 컨텐츠와 하위 **Directory**를 가지는 폴더 클래스입니다. 인덱서 및 GetContent 함수를 통해 컨텐츠를 가져올 수 있습니다.

**Script**가 로드될 때 indexing이 true라면 인덱스를 통해 컨텐츠를 가져올 수 있습니다.

## 레퍼런스

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

| Indexer |                        |
| ------- | ---------------------- |
| this    | 경로와 인덱스로부터 컨텐츠를 가져옵니다. |

| Properties     |                       |
| -------------- | --------------------- |
| Parent         | 상위 Directory를 가져옵니다.  |
| Name           | Directory의 경로 이름입니다.  |
| Path           | Directory의 전체 경로 입니다. |
| ScriptCount    | 보유중인 컨텐츠의 수 입니다.      |
| DirectoryCount | 하위 Directory의 수 입니다.  |
| SubDirectories | 하위 Directory들을 가져옵니다. |
| ScriptKeys     | 보유중인 컨텐츠의 id들을 가져옵니다. |
| ScriptValues   | 보유중인 컨텐츠들을 가져옵니다.     |

| Functions       |                                |
| --------------- | ------------------------------ |
| GetContent      | 해당 id의 컨텐츠를 가져옵니다.             |
| GetSubDirectory | 해당 이름의 Directory를 가져옵니다.       |
| Contains        | 해당 id의 컨텐츠의 존재 여부를 가져옵니다.      |
| HasIndex        | 해당 인덱스의 컨텐츠 존재 여부를 가져옵니다.      |
| HasSubDirectory | 해당 이름의 Directory 존재 여부를 가져옵니다. |

## Directory로 부터 컨텐츠 가져오기

**Directory**의 인덱서는 컨텐츠를 반환합니다. string 인덱서는 상대 경로로부터 컨텐츠를 가져오며 int 인덱서는 현재 **Directory**에서 인덱스에 해당되는 컨텐츠를 가져옵니다.

예시는 "First/Second/script001" 경로의 컨텐츠를 가져오는 예시입니다.

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
GetContent는 인덱서와 달리 현재 **Directory**의 컨텐츠를 가져오는 함수입니다. 인덱서로 하위 컨텐츠를 가져올 때는 추가적인 경로 조사가 필요하며 GetContent는 그런 작업 없이 바로 가져올 수 있습니다. 다만, 성능적으로 크게 차이는 없으니 편한 방법으로 사용해도 됩니다.
{% endhint %}
