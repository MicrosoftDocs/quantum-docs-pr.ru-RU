---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Операция Естиматетермекспектатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713731"
---
# <a name="estimatetermexpectation-operation"></a>Операция Естиматетермекспектатион

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакеты [](https://nuget.org/packages/)


Вычисление энергии, связанной с заданным Jordan-Wignerным термином Хамилтониан

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Описание

Эта операция оценивает значение ожидания, связанное с каждым оператором измерения, и умножает его на соответствующий коэффициент, используя выборку.
Результаты объединяются в переменную, содержащую энергию Jordan-Wigner термина.

## <a name="input"></a>Входные данные

### <a name="inputstateunitary--qubit--unit-adj"></a>Инпутстатеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Единое значение, используемое для подготовки состояния.


### <a name="ops--pauli"></a>Ops: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Операторы измерения Jordan-Wigner термина.


### <a name="coeffs--double"></a>коеффс: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты Jordan-Wignerного термина.


### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс, необходимое для имитации системы молекулярное.


### <a name="nsamples--int"></a>Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)

Количество выборок для оценки условия использования.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Энергия, связанная с Jordan-Wignerным термином.