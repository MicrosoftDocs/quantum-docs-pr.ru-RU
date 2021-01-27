---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Функция СтатепрепаратионпоситивекоеффиЦиентс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855843"
---
# <a name="statepreparationpositivecoefficients-function"></a>Функция СтатепрепаратионпоситивекоеффиЦиентс

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> СтатепрепаратионпоситивекоеффиЦиентс является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>.

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



## <a name="output--littleendian--unit--is-adj--ctl"></a>Выходные данные [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"

Единая операция подготовки состояния $U $.

## <a name="example"></a>Пример

Следующий фрагмент кода готовит состояние такта $ \кет{\пси} = \ sqrt {1/8} \ Сисакет {0} + \ sqrt {7/8} \ Сисакет {2} $ в регистре кубит `qubitsLE` .

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a>Remarks

Отрицательные коэффициенты ввода $ \ alpha_j < $0 будут рассматриваться как положительные со значением $ | \ alpha_j | $. `coefficients` будет дополнен элементами $ \ alpha_j = $0,0, если указано меньше $2 ^ n $.