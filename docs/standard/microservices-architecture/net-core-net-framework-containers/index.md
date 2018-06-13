---
title: Choix entre .NET Core et .NET Framework pour les conteneurs Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Choix entre .NET Core et .NET Framework pour les conteneurs Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: b483214e7bd039a71ae642aa26e69d63222af8ab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33580125"
---
# <a name="choosing-between-net-core-and-net-framework-for-docker-containers"></a><span data-ttu-id="05d58-103">Choix entre .NET Core et .NET Framework pour les conteneurs Docker</span><span class="sxs-lookup"><span data-stu-id="05d58-103">Choosing Between .NET Core and .NET Framework for Docker Containers</span></span>

<span data-ttu-id="05d58-104">Il existe deux implémentations prises en charge pour générer des applications Docker en conteneur côté serveur avec .NET : [.NET Framework](https://www.microsoft.com/net/download/framework) et [.NET Core](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="05d58-104">There are two supported implementations for building server-side containerized Docker applications with .NET: [.NET Framework](https://www.microsoft.com/net/download/framework) and [.NET Core](https://www.microsoft.com/net/download/core).</span></span> <span data-ttu-id="05d58-105">Elles partagent de nombreux composants .NET Standard et vous permettent de partager du code entre les deux.</span><span class="sxs-lookup"><span data-stu-id="05d58-105">They share many .NET Standard components, and you can share code across the two.</span></span> <span data-ttu-id="05d58-106">Toutefois, il existe des différences fondamentales entre elles et votre choix dépend de ce que vous souhaitez accomplir.</span><span class="sxs-lookup"><span data-stu-id="05d58-106">However, there are fundamental differences between them, and which implementation you use will depend on what you want to accomplish.</span></span> <span data-ttu-id="05d58-107">Cette section fournit des instructions pour éclairer le choix de chaque implémentation.</span><span class="sxs-lookup"><span data-stu-id="05d58-107">This section provides guidance on when to choose each implementation.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="05d58-108">[Précédent] (../container-docker-introduction/docker-containers-images-registries.md) [Suivant] (general-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="05d58-108">[Previous] (../container-docker-introduction/docker-containers-images-registries.md) [Next] (general-guidance.md)</span></span>
