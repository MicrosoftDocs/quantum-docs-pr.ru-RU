---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: Функция Блочсферекурдинатес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 594896a72fe40e5ba994e08500c3ce71b185bfff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193562"
---
# <a name="blochspherecoordinates-function"></a>Функция Блочсферекурдинатес

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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