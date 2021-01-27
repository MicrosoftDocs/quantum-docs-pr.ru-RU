---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Пространство имен Microsoft. тактов. Амплитудеамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: a014f923de62c5e660c1c0fc839fbe60e80f8ba9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845827"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a>Пространство имен Microsoft. тактов. Амплитудеамплификатион

Это пространство имен содержит функции и операции для выполнения усиления амплитуды.



## <a name="description"></a>Описание

Усиление амплитуды очевидным с частичными отражениями — это наиболее Общая форма реализации усиления амплитуды.

Это вызывается с помощью операции Ампампобливиаусбирефлектионфасес.

Он имеет два регистра: `ancillaRegister` и `systemRegister` .

Это принимает две Oracle для этих отражений типа `ReflectionOracle` , которые работают только с `ancillaRegister` регистром.

При этом принимается специальное значение Oracle для очевиднымности амплитуды типа `ObliviousOracle` , который работает совместно с обеими регистрами.

Предполагается, что входное состояние `ancillaRegister` — это уникальный $-$1 еиженстате первого оператора отражения $I-2 \ Сисакет {s} \ неверное {s} $.

Отражения, связанные с состоянием целевого такта, часто реализуются при условии доступа к Oracle, который подготавливает это состояние от вычислительной базы $ \ket{0\cdots 0} $.

Для нашего соглашения для этих Oracle требуется два регистра: один кубит `flagQubit` регистр и регистр для всех остальных элементов регистра анЦилларегистер.

Oracle типа `StateOracle` работает совместно с обоими регистрами для создания целевого состояния, помеченного $ \кет {1} $ в `flagQubit` регистре, с некоторой реальной амплитудой.

Отражение `ReflectionOracle` о состоянии этого флага создается операцией `TargetStateReflectionOracle` .

Отражение `ReflectionOracle` состояния ввода `ancillaRegister` создается инвертированным статеоракле, а затем отразится около $ \ket{0\cdots 0} $ с рефлектионстарт ().

Oracle типа `DeterministicStateOracle` обрабатывает `qubitState` регистры для создания целевого состояния точно без флага.

`AmpAmpObliviousByOraclePhases` — Это версия усиления амплитуды очевидным, которая принимает Oracle `StateOracle` и `ObliviousOracle` вместо отражения.

Обратите внимание, что усиление амплитуды является особым случаем для очевидныма амплитуды `ObliviousOracle` , где является оператором идентификации, и отсутствует системный Кубитс, т. е. `systemRegister` пустой.

Это вызывается с помощью операции `AmpAmByReflectionPhases` и `AmpAmpByOraclePhases` .

Этапы частичной отражения в стандартном случае поиска Гровер предоставляются функцией Ампампфасесстандард.

Например, у нас есть следующие зависимости: Ампампбйоракле-> Ампампбйораклефасес-> Ампампобливиаусбйораклефасес-> Ампампобливиаусбирефлектионфасес.