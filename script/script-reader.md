---
description: Script file load class
---

# Script Reader

스크립트는 게임에 사용되는 텍스트를 언어별로 파일을 나누어 필요한 언어에 대한 텍스트만 메모리에 로드하여 사용하는 방식입니다. **Localizer Component** 나 **Localized Dictionary** 보다 메모리 관리 측면에서 더 유용하게 사용할 수 있습니다. 게임의 텍스트 량이 많은 경우라면 이 방식을 추천드립니다.

스크립트에는 언어별로 텍스트를 편집할 수 있는 **Script Writer Node Collection** \(.swnc\)와 특정 언어의 데이터를 일반적인 텍스트로 저장하는 **Script** \(.scrt\) 및 특정 언어의 데이터를 압축하여 바이트 배열로 저장하는 **Compressed Script** \(.cscrt\)를 지원합니다. swnc 파일은 **Script Writer Window** 에서 편집할 수 있습니다.

**Script Reader**는 swnc 파일로부터 추출된 scrt 파일과 cscrt 파일을 읽어들여 **Script** 클래스로 반환하는 기능을 가지고 있습니다.

## 레퍼런스

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
        <p>scrt &#xD30C;&#xC77C;&#xC758; &#xB0B4;&#xC6A9;&#xC73C;&#xB85C;&#xBD80;&#xD130;
          <a
          href="script/">Script</a>&#xB97C; &#xB85C;&#xB4DC;&#xD558;&#xC5EC; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
        <p>indexing&#xC774; true&#xB77C;&#xBA74; &#xC778;&#xB371;&#xC2A4;&#xB97C;
          &#xD1B5;&#xD574; &#xCEE8;&#xD150;&#xCE20;&#xB97C; &#xAC00;&#xC838;&#xC62C;
          &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LoadCompressed</td>
      <td style="text-align:left">
        <p>cscrt &#xD30C;&#xC77C;&#xC758; &#xBC14;&#xC774;&#xD2B8;&#xB85C;&#xBD80;&#xD130;
          <a
          href="script/">Script</a>&#xB97C; &#xB85C;&#xB4DC;&#xD558;&#xC5EC; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</p>
        <p>indexing&#xC774; true&#xB77C;&#xBA74; &#xC778;&#xB371;&#xC2A4;&#xB97C;
          &#xD1B5;&#xD574; &#xCEE8;&#xD150;&#xCE20;&#xB97C; &#xAC00;&#xC838;&#xC62C;
          &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <p>&#xBCF5;&#xD638;&#xD654;&#xAC00; &#xD544;&#xC694;&#xD55C; &#xB0B4;&#xC6A9;&#xC77C;
          &#xACBD;&#xC6B0; decrtypt Function&#xC744; &#xC0AC;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
로드에 사용되는 scriptFile은 경로가 아닌 파일의 내용입니다. 

파일의 경로로부터 직접 로드할 수 있는 경우라면 File.ReadAllText, File.ReadAllBytes를 사용하거나 StreamReader 등을 사용할 수 있습니다. 

Resources 폴더를 사용하는 경우라면 TextAsset으로 받은 뒤 text 나 bytes로 파일 내용을 가져올 수 있습니다. TextAsset을 사용하는 경우라면 파일의 확장자가 txt 또는 bytes로 되어야 정상적으로 에셋을 가져올 수 있습니다.
{% endhint %}



