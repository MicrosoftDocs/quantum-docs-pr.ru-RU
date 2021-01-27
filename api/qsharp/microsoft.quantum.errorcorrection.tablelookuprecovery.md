---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: Функция Таблелукупрековери
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: 9f957155e42bb6b5163521171fcba5897f290335
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824395"
---
# <a name="tablelookuprecovery-function"></a>Функция Таблелукупрековери

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Для заданной таблицы операций Паули с заданным регистром Кубитс эта функция возвращает объект типа `RecoveryFn` , который содержит всю информацию, необходимую для декодирования уточняющего запроса таблицы по отношению к заданному массиву операций Паули.

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a>Входные данные

### <a name="table--pauli"></a>Таблица: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Таблица операций Паули, которые работают с заданным регистром кубит



## <a name="output--recoveryfn"></a>Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Объект типа, т `RecoveryFn` . е. карту `Syndrome -> Pauli[]` , которая связывается с заданным массивом синдром и соответствующей операцией исправления Паули.