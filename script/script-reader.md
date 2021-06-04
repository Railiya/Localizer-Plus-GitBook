---
description: Script file load class
---

# Script Reader

The way of load only specific language text to memory to use. The scripts used in the game will be saved in the project as a file. It can use memory more flexible rather than **Localizer Object** or **Localized Dictionary**. Recommended using this way if your game has many texts.

The script supports **Script Writer Node Collection** \(.swnc\) that edit texts of each language, **Script** \(.scrt\) that saved data of specific language as common text file, **Compressed Script** \(.cscrt\) that saved data of specific language as compressed binary file. You can edit swnc file in Script Writer Winodw.

**Script Reader** has function load scrt file and cscrt file which exported from swnc file and return converted **Script** class from file.

## Reference

{% code title="ScriptReader.cs" %}
```csharp
public static class ScriptReader {
    public static Script Load (string scriptFile, bool indexing = false) { }
    public static Script LoadCompressed (byte[] scriptFile, bool indexing = false, Func<string, string> decrypt = null) { }
}
```
{% endcode %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">Static Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Load</td>
      <td style="text-align:left">
        <p>Get loaded <a href="script/">Script</a> from content of scrt file.</p>
        <p>It can be get content by index if indexing is true.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LoadCompressed</td>
      <td style="text-align:left">
        <p>Get loaded <a href="script/">Script</a> from bytes of cscrt file.</p>
        <p>It can be get content by index if indexing is true.</p>
        <p>Use decrypt Function if content need to be decryption</p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The scriptFile used in load is not file path but file content.

You can use File.ReadAllText, File.ReadAllBytes or StreamReader if file is loaded from file path directly.

If you want to use Resources folder, you have to load the file as TextAsset and get text or bytes from it. To get TextAsset normally, the extension of assets are must be txt or bytes.
{% endhint %}

