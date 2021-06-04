---
description: LString collection collection
---

# Localized Dictionary

The class has **Key Content Pair** list. You can get Key Content Pair by key or index, and get **LString** by key or index from **Key Content Pair**.

{% hint style="info" %}
Recommended to use **Localized Dictionary Object** edited in editor or use csv, tsv, google spread sheets parsing static functions instead of add contents in script.
{% endhint %}

## Reference

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
| this | Get [KeyContentPair](key-content-pair.md) by index or key. |

| Properties |  |
| :--- | :--- |
| Count | Get number of [KeyContentPair](key-content-pair.md) has. |

| Functions |  |
| :--- | :--- |
| AddKeyContentPair | Add [KeyContentPair](key-content-pair.md). Return false if it's exist. |
| IndexOfPair | Get index of [KeyContentPair](key-content-pair.md). |
| RemovePairAt | Remove [KeyContentPair](key-content-pair.md) at index. |
| RemoveKeyContentPair | Remove [KeyContentPair](key-content-pair.md). |
| InsertPairAt | Add [KeyContentPair](key-content-pair.md) to index. |
| ContainsPair | Get existence of [KeyContentPair](key-content-pair.md). |
| GetKeyContentPair | Get [KeyContentPair](key-content-pair.md) by key. |
| TryGetKeyContentPair | Get [KeyContentPair](key-content-pair.md) by key. Return false if it's exist. |

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
        <p>Get <a href="key-content-pair.md">KeyContentPair</a> from converted csv
          content.</p>
        <p>Skip first lineconversion if it&apos;s ignoreFirstLine is true.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetKeyContentPairFromTSV</td>
      <td style="text-align:left">
        <p>Get <a href="key-content-pair.md">KeyContentPair</a> from converted tsv
          content.</p>
        <p>Skip first lineconversion if it&apos;s ignoreFirstLine is true.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LoadKeyContentPairFromSpreadSheets</td>
      <td style="text-align:left">
        <p>Load <a href="key-content-pair.md">KeyContentPair</a> asynchronously from
          google spread sheets. Call onLoadComplete when load is ended.</p>
        <p>Skip first lineconversion if it&apos;s ignoreFirstLine is true.</p>
        <p>It uses tsv export format url, if convertToExportURL is true.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetSpreadSheetsExportURL</td>
      <td style="text-align:left">Convert url to export format. format parameter is file extension.</td>
    </tr>
  </tbody>
</table>

