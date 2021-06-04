---
description: Localizer Component를 다루기 위한 최고의 선택
---

# Localizer Manager Window

에디터에서 사용되는 주 **Localizer Project Settings** 설정, 언어 미리보기, **Style Localizer** 일괄 설정 등의 기능을 지원하는 에디터 윈도우 입니다.

![Cube Collector &#xC608;&#xC81C; &#xC52C;&#xC758; Localizer &#xBAA9;&#xB85D;](../.gitbook/assets/localizer_manager_window%20%281%29.png)

## Localizer Object 목록

**Localizer Object** 컴포넌트를 가진 게임 오브젝트 목록 입니다. **Tag Formatter**는 포함되지 않습니다. 목록에서 오브젝트를 선택하면 하이어라키에서도 오브젝트가 선택됩니다. 반대로 하이어라키에서 오브젝트를 선택하면 리스트에서도 선택됩니다. 

## Localizer 정보

리스트에서 선택된 **Localizer Object**의 정보를 표시합니다. 게임 오브젝트와 컴포넌트 형식 및 컴포넌트의 내용이 표시됩니다. **Localizer Object**가 아닌 게임 오브젝트가 하이어라키에서 선택되면 Add Localizer 버튼이 활성화 됩니다. "Add Localizer"를 클릭하면 현재 선택된 게임 오브젝트가 가진 컴포넌트에 따라 자동적으로 Localizer 컴포넌트를 추가해줍니다.

## Localizer Project Settings

프로젝트에서 실제로 사용되는 **Localizer Project Settings**를 설정합니다. 설정된 프로젝트 세팅의 언어 설정과 하단의 기본 오버라이드 옵션 등의 값들이 적용됩니다.

## Localizer 관리

| Management |  |
| :--- | :--- |
| Language | 에디터에서 사용되는 언어 설정 입니다. |
| Override Contents | Localizer 컴포넌트가 수정될 때 해당 언어의 컨텐츠가 실시간으로 적용됩니다. |
| Apply Language to Selected Localizer | 리스트에서 선택된 컴포넌트의 언어를 Language로 설정합니다. |
| Apply Language to Scene Localizers | 리스트의 모든 컴포넌트의 언어를 Language로 설정합니다. |
| Update Project Language Settings |  모든 씬의 컴포넌트의 언어 설정을 갱신합니다. |
| Add Localizer to All Scene Texts | 씬의 모든 Text, TextMesh, TMP Text에 컴포넌트를 추가합니다. |

{% hint style="info" %}
Language 설정 후 "Apply Language to Scene Localizers" 버튼을 누르면 씬의 모든 Localizer 컴포넌트들의 언어가 변경됩니다. 이는 에디터의 미리보기 작업을 위한 것이며 실제로 사용할 때는 기본 언어로 다시 돌려주어야 합니다. \(참고 : 현재 씬에만 적용됩니다.\)

언어 설정이 변경되고 스크립트가 다시 컴파일되면 Localizer 컴포넌트들의 언어 설정들도 같이 변경됩니다. 정상적으로 처리되지 않았을 경우 "Update Project Language Settings" 버튼을 클릭하여 업데이트 할 수 있습니다.
{% endhint %}

## Style Localizer 기본 오버라이드 옵션

**Style Localizer** 컴포넌트가 추가될 때 자동적으로 Override 옵션이 활성화되고 값이 설정되는 기능입니다. Override 항목들을 체크하는 것으로 활성화하고 하단의 언어별로 값을 설정하여 기본값을 설정합니다.

| Options |  |
| :--- | :--- |
| Override Font | Text Style의 폰트를 활성화 합니다. |
| Override Line Spacing | Text Style의 라인 스페이싱을 활성화 합니다. |
| Override Font Asset | TMP Style의 폰트 에셋 및 매트리얼 프리셋을 활성화 합니다. |
| Override Spacing Options | TMP Style의 스페이싱 옵션들을 활성화 합니다. |
| Override Selected Style Localizer | 리스트에서 선택된 컴포넌트의 설정을 오버라이딩 합니다. |
| Override All Style Localizers | 씬의 모든 Style 컴포넌트의 설정을 오버라이딩 합니다. |

{% hint style="info" %}
"Override All Style Localizers" 버튼을 클릭하면 씬의 모든 **Style Localizer**들의 오버라이딩 설정 및 기본값들을 에디터 윈도우의 설정에 맞춰 일괄 변경합니다. 
{% endhint %}

