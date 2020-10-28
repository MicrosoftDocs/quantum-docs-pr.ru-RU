---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Функция Куантумвалкбикубитизатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ef9740f1867cee3c79a7ec0bf90f2c2f4b39ad28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734120"
---
# <a name="quantumwalkbyqubitization-function"></a><span data-ttu-id="1bf97-102">Функция Куантумвалкбикубитизатион</span><span class="sxs-lookup"><span data-stu-id="1bf97-102">QuantumWalkByQubitization function</span></span>

<span data-ttu-id="1bf97-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1bf97-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1bf97-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1bf97-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1bf97-105">Преобразует отражение кодирования блока в проход такта.</span><span class="sxs-lookup"><span data-stu-id="1bf97-105">Converts a block-encoding reflection into a quantum walk.</span></span>

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="1bf97-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1bf97-106">Description</span></span>

<span data-ttu-id="1bf97-107">Учитывая значение, `BlockEncodingReflection` представленное единым $U $, которое кодирует какой-то оператор $H $ of, преобразует его в проход такта $W $, содержащий спектр $ \пм e ^ {\пм и\син ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="1bf97-107">Given a `BlockEncodingReflection` represented by a unitary $U$ that encodes some operator $H$ of interest, converts it into a quantum walk $W$ containing the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="input"></a><span data-ttu-id="1bf97-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1bf97-108">Input</span></span>

### <a name="blockencoding--blockencodingreflection"></a><span data-ttu-id="1bf97-109">Блоккенкодинг: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="1bf97-109">blockEncoding : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="1bf97-110">`BlockEncodingReflection`Единое $U $ для преобразования в проход такта.</span><span class="sxs-lookup"><span data-stu-id="1bf97-110">A `BlockEncodingReflection` unitary $U$ to be converted into a Quantum walk.</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="1bf97-111">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия</span><span class="sxs-lookup"><span data-stu-id="1bf97-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="1bf97-112">Проверка такта $W $ действует совместно с регистрами `a` и `s` кодирует $H $ и содержит спектр $ \пм e ^ {\пм и\син ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="1bf97-112">A quantum walk $W$ acting jointly on registers `a` and `s` that block- encodes $H$, and contains the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="references"></a><span data-ttu-id="1bf97-113">Ссылки</span><span class="sxs-lookup"><span data-stu-id="1bf97-113">References</span></span>

- <span data-ttu-id="1bf97-114">Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="1bf97-114">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="1bf97-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="1bf97-115">See Also</span></span>

- [<span data-ttu-id="1bf97-116">Microsoft. тактов. моделирование. Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="1bf97-116">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="1bf97-117">Microsoft. тактов. моделирование. Блоккенкодингрефлектион</span><span class="sxs-lookup"><span data-stu-id="1bf97-117">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)