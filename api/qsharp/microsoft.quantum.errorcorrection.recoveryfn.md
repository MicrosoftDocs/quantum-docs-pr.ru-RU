---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: Определяемый пользователем тип Рековерифн
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 7e8afa37e6225239ae7cafa1f48377a97c43297d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825099"
---
# <a name="recoveryfn-user-defined-type"></a>Определяемый пользователем тип Рековерифн

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Тип для функции, которая сопоставляет ошибку синдром с последовательностью `Pauli[]` операций, исправлять обнаруженную ошибку.

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

