---
title: Choix entre .NET Core et .NET Framework pour les conteneurs Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Choix entre .NET Core et .NET Framework pour les conteneurs Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: 9abff2614e4022408a069be25440196111db19ab
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562107"
---
# <a name="choosing-between-net-core-and-net-framework-for-docker-containers"></a><span data-ttu-id="c62b5-103">Choix entre .NET Core et .NET Framework pour les conteneurs Docker</span><span class="sxs-lookup"><span data-stu-id="c62b5-103">Choosing Between .NET Core and .NET Framework for Docker Containers</span></span>

<span data-ttu-id="c62b5-104">Il existe deux frameworks pris en charge pour générer des applications Docker en conteneur côté serveur avec .NET : [.NET Framework et .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="c62b5-104">There are two supported frameworks for building server-side containerized Docker applications with .NET: [.NET Framework and .NET Core](https://www.microsoft.com/net/download).</span></span> <span data-ttu-id="c62b5-105">Ils partagent de nombreux composants de plateforme .NET et vous permettent de partager du code entre les deux.</span><span class="sxs-lookup"><span data-stu-id="c62b5-105">They share many .NET platform components, and you can share code across the two.</span></span> <span data-ttu-id="c62b5-106">Toutefois, il existe des différences fondamentales entre eux et votre choix dépend de ce que vous souhaitez accomplir.</span><span class="sxs-lookup"><span data-stu-id="c62b5-106">However, there are fundamental differences between them, and which framework you use will depend on what you want to accomplish.</span></span> <span data-ttu-id="c62b5-107">Cette section fournit des instructions pour éclairer le choix de chaque framework.</span><span class="sxs-lookup"><span data-stu-id="c62b5-107">This section provides guidance on when to choose each framework.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="c62b5-108">[Précédent](../container-docker-introduction/docker-containers-images-registries.md)
[Suivant](general-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="c62b5-108">[Previous](../container-docker-introduction/docker-containers-images-registries.md)
[Next](general-guidance.md)</span></span>
