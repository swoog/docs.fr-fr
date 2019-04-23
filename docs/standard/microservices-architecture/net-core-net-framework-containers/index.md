---
title: Choix entre .NET Core et .NET Framework pour les conteneurs Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Choix entre .NET Core et .NET Framework pour les conteneurs Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: e71739b06275d4ee786d246004930d7b66fbc72b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62019605"
---
# <a name="choosing-between-net-core-and-net-framework-for-docker-containers"></a><span data-ttu-id="604b6-103">Choix entre .NET Core et .NET Framework pour les conteneurs Docker</span><span class="sxs-lookup"><span data-stu-id="604b6-103">Choosing Between .NET Core and .NET Framework for Docker Containers</span></span>

<span data-ttu-id="604b6-104">Il existe deux frameworks pris en charge pour générer des applications Docker en conteneur côté serveur avec .NET : [.NET Framework et .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="604b6-104">There are two supported frameworks for building server-side containerized Docker applications with .NET: [.NET Framework and .NET Core](https://www.microsoft.com/net/download).</span></span> <span data-ttu-id="604b6-105">Ils partagent de nombreux composants de plateforme .NET et vous permettent de partager du code entre les deux.</span><span class="sxs-lookup"><span data-stu-id="604b6-105">They share many .NET platform components, and you can share code across the two.</span></span> <span data-ttu-id="604b6-106">Toutefois, il existe des différences fondamentales entre eux et votre choix dépend de ce que vous souhaitez accomplir.</span><span class="sxs-lookup"><span data-stu-id="604b6-106">However, there are fundamental differences between them, and which framework you use will depend on what you want to accomplish.</span></span> <span data-ttu-id="604b6-107">Cette section fournit des instructions pour éclairer le choix de chaque framework.</span><span class="sxs-lookup"><span data-stu-id="604b6-107">This section provides guidance on when to choose each framework.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="604b6-108">[Précédent](../container-docker-introduction/docker-containers-images-registries.md)
>[Suivant](general-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="604b6-108">[Previous](../container-docker-introduction/docker-containers-images-registries.md)
[Next](general-guidance.md)</span></span>