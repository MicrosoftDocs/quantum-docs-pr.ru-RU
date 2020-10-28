---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Функция Ораклетодискрете
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733360"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="523c6-102">Функция Ораклетодискрете</span><span class="sxs-lookup"><span data-stu-id="523c6-102">OracleToDiscrete function</span></span>

<span data-ttu-id="523c6-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="523c6-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="523c6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="523c6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="523c6-105">При наличии операции, представляющей "черный ящик" Oracle, возвращает отдельную репликацию Oracle, которая представляет "черный ящик", повторяющийся несколько раз.</span><span class="sxs-lookup"><span data-stu-id="523c6-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="523c6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="523c6-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a><span data-ttu-id="523c6-107">Блаккбоксоракле: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="523c6-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="523c6-108">Возведен операция.</span><span class="sxs-lookup"><span data-stu-id="523c6-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="523c6-109">Выходные данные: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="523c6-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="523c6-110">Операция частично применена к "черному ящику" Oracle, представляющему Дискретное время Oracle</span><span class="sxs-lookup"><span data-stu-id="523c6-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>