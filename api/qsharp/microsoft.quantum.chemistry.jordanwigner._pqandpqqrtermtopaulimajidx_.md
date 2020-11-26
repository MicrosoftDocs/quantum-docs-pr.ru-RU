---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQandPQQRTermToPauliMajIdx_
title: Функция _пкандпккртермтопаулимажидкс_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQandPQQRTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ or PQQR term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 1a04f5f3b66e0dccb650b2d451a086a380b9810a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225012"
---
# <a name="_pqandpqqrtermtopaulimajidx_-function"></a>Функция _пкандпккртермтопаулимажидкс_

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Преобразует Женераториндекс, описывающий термин PQ или ПККР, в выражение "Женераториндекс []" с точки зрения пол.

```qsharp
function _PQandPQQRTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a>Входные данные

### <a name="term--generatorindex"></a>термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` представление термина PQ или ПККР.



## <a name="output--optimizedbetermindex"></a>Выходные данные: [оптимизедбетерминдекс](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)

"Женераториндекс []" выражает PQ или ПККР термин как Паули условия.