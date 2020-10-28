---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: Функция Блоккенкодингторефлектион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: a8b4c65f8c32f7f9185f1dbdacf8fc75fd4573b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732113"
---
# <a name="blockencodingtoreflection-function"></a><span data-ttu-id="13c1f-102">Функция Блоккенкодингторефлектион</span><span class="sxs-lookup"><span data-stu-id="13c1f-102">BlockEncodingToReflection function</span></span>

<span data-ttu-id="13c1f-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="13c1f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="13c1f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="13c1f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="13c1f-105">Преобразует `BlockEncoding` в эквивалентный `BLockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="13c1f-105">Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.</span></span>

<span data-ttu-id="13c1f-106">То есть, учитывая `BlockEncoding` единое $U $, которое кодирует некоторый оператор $H $ of, преобразует его в `BlockEncodingReflection` $U "$, который кодирует тот же оператор, но также удовлетворяет $U" ^ \Дагжер = U "$.</span><span class="sxs-lookup"><span data-stu-id="13c1f-106">That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$.</span></span>
<span data-ttu-id="13c1f-107">Это увеличивает размер дополнительного регистра $U $ на один кубит.</span><span class="sxs-lookup"><span data-stu-id="13c1f-107">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="13c1f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="13c1f-108">Input</span></span>

### <a name="blockencoding--blockencoding"></a><span data-ttu-id="13c1f-109">Блоккенкодинг: [блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span><span class="sxs-lookup"><span data-stu-id="13c1f-109">blockEncoding : [BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)</span></span>

<span data-ttu-id="13c1f-110">`BlockEncoding`Единое $U $ для преобразования в отражение.</span><span class="sxs-lookup"><span data-stu-id="13c1f-110">A `BlockEncoding` unitary $U$ to be converted into a reflection.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="13c1f-111">Выходные данные: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="13c1f-111">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="13c1f-112">Единая $U "$ действует совместно с регистрами `a` и `s` блок-кодировка $H $ и соответствует $U" ^ \Дагжер = U "$.</span><span class="sxs-lookup"><span data-stu-id="13c1f-112">A unitary $U'$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^\dagger = U'$.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c1f-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="13c1f-113">Remarks</span></span>

<span data-ttu-id="13c1f-114">Это увеличивает размер дополнительного регистра $U $ на один кубит.</span><span class="sxs-lookup"><span data-stu-id="13c1f-114">This increases the size of the auxiliary register of $U$ by one qubit.</span></span>

## <a name="references"></a><span data-ttu-id="13c1f-115">Ссылки</span><span class="sxs-lookup"><span data-stu-id="13c1f-115">References</span></span>

- <span data-ttu-id="13c1f-116">Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="13c1f-116">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="13c1f-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="13c1f-117">See Also</span></span>

- [<span data-ttu-id="13c1f-118">Microsoft. тактов. моделирование. Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="13c1f-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="13c1f-119">Microsoft. тактов. моделирование. Блоккенкодингрефлектион</span><span class="sxs-lookup"><span data-stu-id="13c1f-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)