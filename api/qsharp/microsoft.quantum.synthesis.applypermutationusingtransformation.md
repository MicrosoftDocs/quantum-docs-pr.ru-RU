---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Операция Апплипермутатионусингтрансформатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: a05b433eae2612bbf5c87522c4ef251976184aa8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192066"
---
# <a name="applypermutationusingtransformation-operation"></a>Операция Апплипермутатионусингтрансформатион

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе преобразования.

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта процедура реализует метод синтеза на основе однонаправленного преобразования.  Входные данные — это перестановка $ \пи $ over $2 ^ n $ Elements $ \{ 0, \дотс, 2 ^ n-1 \} $, представляющая $n $-Variable обратимая логическая функция.
Алгоритм последовательно выполняет следующие шаги:

1. Найдите наименьшее $x $ например, $x \не \пи (x) = y $.
2. Поиск нескольких управляемых операций Тоффоли, которые применяются к выходам, делают $ \пи (x) = x $ и не изменяют $ \пи (x ') $ для всех $x "< x $

## <a name="input"></a>Входные данные

### <a name="perm--int"></a>разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]

Перестановка элементов $2 ^ n $, начиная с 0.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Список $n $ Кубитс, к которому применяется перестановка.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- [*Г. Майкл Миллер*, *Дмитрий Маслов*, *жерхард W. дуекк*, proc. DAC 2003, IEEE, PP. 318-323, 2003](https://doi.org/10.1145/775832.775915)
- [*Матиас соекен*, *Жерхард W. дуекк*, *D. Майкл миллер*, proc. RC 2016, springer link, PP. 307-321, 2016](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситион](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)