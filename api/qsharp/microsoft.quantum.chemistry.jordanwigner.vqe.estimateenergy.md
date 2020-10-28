---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Операция Естиматинерги
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713746"
---
# <a name="estimateenergy-operation"></a>Операция Естиматинерги

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакеты [](https://nuget.org/packages/)


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