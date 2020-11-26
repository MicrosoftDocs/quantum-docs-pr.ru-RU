---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Операция Апплитранспоситион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203320"
---
# <a name="applytransposition-operation"></a>Операция Апплитранспоситион

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция меняет местами амплитуду с индексом на `a` амплитуду по индексу `b` в заданном векторе состояния `register` длины $n $.  Если `a` равно `b` , вектор состояния не изменяется.

## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)

Первый индекс (должен быть значением от 0 до $2 ^ n-$1)


### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)

Второй индекс (должен быть значением от 0 до $2 ^ n-$1)


### <a name="qubits--littleendian"></a>Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Список $n $ Кубитс, к которому применяется транспоситион.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

