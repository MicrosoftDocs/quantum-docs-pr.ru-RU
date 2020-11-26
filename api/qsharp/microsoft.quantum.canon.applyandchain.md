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
# <a name="applyandchain-operation"></a><span data-ttu-id="f2038-102">Операция Аппляндчаин</span><span class="sxs-lookup"><span data-stu-id="f2038-102">ApplyAndChain operation</span></span>

<span data-ttu-id="f2038-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f2038-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f2038-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2038-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2038-105">Вычисление цепочки шлюзов и</span><span class="sxs-lookup"><span data-stu-id="f2038-105">Computes a chain of AND gates</span></span>

```qsharp
operation ApplyAndChain (auxRegister : Qubit[], ctrlRegister : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="f2038-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f2038-106">Description</span></span>

<span data-ttu-id="f2038-107">Вспомогательные Кубитс для расчета временных результатов необходимо указать явным образом.</span><span class="sxs-lookup"><span data-stu-id="f2038-107">The auxiliary qubits to compute temporary results must be specified explicitly.</span></span>
<span data-ttu-id="f2038-108">Длина этого регистра равна `Length(ctrlRegister) - 2` , если имеется по крайней мере два элемента управления, в противном случае длина равна 0.</span><span class="sxs-lookup"><span data-stu-id="f2038-108">The length of that register is `Length(ctrlRegister) - 2`, if there are at least two controls, otherwise the length is 0.</span></span>

## <a name="input"></a><span data-ttu-id="f2038-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f2038-109">Input</span></span>

### <a name="auxregister--qubit"></a><span data-ttu-id="f2038-110">Ауксрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f2038-110">auxRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="ctrlregister--qubit"></a><span data-ttu-id="f2038-111">Ктрлрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f2038-111">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="f2038-112">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f2038-112">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f2038-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f2038-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

