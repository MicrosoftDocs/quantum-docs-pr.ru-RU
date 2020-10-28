---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Операция Каррйоуткорекдкм
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 6a292e66f6d9911d2a9075f6397f4f5ba97ec64d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731640"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="ee7db-102">Операция Каррйоуткорекдкм</span><span class="sxs-lookup"><span data-stu-id="ee7db-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="ee7db-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ee7db-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ee7db-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ee7db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ee7db-105">Основная операция в Рипплекарряддеркдкм, используемая с приведенной выше операцией Апплйоутеркдкмаддер, которая была сопряжена с этой операцией для получения внутренней операции Рипплекарряддеркдкм.</span><span class="sxs-lookup"><span data-stu-id="ee7db-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="ee7db-106">Эта операция выполняет вычисление кубит и применяет последовательность нешлюзов для части входных данных `ys` .</span><span class="sxs-lookup"><span data-stu-id="ee7db-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ee7db-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee7db-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="ee7db-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ee7db-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ee7db-109">Первый кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="ee7db-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="ee7db-110">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ee7db-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ee7db-111">Второй кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="ee7db-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="ee7db-112">анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ee7db-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ee7db-113">АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.</span><span class="sxs-lookup"><span data-stu-id="ee7db-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="ee7db-114">выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ee7db-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ee7db-115">Выполните кубит в операции Рипплекарряддеркдкм.</span><span class="sxs-lookup"><span data-stu-id="ee7db-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ee7db-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ee7db-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="ee7db-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="ee7db-117">References</span></span>

- <span data-ttu-id="ee7db-118">Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.</span><span class="sxs-lookup"><span data-stu-id="ee7db-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1