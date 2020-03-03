---
title: Базовые сведения о пакете средств для квантового машинного обучения | Документация Майкрософт
description: Базовые сведения о пакете средств для квантового машинного обучения
author: QuantumWriter
ms.author: alexeib@microsoft.com
ms.date: 12/5/2019
ms.topic: article
uid: microsoft.quantum.machine-learning.concepts.intro
ms.openlocfilehash: 7f22d5d3212890abc764f88693937b534466170f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907857"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a><span data-ttu-id="2faae-103">Базовые сведения о библиотеке квантового машинного обучения</span><span class="sxs-lookup"><span data-stu-id="2faae-103">Introduction to the Quantum Machine Learning Library</span></span>

<span data-ttu-id="2faae-104">Библиотека квантового машинного обучения — это API-интерфейс, написанный на Q#. Он позволяет выполнять гибридные квантовые и классические эксперименты машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="2faae-104">The Quantum Machine Learning Library is an API, written in Q#, that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="2faae-105">Библиотека предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="2faae-105">The library gives you the ability to:</span></span>

- <span data-ttu-id="2faae-106">загрузка собственных данных для классификации с помощью квантовых симуляторов;</span><span class="sxs-lookup"><span data-stu-id="2faae-106">Load your own data to classify with quantum simulators</span></span>

- <span data-ttu-id="2faae-107">освоение области квантового машинного обучения с помощью примеров и руководств.</span><span class="sxs-lookup"><span data-stu-id="2faae-107">Use samples and tutorials to get introduced to the field of quantum machine learning</span></span>

<span data-ttu-id="2faae-108">Скорее всего, производительность будет низкой по сравнению с текущими классическими платформами машинного обучения (учитывайте, что все выполняется на основе имитированного квантового устройства, что само по себе затратно в плане вычислительных ресурсов).</span><span class="sxs-lookup"><span data-stu-id="2faae-108">You can expect low performance compared to current classical machine learning frameworks (remember that everything is running on top of the simulation of a quantum device that is already computationally expensive).</span></span>

<span data-ttu-id="2faae-109">Назначение этой документации:</span><span class="sxs-lookup"><span data-stu-id="2faae-109">The purpose of this documentation is:</span></span>

- <span data-ttu-id="2faae-110">краткое описание средств (на Q\#) для гибридного квантового и классического машинного обучения;</span><span class="sxs-lookup"><span data-stu-id="2faae-110">A concise introduction to machine learning tools (written in Q\#) for hybrid quantum/classical learning.</span></span>
- <span data-ttu-id="2faae-111">раскрытие понятий машинного обучения, в частности их реализации в классификаторах, ориентированных на квантовые схемы (также называются квантовыми последовательными классификаторами);</span><span class="sxs-lookup"><span data-stu-id="2faae-111">Introduce machine learning concepts and specifically their realization in quantum circuit centric classifiers (also known as quantum sequential classifiers).</span></span>
- <span data-ttu-id="2faae-112">предоставление ряда руководств с основными сведениями для начала работы со средствами библиотеки;</span><span class="sxs-lookup"><span data-stu-id="2faae-112">Provide a set of tutorials on the basics to start using the tools provided by the library.</span></span>
- <span data-ttu-id="2faae-113">рассмотрение методов обучения и проверки для таких классификаторов и того, как они переводятся в конкретные операции Q\#, предоставляемые библиотекой.</span><span class="sxs-lookup"><span data-stu-id="2faae-113">Discuss the training and validation methods for such classifiers and how they translate into specific Q\# operations provided by the library.</span></span>

<span data-ttu-id="2faae-114">Реализованная в этой библиотеке модель основана на схеме квантового и классического обучения, которая представлена в статье об [ориентированных на схему квантовых классификаторах](https://arxiv.org/abs/1804.00633).</span><span class="sxs-lookup"><span data-stu-id="2faae-114">The model implemented in this library is based on the quantum-classical training scheme presented in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span></span>
