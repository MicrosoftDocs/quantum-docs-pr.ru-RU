---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Функция СтатепрепаратионпоситивекоеффиЦиентс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732585"
---
# <a name="statepreparationpositivecoefficients-function"></a>Функция СтатепрепаратионпоситивекоеффиЦиентс

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакеты [](https://nuget.org/packages/)


Возвращает операцию, которая готовит заданное состояние такта.

Возвращаемая операция, $U $, подготавливает произвольное состояние такта $ \ alpha_j \же $0 из $n $-кубит вычислительного состояния $ \ket{0...0} $.

Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} U \ket{0\cdots 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.
\енд{алигн} $ $

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив до $2 ^ n $ коэффициенты $ \ alpha_j $. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.



## <a name="output--littleendian--unit-adj--ctl"></a>Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Единая операция подготовки состояния $U $.

## <a name="remarks"></a>Remarks

Отрицательные коэффициенты ввода $ \ alpha_j < $0 будут рассматриваться как положительные со значением $ | \ alpha_j | $. `coefficients` будет дополнен элементами $ \ alpha_j = $0,0, если указано меньше $2 ^ n $.