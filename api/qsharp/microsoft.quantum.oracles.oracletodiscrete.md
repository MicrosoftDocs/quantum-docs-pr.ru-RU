---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: Функция Ораклетодискрете
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842537"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="09ef9-102">Функция Ораклетодискрете</span><span class="sxs-lookup"><span data-stu-id="09ef9-102">OracleToDiscrete function</span></span>

<span data-ttu-id="09ef9-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="09ef9-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="09ef9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09ef9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09ef9-105">При наличии операции, представляющей "черный ящик" Oracle, возвращает отдельную репликацию Oracle, которая представляет "черный ящик", повторяющийся несколько раз.</span><span class="sxs-lookup"><span data-stu-id="09ef9-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="09ef9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="09ef9-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="09ef9-107">Блаккбоксоракле: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="09ef9-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="09ef9-108">Возведен операция.</span><span class="sxs-lookup"><span data-stu-id="09ef9-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="09ef9-109">Выходные данные: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="09ef9-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="09ef9-110">Операция частично применена к "черному ящику" Oracle, представляющему Дискретное время Oracle</span><span class="sxs-lookup"><span data-stu-id="09ef9-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>

## <a name="example"></a><span data-ttu-id="09ef9-111">Пример</span><span class="sxs-lookup"><span data-stu-id="09ef9-111">Example</span></span>

<span data-ttu-id="09ef9-112">`OracleToDiscrete(U)(3, target)` эквивалентно `U(target)` повторяется три раза.</span><span class="sxs-lookup"><span data-stu-id="09ef9-112">`OracleToDiscrete(U)(3, target)` is equivalent to `U(target)` repeated three times.</span></span>