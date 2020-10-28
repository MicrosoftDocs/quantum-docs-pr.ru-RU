---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Операция Апплитолиттлиндиан
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: d94a9969a3f827d594946ab8ca6cd4672da7ef7e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733280"
---
# <a name="applytolittleendian-operation"></a><span data-ttu-id="4dc22-102">Операция Апплитолиттлиндиан</span><span class="sxs-lookup"><span data-stu-id="4dc22-102">ApplyToLittleEndian operation</span></span>

<span data-ttu-id="4dc22-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="4dc22-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="4dc22-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4dc22-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4dc22-105">Применяет операцию к базовому Кубитс, делая регистр с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4dc22-105">Applies an operation to the underlying qubits making up a little-endian register.</span></span> <span data-ttu-id="4dc22-106">Эта операция помечена как внутренняя, так как регистр с прямым порядком байтов должен быть "непрозрачным", так что это только деталь реализации.</span><span class="sxs-lookup"><span data-stu-id="4dc22-106">This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.</span></span>

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="4dc22-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4dc22-107">Input</span></span>

### <a name="bareop--qubit--unit-adj--ctl"></a><span data-ttu-id="4dc22-108">Бареоп: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="4dc22-108">bareOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="register--littleendian"></a><span data-ttu-id="4dc22-109">Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4dc22-109">register : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>





## <a name="output--unit"></a><span data-ttu-id="4dc22-110">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4dc22-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

