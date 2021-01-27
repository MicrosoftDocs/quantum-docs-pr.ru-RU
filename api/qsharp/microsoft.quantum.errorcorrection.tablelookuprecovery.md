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
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="420f8-102">Функция Таблелукупрековери</span><span class="sxs-lookup"><span data-stu-id="420f8-102">TableLookupRecovery function</span></span>

<span data-ttu-id="420f8-103">Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="420f8-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="420f8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="420f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="420f8-105">Для заданной таблицы операций Паули с заданным регистром Кубитс эта функция возвращает объект типа `RecoveryFn` , который содержит всю информацию, необходимую для декодирования уточняющего запроса таблицы по отношению к заданному массиву операций Паули.</span><span class="sxs-lookup"><span data-stu-id="420f8-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="420f8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="420f8-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="420f8-107">Таблица: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="420f8-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="420f8-108">Таблица операций Паули, которые работают с заданным регистром кубит</span><span class="sxs-lookup"><span data-stu-id="420f8-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="420f8-109">Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="420f8-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="420f8-110">Объект типа, т `RecoveryFn` . е. карту `Syndrome -> Pauli[]` , которая связывается с заданным массивом синдром и соответствующей операцией исправления Паули.</span><span class="sxs-lookup"><span data-stu-id="420f8-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>