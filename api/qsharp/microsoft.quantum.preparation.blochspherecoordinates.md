---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: Функция Блочсферекурдинатес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 62643f64a6b829949fa708e300d9d262527dbb29
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855903"
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