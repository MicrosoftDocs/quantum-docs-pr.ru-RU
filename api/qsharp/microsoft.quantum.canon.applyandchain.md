---
uid: Microsoft.Quantum.Canon.ApplyAndChain
title: Операция Аппляндчаин
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAndChain
qsharp.summary: Computes a chain of AND gates
ms.openlocfilehash: 3991ded1a9c70bf4b58d19b0304a1df3b31896d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842018"
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

