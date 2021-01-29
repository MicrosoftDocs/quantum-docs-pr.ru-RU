---
title: Разработка на Q# и Binder
description: Узнайте, как создавать приложения Q# с помощью Binder.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: quickstart
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f7e9b1ae67d6275ec7ba39ea411842dc537536c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856708"
---
# <a name="develop-with-no-locq-and-binder"></a><span data-ttu-id="e7907-103">Разработка на Q# и Binder</span><span class="sxs-lookup"><span data-stu-id="e7907-103">Develop with Q# and Binder</span></span>

<span data-ttu-id="e7907-104">Вы можете использовать Binder для запуска своих записных книжек Jupyter Notebook и предоставления к ним общего доступа по сети.</span><span class="sxs-lookup"><span data-stu-id="e7907-104">You can use Binder to run and share your Jupyter Notebooks online.</span></span>

## <a name="use-binder-with-the-microsoft-qdk-samples"></a><span data-ttu-id="e7907-105">Использование Binder с примерами Microsoft QDK</span><span class="sxs-lookup"><span data-stu-id="e7907-105">Use Binder with the Microsoft QDK samples</span></span>

<span data-ttu-id="e7907-106">Чтобы настроить Binder автоматически на использование примеров Microsoft QDK, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e7907-106">To configure Binder automatically to use the Microsoft QDK samples:</span></span>

1. <span data-ttu-id="e7907-107">Откройте браузер и перейдите на страницу https://aka.ms/try-qsharp.</span><span class="sxs-lookup"><span data-stu-id="e7907-107">Open a browser and run https://aka.ms/try-qsharp.</span></span>
1. <span data-ttu-id="e7907-108">На целевой странице **Quantum Development Kit Samples** (Примеры пакета средств разработки Quantum) щелкните **Q# notebook** (Записная книжка Q#), чтобы узнать больше об использовании IQ# для написания собственных записных книжек квантовых приложений.</span><span class="sxs-lookup"><span data-stu-id="e7907-108">On the **Quantum Development Kit Samples** landing page, click **Q# notebook** to learn how to use IQ# to write your own quantum application notebooks.</span></span>

![Целевая страница QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a><span data-ttu-id="e7907-110">Использование Binder с записными книжками и репозиторием</span><span class="sxs-lookup"><span data-stu-id="e7907-110">Use Binder with your own notebooks and repository</span></span>

<span data-ttu-id="e7907-111">Если у вас уже есть записные книжки в репозитории GitHub, вы можете настроить Binder для работы с ним:</span><span class="sxs-lookup"><span data-stu-id="e7907-111">If you already have notebooks in a GitHub repository, you can configure Binder to work with your repo:</span></span>

1. <span data-ttu-id="e7907-112">Убедитесь, что в корневом каталоге вашего репозитория присутствует файл с именем *Dockerfile*.</span><span class="sxs-lookup"><span data-stu-id="e7907-112">Ensure that there is a file named *Dockerfile* in the root of your repository.</span></span> <span data-ttu-id="e7907-113">Файл должен содержать по меньшей мере следующие строки:</span><span class="sxs-lookup"><span data-stu-id="e7907-113">The file must contain at least the following lines:</span></span>

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > <span data-ttu-id="e7907-114">Вы можете проверить самую актуальную версию IQ# в [заметках о выпуске](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="e7907-114">You can verify the most current version of IQ# in the [Release Notes](xref:microsoft.quantum.relnotes).</span></span>

    <span data-ttu-id="e7907-115">Дополнительные сведения о создании файла Dockerfile см. в [справке по Dockerfile](https://docs.docker.com/engine/reference/builder/).</span><span class="sxs-lookup"><span data-stu-id="e7907-115">For more information about creating a Dockerfile, see the [Dockerfile reference](https://docs.docker.com/engine/reference/builder/).</span></span>

2. <span data-ttu-id="e7907-116">Откройте браузер и перейдите на страницу [mybinder.org](https://mybinder.org).</span><span class="sxs-lookup"><span data-stu-id="e7907-116">Open a browser to [mybinder.org](https://mybinder.org).</span></span>
3. <span data-ttu-id="e7907-117">Введите имя репозитория в виде **URL-адреса GitHub** (например, *мое_имя/мой_репозиторий*), и щелкните **launch** (Выполнить).</span><span class="sxs-lookup"><span data-stu-id="e7907-117">Enter your repository name as the **GitHub URL** (for example *MyName/MyRepo*), and click **launch**.</span></span>

![Форма MyBinder](~/media/mybinder.png)
    
## <a name="next-steps"></a><span data-ttu-id="e7907-119">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e7907-119">Next steps</span></span>

<span data-ttu-id="e7907-120">Теперь, когда вы настроили свою среду Binder, вы можете написать и выполнить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="e7907-120">Now that you have set up your Binder environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
