---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Операция Естиматетермекспектатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 3f0ff5037b1424abb6fb318bd49ffd89f545822d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224655"
---
# <a name="estimatetermexpectation-operation"></a>Операция Естиматетермекспектатион

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Вычисление энергии, связанной с заданным Jordan-Wignerным термином Хамилтониан

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a>Описание

Эта операция оценивает значение ожидания, связанное с каждым оператором измерения, и умножает его на соответствующий коэффициент, используя выборку.
Результаты объединяются в переменную, содержащую энергию Jordan-Wigner термина.

## <a name="input"></a>Входные данные

### <a name="inputstateunitary--qubit--unit--is-adj"></a>Инпутстатеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

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