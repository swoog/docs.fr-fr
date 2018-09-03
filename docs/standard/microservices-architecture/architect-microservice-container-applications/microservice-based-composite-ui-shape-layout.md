---
title: Création d’une interface utilisateur composite basée sur des microservices, notamment la forme et la disposition de l’interface utilisateur visuelle générées par plusieurs microservices
description: Architecture de microservices .NET pour les applications .NET en conteneur | Création d’une interface utilisateur composite basée sur des microservices, notamment la forme et la disposition de l’interface utilisateur visuelle générées par plusieurs microservices
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 79b63c376d25725b2bcb6c16cdb4d06e107d5c07
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43418638"
---
# <a name="creating-composite-ui-based-on-microservices-including-visual-ui-shape-and-layout-generated-by-multiple-microservices"></a>Création d’une interface utilisateur composite basée sur des microservices, notamment la forme et la disposition de l’interface utilisateur visuelle générées par plusieurs microservices

L’architecture de microservices commence généralement par la gestion des données et de la logique du côté serveur. Cependant, une approche plus avancée consiste à concevoir l’interface utilisateur de votre application également en fonction de microservices. Ceci implique d’avoir une interface utilisateur composite produite par les microservices, et non pas des microservices sur le serveur et simplement une application cliente monolithique consommant les microservices. Avec cette approche, les microservices que vous créez peuvent être complets, avec à la fois la logique et une représentation visuelle.

La figure 4-20 montre une approche plus simple consistant à seulement consommer des microservices à partir d’une application cliente monolithique. Bien sûr, vous pourriez avoir un service ASP.NET MVC intermédiaire produisant du code HTML et JavaScript. La figure est une simplification qui met en évidence le fait que vous avez une interface utilisateur cliente (monolithique) consommant les microservices, qui s’occupe seulement de la logique et des données, mais pas de la forme de l’interface utilisateur (HTML et JavaScript).

![](./media/image20.png)

**Figure 4-20**. Une application avec interface utilisateur monolithique consommant des microservices de backend

En revanche, une interface utilisateur composite est précisément générée et composée par les microservices eux-mêmes. Certains des microservices déterminent la forme visuelle de zones spécifiques de l’interface utilisateur. La principale différence est que vous avez des composants d’interface utilisateur clients (par exemple des classes TS) basées sur des modèles, et que le ViewModel de l’interface utilisateur qui met en forme les données pour ces modèles provient de chaque microservice.

Au démarrage de l’application cliente, chacun des composants de l’interface utilisateur cliente (par exemple des classes TypeScript) s’inscrit lui-même auprès d’un microservice de l’infrastructure capable de fournir des ViewModel pour un scénario donné. Si le microservice change la forme, l’interface utilisateur change également.

La figure 4-21 montre une version de cette approche de l’interface utilisateur composite. C’est une version simplifiée, car vous pouvez avoir d’autres microservices qui agrègent des parties plus petites selon différentes techniques : cela dépend de ce que vous créez, une approche web traditionnelle (ASP.NET MVC) ou une application monopage.

![](./media/image21.png)

**Figure 4-21**. Exemple d’une application d’interface utilisateur composite mise en forme des microservices de backend

Chacun de ces microservices de composition de l’interface utilisateur serait similaire à une petite passerelle d’API. Dans ce cas, chacun est cependant responsable d’une petite partie de l’interface utilisateur.

Une approche de l’interface utilisateur composite pilotée par des microservices peut être plus ou moins délicate, selon les technologies d’interface utilisateur que vous utilisez. Par exemple, vous n’utilisez pas les mêmes techniques pour créer une application web classique que pour créer une application monopage ou pour des applications mobiles natives (comme quand vous développez des applications Xamarin, ce qui peut s’avérer plus difficile pour cette approche).

L’exemple d’application [eShopOnContainers](https://aka.ms/MicroservicesArchitecture) utilise l’approche de l’interface utilisateur monolithique pour plusieurs raisons. D’abord, elle constitue une introduction aux microservices et aux conteneurs. Une interface utilisateur composite est plus avancée, mais engendre plus de complexité dans la conception et le développement de l’interface utilisateur. En second lieu, eShopOnContainers fournit également une application mobile native basée sur Xamarin, ce qui rendrait plus complexe le code C\# côté client.

Nous vous encourageons cependant à utiliser les références suivantes pour en savoir plus sur les interfaces utilisateur composites basées sur des microservices.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Composite UI using ASP.NET (Particular’s Workshop)**
    [*http://go.particular.net/workshop-composite-ui-demo*](http://go.particular.net/workshop-composite-ui-demo)

-   **Ruben Oostinga. The Monolithic Frontend in the Microservices Architecture**
    [*http://blog.xebia.com/the-monolithic-frontend-in-the-microservices-architecture/*](http://blog.xebia.com/the-monolithic-frontend-in-the-microservices-architecture/)

-   **Mauro Servienti. The secret of better UI composition**
    [*https://particular.net/blog/secret-of-better-ui-composition*](https://particular.net/blog/secret-of-better-ui-composition)

-   **Viktor Farcic. Including Front-End Web Components Into Microservices**
    [*https://technologyconversations.com/2015/08/09/including-front-end-web-components-into-microservices/*](https://technologyconversations.com/2015/08/09/including-front-end-web-components-into-microservices/)

-   **Managing Frontend in the Microservices Architecture**\
    [*https://allegro.tech/2016/03/Managing-Frontend-in-the-microservices-architecture.html*](https://allegro.tech/2016/03/Managing-Frontend-in-the-microservices-architecture.html)


>[!div class="step-by-step"]
[Précédent](microservices-addressability-service-registry.md)
[Suivant](resilient-high-availability-microservices.md)
