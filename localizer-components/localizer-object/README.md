---
description: 에셋의 핵심의 핵심
---

# LocalizerObject

텍스트, 이미지, 오디오 등 실질적으로 게임에서 렌더링 되고 사운드를 재생하는 게임 오브젝트들에게 컴포넌트 형식으로 로컬라이징을 지원합니다. 이 컴포넌트들은 _LocalizerManager.SetLanguage_ 함수가 호출되면 해당 언어에 맞는 내용을 찾아 교체하게 됩니다.

각 컴포넌트들은 그에 해당하는 **LValue&lt;T&gt;** 의 Wrapper 클래스를 가지고 있습니다. 예를 들어 **Text Localizer Object**에는 **LValue&lt;string&gt;** 을 래핑한 **LString** 클래스를 가지며 이 값을 통해 컨텐츠를 가지고 있게 됩니다. 인스펙터 혹은 스크립트 상에서 자유롭게 변경할 수 있습니다.

일부 컴포넌트는 필수 컴포넌트 형식에 따라 상위 컴포넌트를 상속받은 형태로 구현되어 있습니다. 예를 들어 **Text Localizer, Text Mesh Localizer, TMP Text Localizer** 들은 **Text Localizer Object**를 상속받고 있습니다. 이는 RequireComponent 특성을 사용하기 위함이며 **Style Localizer** 들은 여러 컴포넌트를 대상으로 사용되기 때문에 이러한 특성 없이 운용됩니다.



> ### Q. 컴포넌트를 어떻게 추가하죠?

Localizer 컴포넌트 들은 인스펙터상에서 _Add Component - Localizer_ 에서 추가하거나 또는 에디터 상단 메뉴에서 _Component - Localizer_ 에서 추가할 수 있습니다. **Localizer Manager** 에디터 윈도우를 사용 중이라면 Localizer 컴포넌트가 없는 오브젝트를 클릭 했을 때 Add Localizer 버튼이 활성화되고 현재 오브젝트에 부착된 컴포넌트에 해당되는 Localizer 가 자동적으로 추가됩니다.



> ### Q. 언제 사용하죠?

컴포넌트 사용 방식은 별도의 과정 없이 직접적으로 로컬라이징을 하기에 적절한 방법입니다. 인스펙터 상에서 언어별로 내용을 수정할 수 있으며  **Localized Dictionary** 및 **LValue&lt;T&gt;** 를 이용해 스크립트상에서도 편리하게 내용을 변경할 수 있습니다.

다만 이는 프로젝트에서 사용되는 텍스트의 수가 적거나 언어가 적은 경우에만 유효합니다. 텍스트 수가 많다면 언어에 대한 모든 컨텐츠를 메모리에 올려두고 사용하는 것이 부담되기 때문에 내용이 많은 경우라면 **Script**를 사용하거나 적절히 혼용하여 사용하는 것을 추천합니다.

각 Localizer 들에 대한 자세한 내용은 하위 목록에서 찾아볼 수 있습니다.

