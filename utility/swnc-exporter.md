---
description: Best way to use swnc files
---

# Swnc Exporter

**Script Writer** 에서는 해당 언어의 파일 하나만 추출하거나 **Localized Dictionary**를 추출할 수 있습니다. 언어마다 일일히 추출하는 것은 번거로운 작업이며 추출해야할 swnc 파일이 여러 개 일 경우 시간이 다소 소요될 수 있습니다.

**Swnc Exporter** 는 지정된 다수의 swnc 파일로부터 추출 세팅에 맞는 방식으로 특정 폴더에 한 번에 추출시키는 스크립터블 오브젝트 입니다. 추출 형식은 **Script, Compressed Script, Localized Dictionary**를 지원하며 **Script** 및 **Compressed Script**는 폴더가 생성되고 하위에 언어별 파일이 생성됩니다.

![Capsule Story &#xC608;&#xC81C;&#xC758; swnc &#xD30C;&#xC77C;](../.gitbook/assets/swnc_exporter_inspector.png)

## 파일 정보

swnc 파일과 추출될 때의 이름을 지정할 수 있습니다. 하단의 Add 버튼을 눌러 항목을 추가할 수 있으며 Label을 우 클릭하여 해당 요소를 Script Writer로 열거나 제거할 수 있습니다.

| File Info |  |
| :--- | :--- |
| Reference | 추출 대상 에셋입니다. swnc 확장자의 파일만 등록됩니다. |
| Export Name | 추출될 때의 폴더 혹은 파일의 이름입니다. |
| Last Update | swnc 파일의 최종 수정일 입니다. |

## 추출 세팅

추출에 필요한 세팅입니다. 추출 대상 폴더, 추출 형식 및 확장자, 이름 형식을 지정합니다. 확장자는 추출 형식에 따라 변경됩니다.

| Export Settings |  |
| :--- | :--- |
| Export Path | 추출 대상 폴더 입니다. |
| Export Type | 추출되는 파일의 형식입니다. |
| Extension | 추출되는 파일의 확장자 입니다. |
| Name Type | 추출되는 파일의 이름 형식입니다. |
| Last Export | 최종 추출 날짜 입니다. |
| Export | 추출을 실행합니다. |

{% hint style="info" %}
.scrt 및 .cscrt 확장자는 파일을 클릭하여 인스펙터에서 스크립트 내용을 볼 수 있습니다. 이는 File 정적 클래스로부터 로드하거나 StreamReader를 사용할 때 쓰이는 확장자 입니다. Resources 폴더를 사용할 경우 .txt 나 .bytes 확장자를 사용해야 합니다.

이름 형식은 LanguageText 및 SystemLanguage가 있습니다. LanguageText는 개발자가 지정한 언어의 이름이며 SystemLanguage는 유니티에서 지원하는언어 형식입니다. SystemLanguage의 이름 형식을 사용한다면 영어 명칭의 언어명으로 사용됩니다.
{% endhint %}



