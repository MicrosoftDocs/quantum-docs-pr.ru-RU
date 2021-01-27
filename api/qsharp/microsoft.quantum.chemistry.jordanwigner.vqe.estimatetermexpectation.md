---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Операция Естиматетермекспектатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835668"
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