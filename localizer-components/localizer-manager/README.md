---
description: 에셋의 핵심
---

# LocalizerManager

언어 설정 및 **Localizer Object** 를 관리하는 static class입니다.

**Localizer Object**의 언어를 변경하기 위해서는 **Localizer Manager**의 **SetLanguage** 를 호출합니다. 현재 언어의 정보를 가져오려면 **SelectedLanguage** 혹은 **SelectedLanguageIndex**를 통해 가져올 수 있습니다. 언어가 변경되었을 때 호출되는 이벤트가 필요하다면 **OnLanguageChagned**를 사용합니다.

| Static Properties { get } |  |
| :--- | :--- |
| Languages : [LanguageInfo](languageinfo.md)\[\] | 프로젝트의 언어 목록을 가져옵니다. |
| SelectedLanguage : [LanguageInfo](languageinfo.md) | 현재 적용된 언어의 [LanguageInfo](languageinfo.md)를 가져옵니다. |
| SelectedLanguageIndex : int | 현재 적용된 언어의 인덱스를 가져옵니다. |

| Static Events |  |
| :--- | :--- |
| OnLanguageChanged&lt;[LanguageInfo](languageinfo.md)&gt; | SetLanguage가 호출될 경우 실행되는 이벤트입니다. |

<table>
  <thead>
    <tr>
      <th style="text-align:left">Static Functions</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">SetLanguage (string)</td>
      <td style="text-align:left">LanguageText &#xC5B8;&#xC5B4;&#xB97C; &#xBCC0;&#xACBD;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">SetLanguage (SystemLanguage)</td>
      <td style="text-align:left">SystemLanguage &#xC5B8;&#xC5B4;&#xB97C; &#xBCC0;&#xACBD;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">SetLanguageToDefault ()</td>
      <td style="text-align:left">&#xAE30;&#xBCF8; (&#xCCAB; &#xBC88;&#xC9F8;) &#xC5B8;&#xC5B4;&#xB85C;
        &#xBCC0;&#xACBD;&#xD569;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">RemoveNullObjects ()</td>
      <td style="text-align:left">
        <p>Object &#xB9AC;&#xC2A4;&#xC5D0;&#xC11C; null&#xC778; <a href="../localizer-object/">LocalizerObject</a>&#xB97C;
          &#xC81C;&#xAC70;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <p>(&#xCC38;&#xACE0;: OnDestroy&#xC5D0;&#xC11C; &#xAE30;&#xBCF8;&#xC801;&#xC73C;&#xB85C;
          &#xC81C;&#xAC70;&#xB429;&#xB2C8;&#xB2E4;.)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">GetLocalizersOfType&lt;T&gt; ()</td>
      <td style="text-align:left">&#xD574;&#xB2F9; <a href="../localizer-object/">LocalizerObject </a>&#xD0C0;&#xC785;&#xC758;
        Object&#xB4E4;&#xC744; &#xB9AC;&#xC2A4;&#xD2B8;&#xC5D0;&#xC11C; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">IndexOfLanguage (<a href="languageinfo.md">LanguageInfo</a>)</td>
      <td style="text-align:left"><a href="languageinfo.md">LanguageInfo</a>&#xB97C; &#xD1B5;&#xD574; &#xC5B8;&#xC5B4;&#xC758;
        &#xC778;&#xB371;&#xC2A4;&#xB97C; &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">IndexOfLanguage (string)</td>
      <td style="text-align:left">LanguageText&#xB97C; &#xD1B5;&#xD574; &#xC5B8;&#xC5B4;&#xC758; &#xC778;&#xB371;&#xC2A4;&#xB97C;
        &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">IndexOfLanguage (SystemLanguage)</td>
      <td style="text-align:left">SystemLanguage&#xB97C; &#xD1B5;&#xD574; &#xC5B8;&#xC5B4;&#xC758; &#xC778;&#xB371;&#xC2A4;&#xB97C;
        &#xAC00;&#xC838;&#xC635;&#xB2C8;&#xB2E4;.</td>
    </tr>
  </tbody>
</table>



