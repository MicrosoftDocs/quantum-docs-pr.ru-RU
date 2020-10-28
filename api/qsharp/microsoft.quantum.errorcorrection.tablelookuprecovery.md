---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: Функция Таблелукупрековери
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: c56a9bbb1db72b5ba03ee9976e648a59f651aa16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712051"
---
# <a name="tablelookuprecovery-function"></a>Функция Таблелукупрековери

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Для заданной таблицы операций Паули с заданным регистром Кубитс эта функция возвращает объект типа `RecoveryFn` , который содержит всю информацию, необходимую для декодирования уточняющего запроса таблицы по отношению к заданному массиву операций Паули.

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a>Входные данные

### <a name="table--pauli"></a>Таблица: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Таблица операций Паули, которые работают с заданным регистром кубит



## <a name="output--recoveryfn"></a>Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Объект типа, т `RecoveryFn` . е. карту `Syndrome -> Pauli[]` , которая связывается с заданным массивом синдром и соответствующей операцией исправления Паули.