---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Операция Апплипермутатионусингдекомпоситионвисвариаблеордер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: f33d2980ff1775b1ae8d2e2e7a4fa1e5cbe7d5ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858878"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a>Операция Апплипермутатионусингдекомпоситионвисвариаблеордер

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе декомпозиции.

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция является более общей версией, @"microsoft.quantum.synthesis.applypermutationusingdecomposition" в которой можно указать порядок переменных. Другой порядок переменных изменяет последовательность декомпозиции и таблицы истинности, используемые для управляемых @"microsoft.quantum.intrinsic.x" шлюзов.  Поэтому при изменении порядка переменных изменяется количество общих шлюзов, используемых для реализации перестановки.

## <a name="input"></a>Входные данные

### <a name="perm--int"></a>разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]

Перестановка элементов $2 ^ n $, начиная с 0.


### <a name="variableorder--int"></a>Вариаблеордер: [int](xref:microsoft.quantum.lang-ref.int)[]

Перестановка элементов $n $, начиная с 0.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Список $n $ Кубитс, к которому применяется перестановка.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

Для синтезирования `SWAP` операции выполните следующие действия.

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingDecompositionWithVariableOrder([0, 2, 1, 3], [1, 0], LittleEndian(qubits));
}
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситион](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [Microsoft. тактов. синтез. Апплипермутатионусингтрансформатион](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)