---
description: 나만의 시리얼라이징 LValue<T>
---

# 커스텀 형식 추가

미리 정의된 **LValue\<T>** Wrapper 클래스가 아닌 새 형식을 사용하는 방법입니다.&#x20;

{% hint style="info" %}
유니티 2019.3 이상의 버전 부터는 스크립트 레퍼런스가 지원됨에 따라 Wrapper 클래스를 사용하지 않고 **LValue\<T>** 를 사용하더라도 시리얼라이징이 지원됩니다.
{% endhint %}

## 스크립트 레퍼런스에 의한 사용

```csharp
using UnityEngine;
using LocalizerPlus;

public class TestScript : MonoBehaviour {
    public LValue<float> floatLValue;
}
```

![](../.gitbook/assets/lvalue\_custom\_serialize.PNG)

2019.2 버전 이하에서는 이 기능이 지원되지 않기 때문에 Wrapper 클래스와 프로퍼티 드로워를 작성해야 합니다.&#x20;

## Wrapper 클래스 작성

```csharp
using LocalizerPlus;

[System.Serializable]
public class LFloat : LValue<float> {
    public LFloat () : base () { }
    public LFloat (LFloat value) : base (value) { }
    public LFloat (float[] values) : base (values) { }
}
```

Wrapper 클래스는 다음과 같이 System.Serializable 어트리뷰트와 함께  **LValue\<T>** 를 상속받고 3 가지의 기본 생성자를 구현합니다. 이 때 T 형식은 유니티에서 시리얼라이징이 가능한 형식이어야 합니다. 구조체나 클래스일 경우 System.Serializable 어트리뷰트를 사용합니다.

## 프로퍼티 드로워 작성

프로퍼티 드로워는 UnityEditor의 기능입니다. 이는 Editor 폴더 내에 스크립트가 위치해야 정상적으로 사용될 수 있습니다. 기존 **LValue\<T>**에 사용되는 **LValueDrawer**를 상속받아 사용하는 방법입니다.

```csharp
using UnityEditor;
using LocalizerPlus;

[CustomPropertyDrawer (typeof (LFloat))]
public class LFloatDrawer : LValueDrawer { }
```

{% hint style="info" %}
**LValueDrawer**에 의한 그리기는 언어별 한 줄 (EditorGUIUtility.singleLineHeight) 인 경우에만 정상적으로 그려집니다. 이는 int, float, bool, 오브젝트 레퍼런스에 해당되며 폴드 아웃이 사용되는 요소들인 Vector4, 배열, 리스트, 시리얼라이징 된 구조체나 클래스에는 적용되지 않습니다.
{% endhint %}

**LValueDrawer**는 제한적 입니다. 더 다양한 형식을 그리고 싶다면 PropertyDrawer를 상속받아 직접 그리는 것이 좋습니다.
