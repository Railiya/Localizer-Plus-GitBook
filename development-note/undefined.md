---
description: 향후 개발 예정에 있거나 고민중인 사항들
---

# 지원 예정

## 추후 개발 예정 사항

1. 메인 메뉴 \(언어 변경\) - 인 게임 로딩 중 cscrt 로드 예제 추가
2. 첫 번째 예제 게임 시작시 초기 언어 설정 넣기
3. 첫 번째 예제 게임에서 cscrt 관련 스크립트 제거 및 Localized Dictionary로 변경
4. Text Localizer \(및 TMP Localizer\) 의 오버라이딩 옵션과 해당되는 값들을 Style Localizer 컴포넌트로 분할 \(성능적 이슈 보완\)
5. Localized Dictionary 인스펙터 내에서 새로운 KeyContentsPair 임포트 기능 넣기
6. Localized Dictionary 에서 Open Script Writer 가능 넣기
7. Localized Dictionary 및 swnc 파일을 실시간으로 인 게임 UI에 적용해가며 테스트하기 위한 새로운 에디터 윈도우 도입
8. Right To Left 기능 도입

## 우리들의 소통 현황

* 입문자들을 위한 예제가 부족하다.
* 현재 데모에서 cscrt 의 사용법이 부적절하다.
* Text Localizer \(및 TMP Localizer\)의 기능들이 너무 밀집되어있다. cscrt의 경우 Localizer를 통해서가 아닌 Text 컴포넌트로 직접 수정하는 편이 좋을 것이다. 폰트 및 라인 스페이싱 기능들만 따로 빼두는 편이 성능적으로 유리하다.
* Text 와 Text Mesh, Sprite와 Image 각각의 Localizer를 나눠 RequireComponent 애트리뷰트를 사용하는 것이 사용하는 이의 측면에서 바람직하다.
* Localized Dictionary 의 임포트 기능이 너무 깊이 있다.
* 에디터들의 상단 메뉴의 단어 통일성이 부족하다. \(Edit.. Export..\)

## 개발자의 한 마디

> 살려주세요.



