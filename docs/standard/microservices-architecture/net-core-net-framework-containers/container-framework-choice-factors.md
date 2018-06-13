---
title: 'Table de décision : versions de .NET Framework à utiliser pour Docker'
description: Architecture de microservices .NET pour les applications .NET en conteneur | Table de décision, versions de .NET Framework à utiliser pour Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.openlocfilehash: 0e384fabca88d8ad6f93ae626140fb3d5dcaf971
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33589320"
---
# <a name="decision-table-net-frameworks-to-use-for-docker"></a>Table de décision : versions de .NET Framework à utiliser pour Docker

Le récapitulatif ci-dessous vous indique s’il convient d’utiliser .NET Framework ou .NET Core, des conteneurs Windows ou des conteneurs Linux. N’oubliez pas que pour les conteneurs Linux, vous avez besoin d’hôtes Docker basés sur Linux (machines virtuelles ou serveurs) et que pour les conteneurs Windows, vous avez besoin d’hôtes Docker basés sur Windows Server (machines virtuelles ou serveurs).

Votre application contient plusieurs fonctionnalités qui vont peser dans votre décision. Vous devez évaluer l’importance de ces fonctionnalités au moment de prendre votre décision.

> [!IMPORTANT]
> Vos machines de développement exécuteront un hôte Docker, Linux ou Windows. Les microservices connexes que vous souhaitez exécuter et tester ensemble dans une solution devront tous s’exécuter sur la même plateforme de conteneur.

* Vous choisissez **Microservices dans conteneurs** comme architecture d’application.
    - Vous devez choisir *.NET Core* comme implémentation .NET.
    - Vous pouvez choisir *Conteneurs Linux* ou *Conteneurs Windows* comme plateforme de conteneur.
* Vous choisissez **Application monolithique** comme architecture d’application.
    - Vous pouvez choisir *.NET Core* ou *.NET Framework* comme implémentation .NET.
    - Si vous avez choisi *.NET Core*, vous pouvez choisir *Conteneurs Linux* ou *Conteneurs Windows* comme plateforme de conteneur.
    - Si vous avez choisi *.NET Framework*, vous devez choisir *Conteneurs Windows* comme plateforme de conteneur.
* Votre application correspond à un **Développement basé sur un nouveau conteneur (« green-field »)**.
    - Vous devez choisir *.NET Core* comme implémentation .NET.
    - Vous pouvez choisir *Conteneurs Linux* ou *Conteneurs Windows* comme plateforme de conteneur.
* Votre application correspond à une **Migration d’application existante Windows Server (« brown-field ») vers des conteneurs**
    - L’implémentation .NET que vous choisissez est *.NET Framework* compte tenu de la dépendance du framework.
    - Vous devez choisir *Conteneurs Windows* comme plateforme de conteneur du fait de la dépendance de .NET Framework.
* L’objectif de conception de votre application est **Performances et scalabilité optimales**.
    - Vous devez choisir *.NET Core* comme implémentation .NET.
    - Vous pouvez choisir *Conteneurs Linux* ou *Conteneurs Windows* comme plateforme de conteneur.
* Vous avez créé votre application en utilisant **ASP.NET Core**.
    - Vous devez choisir *.NET Core* comme implémentation .NET.
    - Vous pouvez utiliser l’implémentation *.NET Framework* si vous avez d’autres dépendances de framework.
    - Si vous avez choisi *.NET Core*, vous pouvez choisir *Conteneurs Linux* ou *Conteneurs Windows* comme plateforme de conteneur.
    - Si vous avez choisi *.NET Framework*, vous devez choisir *Conteneurs Windows* comme plateforme de conteneur.
* Vous avez créé votre application en utilisant **ASP.NET 4 (MVC 5, l’API Web 2 et Web Forms)**.
    - L’implémentation .NET que vous choisissez est *.NET Framework* compte tenu de la dépendance du framework.
    - Vous devez choisir *Conteneurs Windows* comme plateforme de conteneur du fait de la dépendance de .NET Framework.
* Votre application utilise les **services SignalR**.
    - Vous pouvez choisir *.NET Framework* ou *.NET Core version 2.1 (quand elle sera lancée) ou ultérieure*.
    - Vous devez choisir *Conteneurs Windows* comme plateforme de conteneur si vous avez choisi l’implémentation SignalR dans .NET Framework.
    - Vous pouvez choisir Conteneurs Linux ou Conteneurs Windows comme plateforme de conteneur si vous avez choisi l’implémentation SignalR dans .NET Core version 2.1 ou ultérieure (quand elle sera lancée).  
    - Quand les **services SignalR** s’exécutent sur *.NET Core*, vous pouvez utiliser des *conteneurs Linux ou des conteneurs Windows*.
* Votre application utilise **WCF, WF et d’autres frameworks existants**.
    - Choisissez *.NET Framework* ou *.NET Core (dans la feuille de route d’une future une version)* comme implémentation .NET.
    - Vous devez choisir *Conteneurs Windows* comme plateforme de conteneur du fait de la dépendance de .NET Framework.
* Votre application implique une **consommation de services Azure**.
    - Choisissez *.NET Framework* ou *.NET Core (tous les services Azure sont appelés à proposer un SDK client pour .NET Core)*.
    - Vous devez choisir *Conteneurs Windows* comme plateforme de conteneur si vous utilisez des API clientes .NET Framework.
    - Si vous utilisez les API clientes disponibles pour *.NET Core*, vous avez aussi le choix entre les *conteneurs Linux et les conteneurs Windows*.

>[!div class="step-by-step"]
[Précédent] (net-framework-container-scenarios.md) [Suivant] (net-container-os-targets.md)
