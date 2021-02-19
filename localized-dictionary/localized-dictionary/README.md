---
description: LString collection collection
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

| Indexer |  |
| :--- | :--- |
| this | 인덱스 또는 키를 통해 [KeyContentPair](key-content-pair.md)를 가져옵니다. |

| Properties |  |
| :--- | :--- |
| Count | 보유중인 [KeyContentPair](key-content-pair.md)의 수를 가져옵니다. |

| Functions |  |
| :--- | :--- |
| AddKeyContentPair | [KeyContentPair](key-content-pair.md)를 추가합니다. 이미 있다면 false를 반환합니다. |
| IndexOfPair | [KeyContentPair](key-content-pair.md)의 인덱스를 가져옵니다. |
| RemovePairAt | 해당 인덱스의 [KeyContentPair](key-content-pair.md)를 제거합니다. |
| RemoveKeyContentPair | [KeyContentPair](key-content-pair.md)를 제거합니다. |
| InsertPairAt | 해당 인덱스에 [KeyContentPair](key-content-pair.md)를 추가합니다. |
| ContainsPair | 해당 키의 [KeyContentPair](key-content-pair.md)의 존재 여부입니다. |
| GetKeyContentPair | 해당 키의 [KeyContentPair](key-content-pair.md)를 가져옵니다. |
| TryGetKeyContentPair | 해당 키의 [KeyContentPair](key-content-pair.md)를 가져옵니다. 없다면 false를 반환합니다. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Static Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">GetKeyContentPairFromCSV</td>
      <td style="text-align:left">
        <p>csv &#xB0B4;&#xC6A9;&#xC73C;&#xB85C;&#xBD80;&#xD130; <a href="key-content-pair.md">KeyContentPair</a>&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
        <p>ignoreFirstLine&#xAC00; true&#xB77C;&#xBA74; &#xCCAB; &#xBC88;&#xC9F8;
          &#xC904;&#xC744; &#xBB34;&#xC2DC;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetKeyContentPairFromTSV</td>
      <td style="text-align:left">
        <p>tsv &#xB0B4;&#xC6A9;&#xC73C;&#xB85C;&#xBD80;&#xD130; <a href="key-content-pair.md">KeyContentPair</a>&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
        <p>ignoreFirstLine&#xAC00; true&#xB77C;&#xBA74; &#xCCAB; &#xBC88;&#xC9F8;
          &#xC904;&#xC744; &#xBB34;&#xC2DC;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LoadKeyContentPairFromSpreadSheets</td>
      <td style="text-align:left">
        <p>&#xAD6C;&#xAE00; &#xC2A4;&#xD504;&#xB808;&#xB4DC; &#xC2DC;&#xD2B8;&#xB85C;&#xBD80;&#xD130;
          <a
          href="key-content-pair.md">KeyContentPair</a>&#xB97C; &#xBE44;&#xB3D9;&#xAE30; &#xB85C;&#xB4DC;&#xD569;&#xB2C8;&#xB2E4;.
            &#xB85C;&#xB4DC;&#xAC00; &#xB05D;&#xB098;&#xBA74; onLoadComplete&#xB97C;
            &#xD638;&#xCD9C;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>ignoreFirstLine&#xAC00; true&#xB77C;&#xBA74; &#xCCAB; &#xBC88;&#xC9F8;
          &#xC904;&#xC744; &#xBB34;&#xC2DC;&#xD569;&#xB2C8;&#xB2E4;. convertToExportURL&#xC774;
          true&#xB77C;&#xBA74; url&#xC744; tsv &#xCD94;&#xCD9C; &#xD615;&#xC2DD;&#xC73C;&#xB85C;
          &#xBCC0;&#xD658;&#xD558;&#xC5EC; &#xC0AC;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetSpreadSheetsExportURL</td>
      <td style="text-align:left">url&#xC744; &#xCD94;&#xCD9C; &#xD615;&#xC2DD;&#xC73C;&#xB85C; &#xBCC0;&#xD658;&#xD569;&#xB2C8;&#xB2E4;.
        format&#xC740; &#xD30C;&#xC77C; &#xD615;&#xC2DD;&#xC785;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>

