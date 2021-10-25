---
description: LString 모음집 모음집
---

# Localized Dictionary

**Key Content Pair** 리스트를 가지는 클래스입니다. 키 혹은 인덱스를 통해 **Key Content Pair**를 가져올 수 있으며 가져온 **Key Content Pair** 에서 키 혹은 인덱스를 통해 **LString**을 가져옵니다.

{% hint style="info" %}
스크립트 상에서 내용을 추가하는 방식 보다는 **Localized Dictionary Object**를 이용해 에디터에서 편집 하거나 CSV, TSV, 구글 스프레드 시트 등 파싱 정적 함수를 이용하는 것을 추천합니다.
{% endhint %}

## 레퍼런스

{% code title="LocalizedDictionary.cs" %}
```csharp
public class LocalizedDictionary {
    public KeyContentPair this[int index] { get; }
    public KeyContentPair this[string key] { get; }
    
    public int Count { get; }
    
    public bool AddKeyContentPair (KeyContentPair pair) { }
    public int IndexOfPair (KeyContentPair pair) { }
    public void RemovePairAt (int index) { }
    public void RemoveKeyContentPair (KeyContentPair pair) { }
    public void InsertPairAt (int index, KeyContentPair pair) { }
    public bool ContainsPair (string name) { }
    public KeyContentPair GetKeyContentPair (string name) { }
    public bool TryGetKeyContentPair (string name, out KeyContentPair pair) { }
    
    public static KeyContentPair GetKeyContentPairFromCSV (string pairName, string csv, bool ignoreFirstLine) { }
    public static KeyContentPair GetKeyContentPairFromTSV (string pairName, string tsv, bool ignoreFirstLine) { }
    public static IEnumerator LoadKeyContentPairFromSpreadSheets (string pairName, string url, bool ignoreFirstLine, bool convertToExportURL, Action<KeyContentPair> onLoadComplete) { }
    public static string GetSpreadSheetsExportURL (string url, string format) { }
}
```
{% endcode %}

| Indexer |                                                            |
| ------- | ---------------------------------------------------------- |
| this    | 인덱스 또는 키를 통해 [KeyContentPair](key-content-pair.md)를 가져옵니다. |

| Properties |                                                       |
| ---------- | ----------------------------------------------------- |
| Count      | 보유중인 [KeyContentPair](key-content-pair.md)의 수를 가져옵니다. |

| Functions            |                                                                       |
| -------------------- | --------------------------------------------------------------------- |
| AddKeyContentPair    | [KeyContentPair](key-content-pair.md)를 추가합니다. 이미 있다면 false를 반환합니다.    |
| IndexOfPair          | [KeyContentPair](key-content-pair.md)의 인덱스를 가져옵니다.                    |
| RemovePairAt         | 해당 인덱스의 [KeyContentPair](key-content-pair.md)를 제거합니다.                 |
| RemoveKeyContentPair | [KeyContentPair](key-content-pair.md)를 제거합니다.                         |
| InsertPairAt         | 해당 인덱스에 [KeyContentPair](key-content-pair.md)를 추가합니다.                 |
| ContainsPair         | 해당 키의 [KeyContentPair](key-content-pair.md)의 존재 여부입니다.                |
| GetKeyContentPair    | 해당 키의 [KeyContentPair](key-content-pair.md)를 가져옵니다.                   |
| TryGetKeyContentPair | 해당 키의 [KeyContentPair](key-content-pair.md)를 가져옵니다. 없다면 false를 반환합니다. |

| Static Functions                   |                                                                                                                                                                                                                        |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GetKeyContentPairFromCSV           | <p>csv 내용으로부터 <a href="key-content-pair.md">KeyContentPair</a>로 변환하여 가져옵니다. </p><p>ignoreFirstLine가 true라면 첫 번째 줄을 무시합니다.</p>                                                                                          |
| GetKeyContentPairFromTSV           | <p>tsv 내용으로부터 <a href="key-content-pair.md">KeyContentPair</a>로 변환하여 가져옵니다. </p><p>ignoreFirstLine가 true라면 첫 번째 줄을 무시합니다.</p>                                                                                          |
| LoadKeyContentPairFromSpreadSheets | <p>구글 스프레드 시트로부터 <a href="key-content-pair.md">KeyContentPair</a>를 비동기 로드합니다. 로드가 끝나면 onLoadComplete를 호출합니다. </p><p>ignoreFirstLine가 true라면 첫 번째 줄을 무시합니다. convertToExportURL이 true라면 url을 tsv 추출 형식으로 변환하여 사용합니다.</p> |
| GetSpreadSheetsExportURL           | url을 추출 형식으로 변환합니다. format은 파일 형식입니다.                                                                                                                                                                                  |
