---
uid: Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian
title: Функция Литтлиндианасбижендиан
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndianAsBigEndian
qsharp.summary: Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: c89288e1eb421fd5abd8fcd5d9c12049aa47ac89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843075"
---
# <a name="littleendianasbigendian-function"></a><span data-ttu-id="1edbf-102">Функция Литтлиндианасбижендиан</span><span class="sxs-lookup"><span data-stu-id="1edbf-102">LittleEndianAsBigEndian function</span></span>

<span data-ttu-id="1edbf-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1edbf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1edbf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1edbf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1edbf-105">Преобразует `LittleEndian` регистр кубит в `BigEndian` регистр кубит, отменяя порядок кубит.</span><span class="sxs-lookup"><span data-stu-id="1edbf-105">Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function LittleEndianAsBigEndian (input : Microsoft.Quantum.Arithmetic.LittleEndian) : Microsoft.Quantum.Arithmetic.BigEndian
```


## <a name="input"></a><span data-ttu-id="1edbf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1edbf-106">Input</span></span>

### <a name="input--littleendian"></a><span data-ttu-id="1edbf-107">входные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1edbf-107">input : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1edbf-108">Кубит регистр в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="1edbf-108">Qubit register in `LittleEndian` format.</span></span>



## <a name="output--bigendian"></a><span data-ttu-id="1edbf-109">Выходные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="1edbf-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="1edbf-110">Кубит регистр в `BigEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="1edbf-110">Qubit register in `BigEndian` format.</span></span>