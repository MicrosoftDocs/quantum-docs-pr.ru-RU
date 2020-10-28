---
uid: Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian
title: Функция Литтлиндианасбижендиан
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndianAsBigEndian
qsharp.summary: Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: 8c2e6150a839bb0cd4c311c821b78a080288cd22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731449"
---
# <a name="littleendianasbigendian-function"></a><span data-ttu-id="41b02-102">Функция Литтлиндианасбижендиан</span><span class="sxs-lookup"><span data-stu-id="41b02-102">LittleEndianAsBigEndian function</span></span>

<span data-ttu-id="41b02-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="41b02-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="41b02-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41b02-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41b02-105">Преобразует `LittleEndian` регистр кубит в `BigEndian` регистр кубит, отменяя порядок кубит.</span><span class="sxs-lookup"><span data-stu-id="41b02-105">Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function LittleEndianAsBigEndian (input : Microsoft.Quantum.Arithmetic.LittleEndian) : Microsoft.Quantum.Arithmetic.BigEndian
```


## <a name="input"></a><span data-ttu-id="41b02-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="41b02-106">Input</span></span>

### <a name="input--littleendian"></a><span data-ttu-id="41b02-107">входные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="41b02-107">input : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="41b02-108">Кубит регистр в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="41b02-108">Qubit register in `LittleEndian` format.</span></span>



## <a name="output--bigendian"></a><span data-ttu-id="41b02-109">Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="41b02-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="41b02-110">Кубит регистр в `BigEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="41b02-110">Qubit register in `BigEndian` format.</span></span>