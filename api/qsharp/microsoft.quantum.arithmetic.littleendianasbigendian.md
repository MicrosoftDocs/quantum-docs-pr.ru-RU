---
uid: Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian
title: Функция Литтлиндианасбижендиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndianAsBigEndian
qsharp.summary: Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: 3cdcd18f06bf43d109c9f5e69f319f9d33b96bfc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222751"
---
# <a name="littleendianasbigendian-function"></a><span data-ttu-id="1c277-102">Функция Литтлиндианасбижендиан</span><span class="sxs-lookup"><span data-stu-id="1c277-102">LittleEndianAsBigEndian function</span></span>

<span data-ttu-id="1c277-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1c277-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1c277-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1c277-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1c277-105">Преобразует `LittleEndian` регистр кубит в `BigEndian` регистр кубит, отменяя порядок кубит.</span><span class="sxs-lookup"><span data-stu-id="1c277-105">Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function LittleEndianAsBigEndian (input : Microsoft.Quantum.Arithmetic.LittleEndian) : Microsoft.Quantum.Arithmetic.BigEndian
```


## <a name="input"></a><span data-ttu-id="1c277-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1c277-106">Input</span></span>

### <a name="input--littleendian"></a><span data-ttu-id="1c277-107">входные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1c277-107">input : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1c277-108">Кубит регистр в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="1c277-108">Qubit register in `LittleEndian` format.</span></span>



## <a name="output--bigendian"></a><span data-ttu-id="1c277-109">Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="1c277-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="1c277-110">Кубит регистр в `BigEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="1c277-110">Qubit register in `BigEndian` format.</span></span>