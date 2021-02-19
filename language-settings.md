---
description: 시작하기 전에 갖추어야할 필수 덕목
---

# 언어 설정

로컬라이징을 하기 위해서는 시작 전에 어떠한 언어를 지원해 줄지를 정해야 합니다. 이 에셋어서는 언어 설정을 **LocalizerProjectSettings** 스크립터블 오브젝트에서 정의할 수 있습니다. **LocalizerProjectSettings**는 패키지가 임포트될 때 _LocalizerPlus_ 폴더에 기본적으로 포함되어있습니다.

{% hint style="info" %}
예제 게임을 플레이하기 위해서는 언어의 설정이 0번 한국어, 1번 English로 설정되어 있어야 정상적인 플레이가 가능합니다. 예제 게임을 먼저 플레이 하고 싶으시다면 플레이 이후 언어를 변경해주길 바랍니다.
{% endhint %}

## Localizer Project Settings

언어 설정 및 현재 프로젝트에서 사용되는 에디터 전용 기본 값 설정 들을 저장하고 프로젝트 전반에 걸쳐 사용됩니다. 언어 설정은 여기서 할 수 있으며 기본값 설정은 **LocalizerManager** 에디터 윈도우에서 할 수 있습니다.

에셋이 프로젝트에 없다면 **LocalizerManager** 에디터 윈도우에서 생성할 수 있습니다. 이와 별개로 여러 개의 프로젝트 세팅이 존재한다면 **LocalizerManager** 에디터 윈도우에서 실제로 사용되는 에셋을 지정하여 사용할 수도 있습니다. 주 프로젝트 세팅에서만 언어 변경을 할 수 있으며 에디터 기본 값들이 해당 에셋에서 저장되고 사용됩니다.

## 언어 변경

![](.gitbook/assets/language_settings_projectsettings.png)

실수를 방지하는 차원에서 기본적으로 언어 설정은 비활성화되어 있습니다. Enable Edit 버튼을 눌러 언어 설정을 활성화하고 Add New 혹은 Remove Last 등 언어를 추가, 제거하는 작업을 거친 뒤 "Apply Languages" 버튼을 누르면 언어를 변경할 수 있습니다. 해당 작업은 컴파일 및 Localizer 컴포넌트와 관련 에셋들을 갱신하기 때문에 다소 시간이 소요될 수 있습니다.

{% hint style="info" %}
언어의 변경은 Runtime 스크립트 파일에 있는 **Languages.cs** 스크립트의 내용을 수정하고 재컴파일 하는 과정을 거칩니다. 만약 스크립트를 직접 수정한 경우 프로젝트 세팅에서 기존 내용을 복구할 것인지 현재 언어 설정을 사용할 것인지에 대한 선택이 주어집니다. 이런 식으로 언어를 직접 수정하게 되면 컴포넌트들의 언어 설정이 업데이트가 되지 않습니다. 이 경우에는 **Localizer Manager** 에디터 윈도우에서 "Update Project Language Settings" 버튼을 눌러 직접 업데이트 해주어야 합니다.

언어 설정 적용은 **Localizer Project Settings**와 프로젝트 내의 **Localized Dictionary**들의 언어 설정이 갱신되고 현재 씬에 있는 **Localizer Object**들의 언어를 갱신합니다. 현재 씬 이외의 씬들은 이 과정에서 갱신되지 않으며 프로젝트 세팅에 등록되어 있다가 씬이 열릴 때 갱신되고 리스트에서 제외되는 방식으로 이루어집니다.
{% endhint %}

{% hint style="warning" %}
에셋에서 사용되는 기능들은 **Languages.cs** 의 언어 설정을 기반으로 동작됩니다. 이 때 대부분의 기능들이 인덱스를 기반으로 사용되니 가급적 언어의 순서를 바꾸거나 지우는 행위는 하지 말아야 합니다.
{% endhint %}

