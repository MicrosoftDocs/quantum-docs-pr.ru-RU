---
title: Загрузка классических данных
description: Узнайте, как загрузить собственный набор данных для обучения модели-классификатора с помощью Microsoft Quantum Development Kit (КДК).
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
ms.openlocfilehash: efa4a65a489446cbef48507d0b02a932da74c71c
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327668"
---
# <a name="load-and-classify-your-own-datasets"></a><span data-ttu-id="0d5e8-103">Загрузка и классификация собственных наборов данных</span><span class="sxs-lookup"><span data-stu-id="0d5e8-103">Load and classify your own datasets</span></span>

<span data-ttu-id="0d5e8-104">В этом кратком руководстве мы расскажу, как загрузить собственный набор данных для обучения модели классификатора с помощью пакета средств разработки такта (КДК).</span><span class="sxs-lookup"><span data-stu-id="0d5e8-104">In this short tutorial, we are going to learn how to load your own dataset to train a classifier model with the Quantum Development Kit (QDK).</span></span>

<span data-ttu-id="0d5e8-105">Мы настоятельно рекомендуем использовать стандартизированный формат сериализации, например [JSON-файлы](https://en.wikipedia.org/wiki/JSON) , для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-105">We highly recommend the use of a standardized serialization format such as [JSON files](https://en.wikipedia.org/wiki/JSON) to store your data.</span></span>
<span data-ttu-id="0d5e8-106">Такие форматы обеспечивают высокую совместимость с различными платформами, такими как Python и экосистема .NET.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-106">Such formats offer high compatibility with different frameworks like Python and the .NET ecosystem.</span></span>
<span data-ttu-id="0d5e8-107">В частности, мы рекомендуем использовать наш шаблон для загрузки данных, чтобы можно было копировать и вставлять код непосредственно из примеров.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-107">In particular, we recommend using our template for loading the data, so that you can copy-paste the code directly from the samples.</span></span>

## <a name="template-for-loading-your-datasets"></a><span data-ttu-id="0d5e8-108">Шаблон для загрузки наборов данных</span><span class="sxs-lookup"><span data-stu-id="0d5e8-108">Template for loading your datasets</span></span>

<span data-ttu-id="0d5e8-109">Предположим, что у нас есть набор обучающих данных $ (x, y) с размером $N = $2, где каждый экземпляр $x _i $ of $x $ имеет три функции: $x _ {I1} $, $x _ {I2} $ и $x _ {i3} $.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-109">Suppose we have a training dataset $(x, y)$ of size $N=2$ where each instance $x_i$ of $x$ has three features: $x_{i1}$, $x_{i2}$ and $x_{i3}$.</span></span>
<span data-ttu-id="0d5e8-110">Набор данных проверки имеет ту же структуру.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-110">The validation dataset has the same structure.</span></span>
<span data-ttu-id="0d5e8-111">Эти датсетс могут быть представлены `data.json` файлом примерно следующего вида:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-111">These datsets can be represented by a `data.json` file similar to the following:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a><span data-ttu-id="0d5e8-112">Пример с использованием шаблона</span><span class="sxs-lookup"><span data-stu-id="0d5e8-112">Example using the template</span></span>

<span data-ttu-id="0d5e8-113">Предположим, что у нас есть небольшой набор данных с высотой и весом различных кошки и собаки.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-113">Suppose we have a small dataset with the heights and weights of different cats and dogs.</span></span> <span data-ttu-id="0d5e8-114">Этот набор данных очень мал для обучения модели, но будет достаточно для отображения процесса загрузки набора данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-114">This dataset is very small to train a model but will be enough to show the process of loading a dataset.</span></span>

| <span data-ttu-id="0d5e8-115">Высота (m)</span><span class="sxs-lookup"><span data-stu-id="0d5e8-115">Height (m)</span></span> | <span data-ttu-id="0d5e8-116">Вес (кг)</span><span class="sxs-lookup"><span data-stu-id="0d5e8-116">Weight (kg)</span></span> | <span data-ttu-id="0d5e8-117">Животное</span><span class="sxs-lookup"><span data-stu-id="0d5e8-117">Animal</span></span> |
|-----------|------------|--------|
| <span data-ttu-id="0d5e8-118">0,54</span><span class="sxs-lookup"><span data-stu-id="0d5e8-118">0.54</span></span>      | <span data-ttu-id="0d5e8-119">30</span><span class="sxs-lookup"><span data-stu-id="0d5e8-119">30</span></span>         | <span data-ttu-id="0d5e8-120">Собака</span><span class="sxs-lookup"><span data-stu-id="0d5e8-120">Dog</span></span>    |
| <span data-ttu-id="0d5e8-121">0,30</span><span class="sxs-lookup"><span data-stu-id="0d5e8-121">0.30</span></span>      | <span data-ttu-id="0d5e8-122">8</span><span class="sxs-lookup"><span data-stu-id="0d5e8-122">8</span></span>          | <span data-ttu-id="0d5e8-123">Кот</span><span class="sxs-lookup"><span data-stu-id="0d5e8-123">Cat</span></span>    |
| <span data-ttu-id="0d5e8-124">0,91</span><span class="sxs-lookup"><span data-stu-id="0d5e8-124">0.91</span></span>      | <span data-ttu-id="0d5e8-125">44</span><span class="sxs-lookup"><span data-stu-id="0d5e8-125">44</span></span>         | <span data-ttu-id="0d5e8-126">Собака</span><span class="sxs-lookup"><span data-stu-id="0d5e8-126">Dog</span></span>    |
| <span data-ttu-id="0d5e8-127">0,86</span><span class="sxs-lookup"><span data-stu-id="0d5e8-127">0.86</span></span>      | <span data-ttu-id="0d5e8-128">31</span><span class="sxs-lookup"><span data-stu-id="0d5e8-128">31</span></span>          | <span data-ttu-id="0d5e8-129">Собака</span><span class="sxs-lookup"><span data-stu-id="0d5e8-129">Dog</span></span>    |
| <span data-ttu-id="0d5e8-130">0,32</span><span class="sxs-lookup"><span data-stu-id="0d5e8-130">0.32</span></span>      | <span data-ttu-id="0d5e8-131">5</span><span class="sxs-lookup"><span data-stu-id="0d5e8-131">5</span></span>         | <span data-ttu-id="0d5e8-132">Кот</span><span class="sxs-lookup"><span data-stu-id="0d5e8-132">Cat</span></span>    |
| <span data-ttu-id="0d5e8-133">0,25</span><span class="sxs-lookup"><span data-stu-id="0d5e8-133">0.25</span></span>      | <span data-ttu-id="0d5e8-134">4</span><span class="sxs-lookup"><span data-stu-id="0d5e8-134">4</span></span>          | <span data-ttu-id="0d5e8-135">Кот</span><span class="sxs-lookup"><span data-stu-id="0d5e8-135">Cat</span></span>    |

<span data-ttu-id="0d5e8-136">Процесс:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-136">The process is:</span></span>

- <span data-ttu-id="0d5e8-137">Сначала необходимо разделить набор данных на обучение и проверку.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-137">First we need to separate the dataset into training and validation.</span></span> <span data-ttu-id="0d5e8-138">В этом случае мы можем просто взять первые три примера для обучения и другие примеры для проверки.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-138">In this case we can just take the first three samples for training and the rest of samples for validation.</span></span> <span data-ttu-id="0d5e8-139">Как правило, рекомендуется случайным образом задать набор данных для обучения и проверки, чтобы избежать нежелательных смещений в обучающих данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-139">In general it is a good practice to sample randomly the training and validation dataset to avoid unwanted biases in the training data.</span></span>
- <span data-ttu-id="0d5e8-140">Во-вторых, нам нужно назначить числовую метку каждому классу.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-140">Secondly, we need to assign a numeric label to each class.</span></span> <span data-ttu-id="0d5e8-141">Обратите внимание, что в течение этого времени библиотека КМЛ расскажу только о проблемах с двоичной классификацией.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-141">Note that, for the moment, the QML library only admits binary classification problems.</span></span> <span data-ttu-id="0d5e8-142">Поэтому мы присваиваем метке 0 классу `Dog` и номеру 1 классу `Cat` .</span><span class="sxs-lookup"><span data-stu-id="0d5e8-142">So we will assign the label 0 to the class `Dog` and the number 1 to the class `Cat`.</span></span>
- <span data-ttu-id="0d5e8-143">Наконец, мы заполняем шаблон, используя данные из нашего набора данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-143">Finally, we fill the template using the data from our dataset.</span></span> <span data-ttu-id="0d5e8-144">Обратите внимание, что для больших наборов данных следует создать небольшой скрипт для автоматического создания шаблона из конкретного набора.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-144">Note that for big datasets you should build a small script to automatically generate the template from your specific dataset.</span></span> <span data-ttu-id="0d5e8-145">Этот сценарий будет зависеть от исходного формата набора данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-145">This script will depend on the original format of your dataset.</span></span>

<span data-ttu-id="0d5e8-146">Для нашего набора данных `data.json` файл имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-146">For our dataset the `data.json` file is:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a><span data-ttu-id="0d5e8-147">Загрузка данных</span><span class="sxs-lookup"><span data-stu-id="0d5e8-147">Loading the data</span></span>

<span data-ttu-id="0d5e8-148">После сериализации данных в виде JSON-файла его можно загрузить с помощью библиотек JSON, поставляемых с выбранным языком узла.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-148">Once you have your data serialized as a JSON file, you can load it in using JSON libraries provided with your host language of choice.</span></span>

### <a name="python"></a>[<span data-ttu-id="0d5e8-149">Python</span><span class="sxs-lookup"><span data-stu-id="0d5e8-149">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="0d5e8-150">Python предоставляет [встроенный `json` пакет](https://docs.python.org/3.7/library/json.html) для работы с сериализованными данными JSON:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-150">Python provides the [built-in `json` package](https://docs.python.org/3.7/library/json.html) for working with JSON-serialized data:</span></span>

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[<span data-ttu-id="0d5e8-151">C#</span><span class="sxs-lookup"><span data-stu-id="0d5e8-151">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="0d5e8-152">Платформа .NET Core предоставляет [ `System.Text.Json` пакет](https://www.nuget.org/packages/System.Text.Json) для работы с сериализованными данными JSON:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-152">The .NET Core platform provides the [`System.Text.Json` package](https://www.nuget.org/packages/System.Text.Json) for working with JSON-serialized data:</span></span>

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a><span data-ttu-id="0d5e8-153">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0d5e8-153">Next steps</span></span>

<span data-ttu-id="0d5e8-154">Теперь вы готовы приступить к выполнению собственных экспериментов с собственными наборами данных.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-154">Now you are ready to start running your own experiments with your own datasets.</span></span> <span data-ttu-id="0d5e8-155">Попробуйте использовать разные классификаторы и наборы данных и доучастие в сообществе, совместно использующих ваши результаты.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-155">Try different classifiers and dataset and contribute to the community sharing your results!</span></span>
