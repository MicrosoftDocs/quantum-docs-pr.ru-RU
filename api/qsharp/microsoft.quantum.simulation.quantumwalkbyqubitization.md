---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: Функция Куантумвалкбикубитизатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: 8ffb6eb77a3f910d3064c4a3c90215d5d9a694aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851052"
---
# <a name="quantumwalkbyqubitization-function"></a>Функция Куантумвалкбикубитизатион

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует отражение кодирования блока в проход такта.

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a>Описание

Учитывая значение, `BlockEncodingReflection` представленное единым $U $, которое кодирует какой-то оператор $H $ of, преобразует его в проход такта $W $, содержащий спектр $ \пм e ^ {\пм и\син ^ {-1} (H)} $.

## <a name="input"></a>Входные данные

### <a name="blockencoding--blockencodingreflection"></a>Блоккенкодинг: [блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

`BlockEncodingReflection`Единое $U $ для преобразования в проход такта.



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Проверка такта $W $ действует совместно с регистрами `a` и `s` кодирует $H $ и содержит спектр $ \пм e ^ {\пм и\син ^ {-1} (H)} $.

## <a name="references"></a>Ссылки

- Имитация хамилтониан с Кубитизатион Guang Хао Low, Исаак L. Чжуанский https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. моделирование. Блоккенкодинг](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Microsoft. тактов. моделирование. Блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)