---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: Функция СтатепрепаратионкомплекскоеффиЦиентс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: 1d0efa7b83d2e8e75c4b293866f3929f357ec44b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210375"
---
# <a name="statepreparationcomplexcoefficients-function"></a>Функция СтатепрепаратионкомплекскоеффиЦиентс

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> СтатепрепаратионкомплекскоеффиЦиентс является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>.

Возвращает операцию, которая готовит определенное состояние такта.

Возвращенная операция $U $ подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительного состояния $ \ket{0...0} $.

Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} У\кет {0... 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.
\енд{алигн} $ $

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="coefficients--complexpolar"></a>коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]

Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $. Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Выходные данные [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Единая операция подготовки состояния $U $.

## <a name="remarks"></a>Комментарии

Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $. `coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.