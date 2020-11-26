---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: Операция Аппляндчаин
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: c53bca6ecf964f4358b0a7ff1c61d4e8e195cd7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219368"
---
# <a name="applyandchain-operation"></a>Операция Аппляндчаин

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление цепочки шлюзов и

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a>Описание

Вспомогательные Кубитс для расчета временных результатов необходимо указать явным образом.
Длина этого регистра равна `Length(ctrlRegister) - 2` , если имеется по крайней мере два элемента управления, в противном случае длина равна 0.

## <a name="input"></a>Входные данные

### <a name="auxregister--qubit"></a>Ауксрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="ctrlregister--qubit"></a>Ктрлрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

