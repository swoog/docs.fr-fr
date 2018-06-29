---
title: Principes de conception communs conteneur
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: d3ae0c05a7e94d739a3442ecdb11564a70567963
ms.sourcegitcommit: 9e18e4a18284ae9e54c515e30d019c0bbff9cd37
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37071173"
---
# <a name="common-container-design-principles"></a>Principes de conception communs conteneur

Avance de mise en route dans le processus de développement, il existe quelques concepts de base intéressant de mentionner en ce qui concerne la façon dont vous utilisez des conteneurs.

## <a name="container-equals-a-process"></a>Conteneur est égal à un processus

Dans le modèle de conteneur, un conteneur représente un processus unique. En définissant un conteneur comme une limite de processus, commencer à créer les primitives utilisées pour la montée en puissance, ou désactivé par lots, les processus. Lorsque vous exécutez un conteneur Docker, vous verrez un [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) définition. Définit le processus et la durée de vie du conteneur. Lorsque le processus terminé, le cycle de vie de conteneur se termine. Les processus longs, tels que les serveurs web et les processus de courte durée de vie, tels que les traitements par lots, ce qui peuvent avoir été implémentés en tant que Microsoft Azure sont [WebJobs](https://azure.microsoft.com/en-us/documentation/articles/websites-webjobs-resources/). Si le processus échoue, le conteneur prend fin et l’orchestrateur prend le contrôle. Si l’orchestrateur a été invité à conserver les cinq instances en cours d’exécution et une échoue, l’orchestrateur créera un autre conteneur pour remplacer l’échec du processus. Dans un programme de traitement par lots, le processus démarre avec des paramètres. Quand le processus prend fin, le travail est terminé.

Vous constaterez peut-être un scénario dans lequel vous souhaitez plusieurs processus en cours d’exécution dans un seul conteneur. Dans n’importe quel document architecture, il n’est jamais un « jamais » ni toujours un « toujours ». Pour les scénarios qui requièrent plusieurs processus, il est courant d’utiliser [superviseur](http://supervisord.org/).


>[!div class="step-by-step"]
[Précédent](design-docker-applications.md)
[Suivant](monolithic-applications.md)
