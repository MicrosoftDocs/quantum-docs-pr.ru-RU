---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Операция Аппликсконтролледонтрустаблевисклеантаржет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 904ff7e2e7e81ee966846af120e9427f4e92301c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203269"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a>Операция Аппликсконтролледонтрустаблевисклеантаржет

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет @"microsoft.quantum.intrinsic.x" операцию к `target` , если логическая функция `func` возвращает значение true для классического назначения в `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция реализует особый случай @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , в котором Целевая кубит находится в состоянии $ \кет {0} $.

В реализации используются @"microsoft.quantum.intrinsic.cnot" @"microsoft.quantum.intrinsic.r1" шлюзы и.  Реализация примыкающей операции оптимизирована и использует невычисление на основе измерения.

## <a name="input"></a>Входные данные

### <a name="func--bigint"></a>Func: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Логическая таблица истинности, представленная как большое целое число


### <a name="controlregister--qubit"></a>Контролрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация элемента управления Кубитс


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит (должен находиться в $ \кет {0} $ State)



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. синтез. Аппликсконтролледонтрустабле](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)