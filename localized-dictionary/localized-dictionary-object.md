---
description: LString 모음집 모음집의 효율적인 사용 수단
---

# Localized Dictionary Object

**Localized Dictionary**를 에디터상에서 편집하여 사용할 수 있는 스크립터블 오브젝트입니다. 테이블 형식으로 편집할 수 있으며 csv, tsv, 구글 스프레드 시트로부터 파싱하여 사용할 수 있습니다.

**Localized Dictionary**는 프로젝트 _우 클릭 - Create - Localizer Plus - Localized Dictionary_를 통해 생성하거나 **Script Writer Window**에서 추출할 수 있습니다.

## 스크립터블 오브젝트

![Cube Collector 예제의 예시](../.gitbook/assets/localized\_dictionary\_inspector.PNG)

| Editor Only               |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| Language Selector         | 미리보기의 언어 설정입니다.                                                           |
| Open in Script Writer     | [Script Writer Window](../editor-window/script-writer-window.md)에서 편집합니다. |
| Created From              | 생성 출처입니다.                                                                 |
| Last Updated              | 마지막 업데이트 날짜 입니다.                                                          |
| Keys For Primary Language | 기본 언어의 내용을 key 값으로 사용합니다.                                                 |
| Allow Multiple Line       | 에디터 텍스트 편집의 멀티 라인을 허용합니다.                                                 |
| Link Spread Sheets        | 구글 스프레드 시트로부터 내용을 생성합니다.                                                  |

| Key Content Pair Edit |                                                                                              |
| --------------------- | -------------------------------------------------------------------------------------------- |
| Edit                  | 지정된 [KeyContentPair](localized-dictionary/key-content-pair.md) 에디터를 엽니다.                     |
| Delete                | 지정된 [KeyContentPair](localized-dictionary/key-content-pair.md)를 제거합니다.                       |
| Create New Pair       | 새 [KeyContentPair](localized-dictionary/key-content-pair.md)를 추가합니다.                         |
| Import As New Pair    | csv, tsv, 구글 스프레드 시트로부터 새 [KeyContentPair](localized-dictionary/key-content-pair.md)를 추가합니다. |

## Key Content Pair 에디터

![cubeCollect Key Content Pair 에디터](../.gitbook/assets/key\_content\_pair\_editor.PNG)

| Toolbar     |                                                                    |
| ----------- | ------------------------------------------------------------------ |
| Edit        | 편집 메뉴를 엽니다.                                                        |
| Apply       | 수정 사항을 적용합니다.                                                      |
| Revert      | 마지막 수정 사항으로 되돌립니다.                                                 |
| Cell Width  | 셀의 너비를 설정합니다.                                                      |
| Cell Height | 셀의 높이를 설정합니다. AllowMultipleLine 이 true 일 경우에만 가능합니다.               |
| Pair Name   | [KeyContentPair](localized-dictionary/key-content-pair.md)의 이름입니다. |

| Edit Menu               |                                     |
| ----------------------- | ----------------------------------- |
| Add Key                 | 새 항목을 추가합니다.                        |
| Delete Empty Keys       | Key 내용이 비어있는 항목들을 모두 제거합니다.         |
| Sort Keys by  Ascending | Key 값을 기준으로 오름차순 정렬합니다.             |
| Sort Keys by Descending | Key 값을 기준으로 내림차순 정렬합니다.             |
| Import                  | csv, tsv, 구글 스프레드 시트로부터 항목들을 추가합니다. |
| Export                  | 현재 항목들을 csv 또는 tsv 파일로 추출합니다.       |

{% hint style="info" %}
Keys For Primary Language가 활성화되면 첫 번째 언어의 영역이 비활성화 되고 해당 텍스트는 key 값으로 고정됩니다.
{% endhint %}

{% hint style="info" %}
Allow Multiple Line 에 따라 에디터의 텍스트 영역의 종류가 달라집니다. false일 경우 텍스트 필드이며 탭을 통해 다음 컨트롤로 포커싱을 옮길 수 있습니다. true일 경우 텍스트 영역이며 \t 와 \n의 입력이 가능해집니다.
{% endhint %}

## Key Content Pair Importer

![](../.gitbook/assets/key\_content\_pair\_importer.PNG)

| Properties        |                                      |
| ----------------- | ------------------------------------ |
| Ignore First Line | 첫 번째 줄을 무시합니다. (언어 항목을 무시할 때 사용합니다.) |
| File Type         | csv 혹은 tsv 파일 형식을 지정합니다.             |
| Import Method     | 텍스트, 파일 또는 구글 스프레드 시트 임포트 방식입니다.     |

{% hint style="info" %}
구글 스프레드 시트 임포트 방식에서 url를 입력하고 "Convert" 버튼을 사용하면 추출 형식의 url로 변환됩니다. url을 입력할 때 시트의 id (gid) 까지 주소를 전체 복사 후 입력한 뒤 "Convert" 버튼을 누르고 Import를 하면 편리하게 사용할 수 있습니다.
{% endhint %}

## Key Content Pair Exporter

![](<../.gitbook/assets/localized\_dictionary\_object\_exporter (1).PNG>)

| Properties               |                                |
| ------------------------ | ------------------------------ |
| File Type                | csv 또는 tsv 파일 형식을 지정합니다.       |
| Include Language Columns | 첫번 째 줄에 언어 컬럼을 추가합니다.          |
| Include Return Character | 새 줄 (\n)에 캐리지 리턴 (\r) 을 포함합니다. |
| Enable Content Escape    | Escape된 내용으로 저장합니다.            |

## 구글 스프레드 시트 연결

Link Spread Sheets 를 활성화 하면 스프레드 시트의 URL과 여러 시트들의 Pair 이름과 gid를 입력할 수 있는 리스트가 표시됩니다. 원하는 시트들을 gid를 통해 각 내용들을 Key Content Pair로 가져옵니다.&#x20;

![패키지에 포함되지 않은 예시](../.gitbook/assets/localized\_dictionary\_link\_spreadsheets.PNG)

| Properties        |                               |
| ----------------- | ----------------------------- |
| Ignore First Line | 컨텐츠를 가져올 때 첫번째 열을 무시합니다.      |
| Sheets URL        | 대표되는 스프레드 시트의 Export URL 입니다. |

| GID Item  |                                                                              |
| --------- | ---------------------------------------------------------------------------- |
| Pair Name | 시트를 가져올 때의 [KeyContentPair](localized-dictionary/key-content-pair.md) 이름입니다. |
| GID       | 시트의 GID 입니다.                                                                 |

| Property Edit         |                                    |
| --------------------- | ---------------------------------- |
| Convert to Export URL | 일반 형식의 스프레드 시트 URL을 추출 형식으로 변환합니다. |
| Add Sheet             | GID Item을 추가합니다.                   |
| Remove Last           | 마지막 GID Item을 제거합니다.               |
| Refresh               | 설정된 항목들을 기준으로 컨텐츠를 업데이트 합니다.       |

{% hint style="info" %}
GID는 시트마다 다르며 링크의 가장 마지막 부분에 "gid={number}" 형식으로 표시되어 있습니다. 이 중 숫자 부분만 GID 값에 입력하면 됩니다.
{% endhint %}

## 레퍼런스

{% code title="LocalizedDictionaryObject.cs" %}
```csharp
public class LocalizedDictionaryObject : ScriptableObject {
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
    public void RefreshLanguages () { }
}
```
{% endcode %}

| Indexer |                                                                                 |
| ------- | ------------------------------------------------------------------------------- |
| this    | 인덱스 또는 키를 통해 [KeyContentPair](localized-dictionary/key-content-pair.md)를 가져옵니다. |

| Properties |                                                                            |
| ---------- | -------------------------------------------------------------------------- |
| Count      | 보유중인 [KeyContentPair](localized-dictionary/key-content-pair.md)의 수를 가져옵니다. |

| Functions            |                                                                                            |
| -------------------- | ------------------------------------------------------------------------------------------ |
| AddKeyContentPair    | [KeyContentPair](localized-dictionary/key-content-pair.md)를 추가합니다. 이미 있다면 false를 반환합니다.    |
| IndexOfPair          | [KeyContentPair](localized-dictionary/key-content-pair.md)의 인덱스를 가져옵니다.                    |
| RemovePairAt         | 해당 인덱스의 [KeyContentPair](localized-dictionary/key-content-pair.md)를 제거합니다.                 |
| RemoveKeyContentPair | [KeyContentPair](localized-dictionary/key-content-pair.md)를 제거합니다.                         |
| InsertPairAt         | 해당 인덱스에 [KeyContentPair](localized-dictionary/key-content-pair.md)를 추가합니다.                 |
| ContainsPair         | 해당 키의 [KeyContentPair](localized-dictionary/key-content-pair.md)의 존재 여부입니다.                |
| GetKeyContentPair    | 해당 키의 [KeyContentPair](localized-dictionary/key-content-pair.md)를 가져옵니다.                   |
| TryGetKeyContentPair | 해당 키의 [KeyContentPair](localized-dictionary/key-content-pair.md)를 가져옵니다. 없다면 false를 반환합니다. |
| RefreshLanguages     | 보유중인 [KeyContentPair](localized-dictionary/key-content-pair.md)들의 언어 설정을 갱신합니다.            |
