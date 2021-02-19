---
description: 에셋에 관하여
---

# Localizer Plus 문서

> 반갑소 세상아!
>
> Hello World!

여러분들이 만들어나가는 창의적인 유니티 게임에 다양한 언어를 도입하여 온 세상을 향해 진출하고자 하는 강인한 의지가 여러분들을 이 곳으로 이끌었습니다!

텍스트 량이 적은 간단한 게임부터 텍스트 량이 많은 게임까지 프로젝트의 규모에 맞추어 가장 적절한 로컬라이징 방법들을 이 에셋에서 찾아볼 수 있습니다.



> ## Q. 대단해요! 이제 뭘 하면 되죠?

시작하기에 앞서 좌측에 보이는 목차에서 _"언어 설정"_ 을 먼저 읽어주세요. 예제를 보고 싶다면 패키지에 포함되어 있는 데모를 직접 플레이 해보거나 목차에서 _"예제 게임"_ 을 읽으셔도 좋습니다.

프로젝트의 규모가 작고 텍스트의 량이 적어 모든 언어의 텍스트를 메모리에 올려두고 사용해도 지장이 없다면 **Localizer Components**와 **Localized Dictionary** 두 가지를 병합하여 사용하면 됩니다.

기존에 이미 있는 csv, tsv 혹은 구글 스프레드 시트가 있다면 **Localized Dictionary**로 변환하여 사용할 수 있습니다. 구글 스프레드 시트의 경우에는 런타임 동안에도 비동기 방식으로 url을 가져와 변환하여 사용할 수 있으니 참고하길 바랍니다.

**LValue&lt;T&gt;**는 로컬라이징을 지원하기 위한 값 클래스 입니다. 다양한 상황에서 유연하게 사용할 수 있습니다. 미리정의된 형식 이외에 직접 추가할 수도 있습니다. 자세한건 해당 항목을 클릭하여 찾아보세요.

**Tag Parameter**는 텍스트 내에 식별 가능한 태그를 넣고 게임에서 태그를 특정 값으로 변경하여 출력할 수 있는 기능을 제공합니다.

**Localizer Viewer** 와 **Localizer Manager** 에디터 윈도우들은 작업의 편의성을 높혀줍니다.

프로젝트의 규모가 크거나 텍스트의 량이 많아 _\(예: 케릭터 대사, 읽을 거리 수집품 등\)_ 메모리에 부담이 생길 수 있다면 **Script** 항목을 찾아보시길 바랍니다. 이는 기존과는 별도의 로컬라이징 기법으로, 곧 바로 사용할 수 있는 형태가 아닌 텍스트들을 파일로 저장하여 언어별로 나눈 다음 필요할 때 로드하여 사용하는 방식입니다.

{% hint style="warning" %}
레퍼런스 참고 : 문서에 작성된 레퍼런스들은 외부 어셈블리에서 사용 가능한 public 멤버들로만 작성되어 있습니다. 해당 문서에 없는 public 멤버들은 실제 빌드에 포함되지 않는 에디터 전용이며 사용시 경고가 표시됩니다.
{% endhint %}

필요하다면 각 항목들의 레퍼런스들을 참고하고 더 다양한 설명을 원한다면 _외부 링크_의 유튜브를 참고하길 바랍니다.



### 여러분들의 세계를 향한 원대한 발걸음에 심심치 않은 경의를 표합니다. 🙂

