---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Операция Апплипермутатионусингдекомпоситион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733969"
---
# <a name="applypermutationusingdecomposition-operation"></a>Операция Апплипермутатионусингдекомпоситион

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакеты [](https://nuget.org/packages/)


Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе декомпозиции.

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Описание

Эта процедура реализует метод синтеза на основе декомпозиции.  Входные данные представляют собой перестановку $ \пи $ over $2 ^ n $ Elements $ \{ 0, \дотс, 2 ^ n-1 \} $, который представляет переменную $n $-Variable обратимую логическую функцию.
Алгоритм последовательно выполняет следующие действия для каждого индекса переменной $i $:

1. Compute $ ((\ pi_l, \ pi_r), \пи ') $ таким, что изображения $ \ pi_l $ и $ \ pi_r $ не изменяют биты в своих элементах в индексах, отличных от $i $, а изображения $ \пи ' $ не изменяют бит $i $ в своих элементах.
2. Задайте $ \пи \лефтарров \пи "$" и производные таблицы истинности от $ \ pi_l $ и $ \ pi_r $ на основе элементов, которые не являются фиксированными точками.

После применения этих шагов для всех переменных индексов оставшаяся перестановка $ \пи $ будет являться удостоверением, и на основе собранных таблиц и индексов истинности можно применить операции, контролируемые истинной таблицей, @"microsoft.quantum.intrinsic.x" с помощью @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" операции.

Порядок переменных — $0, \дотс, n-$1.  В операции можно указать пользовательский порядок переменных @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .

## <a name="input"></a>Входные данные

### <a name="perm--int"></a>разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]

Перестановка элементов $2 ^ n $, начиная с 0.


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Список $n $ Кубитс, к которому применяется перестановка.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- [*Алексис de вос* , *Иван Van рентержем* , rebys. of Dataport. 2 (2), 2008, PP. 183--200](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [*Матиас соекен* , *Мария Тагуе* , *жерхард W. дуекк* , *ролф дречслер* , журнал символьных вычислений 73 (2016), PP. 1--26](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситионвисвариаблеордер](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [Microsoft. тактов. синтез. Апплипермутатионусингтрансформатион](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)