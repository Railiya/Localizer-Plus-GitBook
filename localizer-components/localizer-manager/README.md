---
description: 에셋의 핵심
---

# LocalizerManager

언어 설정 및 **Localizer Object** 를 관리하는 static class입니다.

**Localizer Object**의 언어를 변경하기 위해서는 **Localizer Manager**의 **SetLanguage** 를 호출합니다. 현재 언어의 정보를 가져오려면 **SelectedLanguage** 혹은 **SelectedLanguageIndex**를 통해 가져올 수 있습니다. 언어가 변경되었을 때 호출되는 이벤트가 필요하다면 **OnLanguageChagned** 델리게이트를 사용합니다.

| Static Properties |  |
| :--- | :--- |
| SelectedLanguage : LanguageInfo | 현재 적용된 언어의 LanguageInfo를 가져옵니다. |
| SelectedLanguageIndex : int | 현재 적용된 언어의 인덱스를 가져옵니다. |

| Static Delegates |  |
| :--- | :--- |
| OnLanguageChanged&lt;LanguageInfo&gt; | SetLanguage가 호출될 경우 실행되는 이벤트입니다. |



