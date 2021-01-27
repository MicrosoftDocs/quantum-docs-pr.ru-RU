---
uid: Microsoft.Quantum.Synthesis.Extended
title: Расширенная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855476"
---
# <a name="extended-function"></a><span data-ttu-id="c774f-102">Расширенная функция</span><span class="sxs-lookup"><span data-stu-id="c774f-102">Extended function</span></span>

<span data-ttu-id="c774f-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c774f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c774f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c774f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c774f-105">Расширяет спектр по инвертированным коэффициентам</span><span class="sxs-lookup"><span data-stu-id="c774f-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="c774f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c774f-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="c774f-107">спектр: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c774f-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c774f-108">Коэффициенты Спектрал</span><span class="sxs-lookup"><span data-stu-id="c774f-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="c774f-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c774f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c774f-110">Коэффициенты, за которыми следует инвертированная копия</span><span class="sxs-lookup"><span data-stu-id="c774f-110">Coefficients followed by inverted copy</span></span>

## <a name="example"></a><span data-ttu-id="c774f-111">Пример</span><span class="sxs-lookup"><span data-stu-id="c774f-111">Example</span></span>

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```