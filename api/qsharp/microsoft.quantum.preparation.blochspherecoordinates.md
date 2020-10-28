---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: Функция Блочсферекурдинатес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 6614b78c8e64c205cc94052cc64dd957814ab3d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733264"
---
# <a name="blochspherecoordinates-function"></a>Функция Блочсферекурдинатес

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакеты [](https://nuget.org/packages/)


Выполняет вычисление координат БЛОЧ-сферы для одного кубит состояния.

Учитывая два комплексных числа $a 0, a1 $, которые представляют состояние кубит, рассчитывает координаты в блочной сфере, что $a 0 \кет {0} + a1 \кет {1} = r e ^ {IT} (e ^ {-i \фи/2}\cos{(\ тета/2)} \кет {0} + e ^ {i \фи/2}\sin{(\ тета/2)} \кет {1} ) $.

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a>Входные данные

### <a name="a0--complexpolar"></a>a0: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)

Сложный коэффициент состояния $ \кет {0} $.


### <a name="a1--complexpolar"></a>a1: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)

Сложный коэффициент состояния $ \кет {1} $.



## <a name="output--complexpolardoubledouble"></a>Выходные данные: ([комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))

Кортеж, содержащий `(ComplexPolar(r, t), phi, theta)` .