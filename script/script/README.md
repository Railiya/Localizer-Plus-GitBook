---
description: 로드된 스크립트 클래스
---

# Script

**Script Reader**로 부터 scrt 혹은 cscrt 파일을 로드하여 사용하는 클래스 입니다.

**Script**는 백그라운드** Directory**를 의미합니다. Root를 통해 백그라운드 **Directory**를 가져올 수 있으며 SubDirectories를 통해 최상단 **Directory**들을 가져올 수 있습니다.

## 레퍼런스

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

| Indexer |                                         |
| ------- | --------------------------------------- |
| this    | 경로로부터 [Directory](directory.md)를 가져옵니다. |

| Properties     |                                          |
| -------------- | ---------------------------------------- |
| Root           | 백그라운드 [Directory](directory.md)를 가져옵니다.  |
| DirectoryCount | 최상단 [Directory](directory.md)의 수를 가져옵니다. |
| SubDirectories | 최상단 [Directory](directory.md)들을 가져옵니다.   |

| Functions       |                                                  |
| --------------- | ------------------------------------------------ |
| GetSubDirectory | 이름으로부터 하위 [Directory](directory.md)를 가져옵니다.      |
| HasSubDirectory | 해당하는 이름의 [Directory](directory.md) 존재 여부를 가져옵니다. |
| Clear           | Script를 초기화합니다.                                  |

## Script로 부터 컨텐츠 가져오기

**Script**의 인덱서는 경로로부터 **Directory**를 반환합니다. 반환 받은 **Directory**로 부터 컨텐츠를 가져오거나 Root로 접근하여 컨텐츠를 가져올 수 있습니다.

예시는 "First/Second/script001" 경로의 컨텐츠를 가져오는 예시입니다.

```csharp
private Script script;

private void Start () {
    string fromIndexer = script["First/Second"]["script001"];
    string fromRoot = script.Root["First/Second/script001"];
}
```

{% hint style="info" %}
경로의 **Directory**가 많을 수록 가져오는 시간이 조금씩 길어집니다. 자주 사용되는 경우에는 **Directory**를 캐싱한 후에 **Directory**로 부터 컨텐츠를 가져오는 방식을 추천합니다.
{% endhint %}
