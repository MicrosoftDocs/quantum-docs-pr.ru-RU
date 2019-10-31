---
uid: microsoft.quantum.standardlibsintro
title: Стандартная библиотека Q# для Microsoft Quantum
description: Справочная документация по стандартной библиотеке Q# для Microsoft Quantum
author: natke
ms.author: nakersha
ms.date: 09/04/2019
ms.topic: landing-page
ms.openlocfilehash: 25a53e1cb8577761ef89cdcf2cfcddc509093f86
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "72999083"
---
# <a name="q-standard-libraries"></a><span data-ttu-id="eaf6c-103">Стандартные библиотеки Q#</span><span class="sxs-lookup"><span data-stu-id="eaf6c-103">Q# standard libraries</span></span> #

<span data-ttu-id="eaf6c-104">Q# поддерживается диапазоном различных полезных операций, функций и определяемых пользователем типов, составляющих *стандартную библиотеку* Q#.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard library*.</span></span>
<span data-ttu-id="eaf6c-105">Стандартная библиотека Q# разделяется на две основные части:</span><span class="sxs-lookup"><span data-stu-id="eaf6c-105">The Q# standard library is split into two main parts:</span></span>

- <span data-ttu-id="eaf6c-106">**Вводная часть**: операции и функции, определенные как элемент целевого компьютера и компилятора, обычно c классическим собственным кодом .NET.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-106">**The prelude**: operations and functions defined as a part of the target machine and compiler, typically in classical native .NET code.</span></span>
  <span data-ttu-id="eaf6c-107">Как правило, разные целевые компьютеры могут иметь разные реализации вводной части, соответствующие каждой системе.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-107">In general, different target machines may have different implementations of the prelude appropriate to each system.</span></span>
- <span data-ttu-id="eaf6c-108">**Canon**: операции и функции, определенные в Q#, основываясь на логике, определенной в вводной части.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-108">**The canon**: operations and functions defined in Q# building on the logic defined in the prelude.</span></span>
  <span data-ttu-id="eaf6c-109">Реализация Canon не зависит от целевых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-109">The canon implementation is agnostic with respect to target machines.</span></span>
<span data-ttu-id="eaf6c-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="sxs-lookup"><span data-stu-id="eaf6c-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span></span>