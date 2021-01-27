---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Операция Синглекубитпроцесстомографимеасуремент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 883b98ad4f2d0ac4a02e55e444c04e8e7cf37af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839655"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a>Операция Синглекубитпроцесстомографимеасуремент

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет кубит процесс томографи измерения на основе Паули, учитывая конкретный интересующий Вас канал.

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a>Входные данные

### <a name="preparation--pauli"></a>подготовка: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Элемент Паули базиса $P $, в котором подготавливается кубит.


### <a name="measurement--pauli"></a>Измерение: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Элемент Паули базиса $Q $, в котором измеряется кубит.


### <a name="channel--qubit--unit"></a>канал: [](xref:microsoft.quantum.lang-ref.qubit) => [единица](xref:microsoft.quantum.lang-ref.unit) кубит 

Один канал кубит $ \Ламбда $, поведение которого оценивается с помощью процесса томографи.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат `Zero` с вероятностью $ $ \Бегин{алигн} \пр (\тексттт{зеро} | \ламбда; P, Q) = \Операторнаме{ТР}\лефт (\фрак{\болдоне + Q} {2} \ламбда\лефт [\фрак{\болдоне + P} {2} \ригхт] \ригхт).
\енд{алигн} $ $

## <a name="remarks"></a>Remarks

Распределение по результатам, возвращаемым этой операцией, является особым случаем для двух кубит состояния томографи. Let $ \рхо = J (\Ламбда)/$2 должно быть Чои – Жамиłковски для $ \Ламбда $. Затем приведенный выше дистрибутив идентичен $ $ \бегин{алигн} \Пр (\Тексттт{зеро} | \рхо; M) = \Операторнаме{ТР} (M \рхо), \енд{алигн} $ $ WHERE $M = 2 (\болдоне + P) ^ \Масрм{т}/2 \кдот (\болдоне + Q)/$2 — это эффективное измерение, соответствующее $P $ и $Q $.