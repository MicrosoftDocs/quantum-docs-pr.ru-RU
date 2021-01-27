---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: Функция Мултиплексерфромженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: b86238debe66747ba23c3b41164813594f80b27c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852550"
---
# <a name="multiplexerfromgenerator-function"></a>Функция Мултиплексерфромженератор

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает операцию, зависящую от умножения, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.

$U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a>унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL")

Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a>Выходные данные: ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, зависящая от умножения, $U $, которая применяет унитариес, описанную в `unitaryGenerator` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Мултиплексоператионсфромженератор](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)