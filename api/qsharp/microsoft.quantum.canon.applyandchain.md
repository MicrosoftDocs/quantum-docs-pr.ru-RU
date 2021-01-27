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
# <a name="applyandchain-operation"></a><span data-ttu-id="3eea7-102">Операция Аппляндчаин</span><span class="sxs-lookup"><span data-stu-id="3eea7-102">ApplyAndChain operation</span></span>

<span data-ttu-id="3eea7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3eea7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3eea7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3eea7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3eea7-105">Вычисление цепочки шлюзов и</span><span class="sxs-lookup"><span data-stu-id="3eea7-105">Computes a chain of AND gates</span></span>

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="3eea7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3eea7-106">Description</span></span>

<span data-ttu-id="3eea7-107">Вспомогательные Кубитс для расчета временных результатов необходимо указать явным образом.</span><span class="sxs-lookup"><span data-stu-id="3eea7-107">The auxiliary qubits to compute temporary results must be specified explicitly.</span></span>
<span data-ttu-id="3eea7-108">Длина этого регистра равна `Length(ctrlRegister) - 2` , если имеется по крайней мере два элемента управления, в противном случае длина равна 0.</span><span class="sxs-lookup"><span data-stu-id="3eea7-108">The length of that register is `Length(ctrlRegister) - 2`, if there are at least two controls, otherwise the length is 0.</span></span>

## <a name="input"></a><span data-ttu-id="3eea7-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3eea7-109">Input</span></span>

### <a name="auxregister--qubit"></a><span data-ttu-id="3eea7-110">Ауксрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3eea7-110">auxRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="ctrlregister--qubit"></a><span data-ttu-id="3eea7-111">Ктрлрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3eea7-111">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="3eea7-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3eea7-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="3eea7-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3eea7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

