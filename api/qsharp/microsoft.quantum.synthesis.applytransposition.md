---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: Операция Апплитранспоситион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855578"
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



## <a name="example"></a>Пример

Подготовьте единое геоотносительное количество Штатов $ | 1 \ рангле $, $ | 2 \ рангле $ и $ | 3 \ рангле $ on 2 Кубитс.

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```