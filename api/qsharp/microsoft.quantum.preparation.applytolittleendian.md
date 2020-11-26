---
uid: Microsoft.Quantum.Preparation.ApplyToLittleEndian
title: Операция Апплитолиттлиндиан
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApplyToLittleEndian
qsharp.summary: Applies an operation to the underlying qubits making up a little-endian register. This operation is marked as internal, as a little-endian register is intended to be "opaque," such that this is an implementation detail only.
ms.openlocfilehash: 1194ac369d2d474330357d26dd22709e9c68dd6e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226491"
---
# <a name="applytolittleendian-operation"></a>Операция Апплитолиттлиндиан

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к базовому Кубитс, делая регистр с прямым порядком байтов. Эта операция помечена как внутренняя, так как регистр с прямым порядком байтов должен быть "непрозрачным", так что это только деталь реализации.

```qsharp
operation ApplyToLittleEndian (bareOp : (Qubit[] => Unit is Adj + Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="bareop--qubit--unit--is-adj--ctl"></a>Бареоп: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"




### <a name="register--littleendian"></a>Регистрация: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

