---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Операция Естиматинерги
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: a64ac3970e3e67568f91b4e67775d834a80c04a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835729"
---
# <a name="estimateenergy-operation"></a>Операция Естиматинерги

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Оценивает энергию молекулы, суммируя энергию за отдельные условия Jordan-Wigner.

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a>Описание

Эта операция неявным образом зависит от соглашения об индексировании со счетчиком.

## <a name="input"></a>Входные данные

### <a name="jwhamiltonian--jordanwignerencodingdata"></a>Жвхамилтониан: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Jordan-Wigner Хамилтониан.


### <a name="nsamples--int"></a>Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)

Число выборок, используемых для оценки ожидаемых терминов.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Предполагаемое энергопотребление молекулы