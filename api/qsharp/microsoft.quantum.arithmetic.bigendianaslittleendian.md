---
uid: Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian
title: Функция Бижендианаслиттлиндиан
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndianAsLittleEndian
qsharp.summary: Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: cb4cf68753468952c7541fae23250ed1fd1914f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843371"
---
# <a name="bigendianaslittleendian-function"></a><span data-ttu-id="93a16-102">Функция Бижендианаслиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="93a16-102">BigEndianAsLittleEndian function</span></span>

<span data-ttu-id="93a16-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="93a16-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="93a16-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93a16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93a16-105">Преобразует `BigEndian` регистр кубит в `LittleEndian` регистр кубит, отменяя порядок кубит.</span><span class="sxs-lookup"><span data-stu-id="93a16-105">Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function BigEndianAsLittleEndian (input : Microsoft.Quantum.Arithmetic.BigEndian) : Microsoft.Quantum.Arithmetic.LittleEndian
```


## <a name="input"></a><span data-ttu-id="93a16-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="93a16-106">Input</span></span>

### <a name="input--bigendian"></a><span data-ttu-id="93a16-107">входные данные: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="93a16-107">input : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="93a16-108">Кубит регистр в `BigEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="93a16-108">Qubit register in `BigEndian` format.</span></span>



## <a name="output--littleendian"></a><span data-ttu-id="93a16-109">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="93a16-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="93a16-110">Кубит регистр в `LittleEndian` формате.</span><span class="sxs-lookup"><span data-stu-id="93a16-110">Qubit register in `LittleEndian` format.</span></span>