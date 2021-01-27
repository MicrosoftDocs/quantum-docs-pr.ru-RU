---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: fc3642b76c6e01f0709e78ea42c9ea7237389afa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847180"
---
# <a name="reflectionphases-user-defined-type"></a>Определяемый пользователем тип Рефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Этапы последовательности частичных отражений в усилении амплитуды.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Именованные элементы

### <a name="aboutstart--double"></a>Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния запуска.
### <a name="abouttarget--double"></a>Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния целевого объекта.

## <a name="remarks"></a>Remarks

Оба массива должны иметь одинаковую длину. Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.