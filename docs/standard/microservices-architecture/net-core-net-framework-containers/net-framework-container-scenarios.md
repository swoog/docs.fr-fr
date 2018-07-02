---
title: Quand choisir .NET Framework pour les conteneurs Docker
description: Architecture de microservices .NET pour les applications .NET en conteneur | Quand choisir .NET Framework pour les conteneurs Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/07/2018
ms.openlocfilehash: 06b67f702b38202f598745826fa48f1ca97b7282
ms.sourcegitcommit: 6c480773ae896f45af4671fb3e26611a50e4dd81
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2018
ms.locfileid: "35251033"
---
# <a name="when-to-choose-net-framework-for-docker-containers"></a>Quand choisir .NET Framework pour les conteneurs Docker

Si .NET Core offre des avantages significatifs pour les nouvelles applications et les modèles d’application, le .NET Framework reste un bon choix pour de nombreux scénarios existants.

## <a name="migrating-existing-applications-directly-to-a-windows-server-container"></a>Migration d’applications existant directement dans un conteneur Windows Server

Vous pouvez utiliser des conteneurs Docker uniquement pour simplifier le déploiement, même si vous ne créez pas de microservices. Par exemple, vous souhaitez peut-être améliorer votre flux de travail DevOps avec Docker (les conteneurs peuvent vous offrir des environnements de test mieux isolés et même éliminer les problèmes de déploiement liés à des dépendances manquantes au moment de passer à un environnement de production). En pareil cas, même si vous déployez une application monolithique, il est judicieux d’utiliser des conteneurs Docker et Windows pour vos applications .NET Framework actuelles.

Dans la plupart des cas, pour ce scénario, vous n’aurez pas besoin de migrer vos applications existantes vers .NET Core ; vous pouvez utiliser des conteneurs Docker qui incluent le .NET Framework classique. En revanche, il est recommandé d’utiliser .NET Core quand il s’agit d’étendre une application existante, notamment en écrivant un nouveau service dans ASP.NET Core.

## <a name="using-third-party-net-libraries-or-nuget-packages-not-available-for-net-core"></a>Utilisation de bibliothèques .NET ou de packages NuGet tiers non disponibles pour .NET Core

Les bibliothèques tierces adoptent rapidement [.NET Standard](../../net-standard.md), ce qui permet de partager du code entre toutes les versions de .NET, notamment .NET Core. Avec la bibliothèque .NET Standard version 2.0 et au-delà, la compatibilité de la surface d’API entre les différents frameworks s’est considérablement élargie et dans.NET Core 2.x, les applications peuvent aussi faire directement référence aux bibliothèques .NET Framework existantes (consultez [compat shim](https://github.com/dotnet/standard/blob/master/docs/faq.md#how-does-net-standard-versioning-work)).

Cependant, malgré cette progression exceptionnelle depuis .NET Standard 2.0 et .NET Core 2.0, certains packages NuGet peuvent avoir besoin que Windows s’exécute et peuvent ne pas prendre en charge .NET Core. Si ces packages sont indispensables à votre application, vous devez utiliser le .NET Framework dans des conteneurs Windows.

## <a name="using-net-technologies-not-available-for-net-core"></a>Utilisation de technologies .NET non disponibles pour .NET Core 

Certaines technologies du .NET Framework ne sont pas disponibles dans la version actuelle de .NET Core (version 2.1 au moment de la rédaction de cet article). Certaines d’entre elles seront disponibles dans les prochaines versions de .NET Core (.NET Core 2.x), tandis que d’autres, qui ne s’appliquent pas aux nouveaux modèles d’application ciblés par .NET Core, risquent de ne jamais l’être.

La liste suivante recense la plupart des technologies qui ne sont pas disponibles dans .NET Core 2.1 :

-   Web Forms ASP.NET : cette technologie est disponible uniquement sur le .NET Framework. Il n’est pas prévu d’intégrer Web Forms ASP.NET à .NET Core.

-   Services WCF : même quand une [bibliothèque de client WCF](https://github.com/dotnet/wcf) est disponible pour consommer des services WCF à partir de .NET Core. Depuis la mi-année 2017, l’implémentation du serveur WCF est disponible uniquement sur le .NET Framework. Ce scénario peut être envisagé pour les futures versions de .NET Core.

-   Services liés aux flux de travail : Windows Workflow Foundation (WF), les services de flux de travail (WCF + WF dans un seul service) et WCF Data Services (anciennement ADO.NET Data Services) sont disponibles uniquement sur le .NET Framework. Il n’est actuellement pas prévu de les intégrer à .NET Core.

En plus des technologies listées dans la [feuille de route .NET Core](https://github.com/aspnet/Home/wiki/Roadmap) officielle, d’autres fonctionnalités pourraient être portées vers .NET Core. Pour obtenir la liste complète, examinez les éléments associés à la balise [port-to-core](https://github.com/dotnet/corefx/issues?q=is%3Aopen+is%3Aissue+label%3Aport-to-core) sur le site GitHub CoreFX. Notez que cette liste ne constitue pas un engagement de la part de Microsoft à intégrer ces composants à .NET Core ; il s’agit simplement des demandes formulées par la communauté. Si vous vous intéressez à l’un des composants listés ci-dessus, participez éventuellement aux discussions sur GitHub pour faire entendre votre voix. Et si vous pensez que quelque chose fait défaut, veuillez [enregistrer un nouveau problème dans le dépôt CoreFX](https://github.com/dotnet/corefx/issues/new).

## <a name="using-a-platform-or-api-that-does-not-support-net-core"></a>Utilisation d’une plateforme ou d’une API qui ne prend pas en charge .NET Core

Certaines plateformes Microsoft ou tierces ne prennent pas en charge .NET Core. Par exemple, certains services Azure proposent un kit SDK qui n’est pas encore utilisable sur .NET Core. Il s’agit d’une situation temporaire, car tous les services Azure sont appelés à utiliser .NET Core. Par exemple, le [SDK Azure DocumentDB pour .NET Core](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB.Core/1.2.1) a été publié en préversion le 16 novembre 2016, mais il est maintenant en disponibilité générale (GA) sous forme de version stable.

En attendant, si une plateforme ou un service Azure ne prend toujours pas en charge .NET Core avec son API cliente, vous pouvez utiliser l’API REST équivalente du service Azure ou le SDK client de .NET Framework.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Guide .NET Core**
    [*https://docs.microsoft.com/dotnet/core/index*](../../../core/index.md)

-   **Portage vers .NET Core à partir du .NET Framework**
    [*https://docs.microsoft.com/dotnet/core/porting/index*](../../../core/porting/index.md)

-   **Guide du .NET Framework sur Docker**
    [*https://docs.microsoft.com/dotnet/framework/docker/*](../../../framework/docker/index.md)

-   **Vue d’ensemble des composants .NET**
    [*https://docs.microsoft.com/dotnet/standard/components*](../../components.md)




>[!div class="step-by-step"]
[Précédent] (net-core-container-scenarios.md) [Suivant] (container-framework-choice-factors.md)
