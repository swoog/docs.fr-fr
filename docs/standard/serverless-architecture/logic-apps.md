---
title: Azure Logic Apps - applications sans serveur
description: Azure Logic Apps permettent de créer des workflows évolutifs automatisés intégrant les applications et des données sur cloud services et systèmes locaux.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 14670a8459db3b80b8fbe3139c2675321cf9592c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147945"
---
# <a name="azure-logic-apps"></a>Azure Logic Apps

[Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps) fournit un moteur sans serveur pour créer des workflows automatisés pour intégrer des données entre les services cloud et les applications et systèmes locaux. Vous générez des flux de travail à l’aide d’un concepteur visuel. Vous pouvez déclencher des workflows basés sur les événements ou les minuteurs et tirez parti des connecteurs pour l’intégration des applications et faciliter la communication de business-to-business (B2B). Logic Apps s’intègre en toute transparence avec Azure Functions.

![Logo de Azure Logic Apps](./media/logic-apps-logo.png)

Logic Apps peut faire plus que simplement connecter vos services de cloud (par exemple, des fonctions) avec des ressources de cloud (telles que les files d’attente et les bases de données). Vous pouvez également organiser les flux de travail en local avec la passerelle locale. Par exemple, vous pouvez utiliser l’application logique à déclencher une procédure stockée SQL de local en réponse à un événement basé sur le cloud ou une logique conditionnelle dans votre flux de travail. En savoir plus sur [connexion aux sources de données sur site avec la passerelle de données Azure local](https://docs.microsoft.com/azure/analysis-services/analysis-services-gateway).

![Architecture d’applications logique](./media/logic-apps-architecture.png)

Comme Azure Functions, vous lancez les workflows d’application logique avec un déclencheur. Il existe plusieurs déclencheurs pour vous permet de choisir à partir de. La capture suivante montre quelques-unes des plus populaires celles de centaines qui sont disponibles.

![Déclencheurs d’applications logique](./media/logic-app-triggers.png)

Une fois que l’application est déclenchée, vous pouvez utiliser le concepteur visuel pour créer des étapes, les boucles, les conditions et les actions. Des données ingérées à l’étape précédente sont disponibles que vous pouvez utiliser dans les étapes suivantes. Le workflow suivant charge les URL à partir d’une base de données CosmosDB. Il détecte les applications avec un hôte de `t.co` puis les recherche sur Twitter. S’il trouve des tweets correspondants, il met à jour les documents avec les tweets associés en appelant une fonction.

![Workflow d’application logique](./media/logic-app-workflow.png)

Le tableau de bord des applications logiques affiche l’historique de l’exécution de vos flux de travail et si chaque exécution terminée avec succès ou non. Vous pouvez naviguer dans une exécution donnée et inspecter les données utilisées par chaque étape pour le dépannage. Logic Apps fournit également des modèles existants, vous pouvez modifier et sont bien adaptés pour les workflows d’entreprise complexes.

Pour plus d’informations, consultez [Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps).

>[!div class="step-by-step"]
>[Précédent](application-insights.md)
>[Suivant](event-grid.md)