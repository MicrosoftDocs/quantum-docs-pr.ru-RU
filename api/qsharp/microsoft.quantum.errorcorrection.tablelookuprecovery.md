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
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="43826-102">Функция Таблелукупрековери</span><span class="sxs-lookup"><span data-stu-id="43826-102">TableLookupRecovery function</span></span>

<span data-ttu-id="43826-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="43826-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="43826-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43826-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43826-105">Для заданной таблицы операций Паули с заданным регистром Кубитс эта функция возвращает объект типа `RecoveryFn` , который содержит всю информацию, необходимую для декодирования уточняющего запроса таблицы по отношению к заданному массиву операций Паули.</span><span class="sxs-lookup"><span data-stu-id="43826-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="43826-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="43826-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="43826-107">Таблица: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="43826-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="43826-108">Таблица операций Паули, которые работают с заданным регистром кубит</span><span class="sxs-lookup"><span data-stu-id="43826-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="43826-109">Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="43826-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="43826-110">Объект типа, т `RecoveryFn` . е. карту `Syndrome -> Pauli[]` , которая связывается с заданным массивом синдром и соответствующей операцией исправления Паули.</span><span class="sxs-lookup"><span data-stu-id="43826-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>