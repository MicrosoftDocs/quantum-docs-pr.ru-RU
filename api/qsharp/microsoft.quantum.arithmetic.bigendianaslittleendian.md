---
uid: Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian
title: Функция Бижендианаслиттлиндиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndianAsLittleEndian
qsharp.summary: Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: 5f5d7dc6e08a13fbdc45f9d11c93c29cfcf90bf8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223635"
---
# <a name="bigendianaslittleendian-function"></a><span data-ttu-id="93a39-102">Функция Бижендианаслиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="93a39-102">BigEndianAsLittleEndian function</span></span>

<span data-ttu-id="93a39-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="93a39-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="93a39-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93a39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93a39-105">Преобразует `BigEndian` регистр кубит в `LittleEndian` регистр кубит, отменяя порядок кубит.</span><span class="sxs-lookup"><span data-stu-id="93a39-105">Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function BigEndianAsLittleEndian (input : Microsoft.Quantum.Arithmetic.BigEndian) : Microsoft.Quantum.Arithmetic.LittleEndian
```


## <a name="input"></a><span data-ttu-id="93a39-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="93a39-106">Input</span></span>

### <a name="input--bigendian"></a><span data-ttu-id="93a39-107">входные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="93a39-107">input : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="93a39-108">Кубит регистр в `BigEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="93a39-108">Qubit register in `BigEndian` format.</span></span>



## <a name="output--littleendian"></a><span data-ttu-id="93a39-109">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="93a39-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="93a39-110">Кубит регистр в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="93a39-110">Qubit register in `LittleEndian` format.</span></span>