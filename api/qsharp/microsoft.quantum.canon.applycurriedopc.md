---
uid: Microsoft.Quantum.Canon.ApplyCurriedOpC
title: Операция Аппликурриедопк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCurriedOpC
qsharp.summary: ''
ms.openlocfilehash: 65e861914b57cf8a32f2321f881248830b72c54e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841904"
---
# <a name="applycurriedopc-operation"></a><span data-ttu-id="f36b2-102">Операция Аппликурриедопк</span><span class="sxs-lookup"><span data-stu-id="f36b2-102">ApplyCurriedOpC operation</span></span>

<span data-ttu-id="f36b2-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f36b2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f36b2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f36b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyCurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl)), first : 'T, second : 'U) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="f36b2-105">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f36b2-105">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="f36b2-106">Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="f36b2-106">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="first--t"></a><span data-ttu-id="f36b2-107">Первый: 'T</span><span class="sxs-lookup"><span data-stu-id="f36b2-107">first : 'T</span></span>




### <a name="second--u"></a><span data-ttu-id="f36b2-108">секунд: ' U</span><span class="sxs-lookup"><span data-stu-id="f36b2-108">second : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="f36b2-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f36b2-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f36b2-110">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f36b2-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f36b2-111">Е</span><span class="sxs-lookup"><span data-stu-id="f36b2-111">'T</span></span>


### <a name="u"></a><span data-ttu-id="f36b2-112">' U</span><span class="sxs-lookup"><span data-stu-id="f36b2-112">'U</span></span>

