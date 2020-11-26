---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Функция Блоккенкодингторефлектион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: 742d4f5623c7c26810998f6c96e2c7b05cc452d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225352"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="750ca-102">Функция Блоккенкодингторефлектион</span><span class="sxs-lookup"><span data-stu-id="750ca-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="750ca-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="750ca-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="750ca-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="750ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="750ca-105">Преобразует `BlockEncoding` в эквивалентный `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="750ca-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="750ca-106">То есть, учитывая `BlockEncoding` единое $U $, которое кодирует некоторый оператор $H $ of, преобразует его в `BlockEncodingReflection` $U "$, который кодирует тот же оператор, но также удовлетворяет $U" ^ \Дагжер = U "$.</span><span class="sxs-lookup"><span data-stu-id="750ca-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="750ca-107">Это увеличивает размер дополнительного регистра $U $ на один кубит.</span><span class="sxs-lookup"><span data-stu-id="750ca-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="750ca-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="750ca-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="750ca-109">Блоккенкодинг: [блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="750ca-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="750ca-110">`BlockEncoding`Единое $U $ для преобразования в отражение.</span><span class="sxs-lookup"><span data-stu-id="750ca-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="750ca-111">Выходные данные: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="750ca-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="750ca-112">Единая $U "$ действует совместно с регистрами `a` и `s` блок-кодировка $H $ и соответствует $U" ^ \Дагжер = U "$.</span><span class="sxs-lookup"><span data-stu-id="750ca-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="750ca-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="750ca-113">Remarks</span></span>

<span data-ttu-id="750ca-114">Это увеличивает размер дополнительного регистра $U $ на один кубит.</span><span class="sxs-lookup"><span data-stu-id="750ca-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="750ca-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="750ca-115">References</span></span>

- <span data-ttu-id="750ca-116">Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="750ca-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="750ca-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="750ca-117">See Also</span></span>

- [<span data-ttu-id="750ca-118">Microsoft. тактов. моделирование. Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="750ca-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="750ca-119">Microsoft. тактов. моделирование. Блоккенкодингрефлектион</span><span class="sxs-lookup"><span data-stu-id="750ca-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)