---
title: Principes de conception communs des conteneurs
description: Découvrez un principe fondamental de la conception de conteneur bon, c’est qu’un conteneur doit héberger qu’un seul processus.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 206963d63cf8e6ab4fc61b9176f1ba095868c6fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61969115"
---
# <a name="common-container-design-principles"></a>Principes de conception communs des conteneurs

À l’avance d’aborder le processus de développement, il existe quelques concepts de base intéressant de mentionner en ce qui concerne la façon dont vous utilisez des conteneurs.

## <a name="container-equals-a-process"></a>Conteneur est égal à un processus

Dans le modèle de conteneur, un conteneur représente un processus unique. En définissant un conteneur comme une limite de processus, commencer à créer les primitives utilisées pour la mise à l’échelle, ou désactivé par lots, les processus. Lorsque vous exécutez un conteneur Docker, vous verrez un [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) définition. Cela définit le processus et la durée de vie du conteneur. Lorsque le processus terminé, le cycle de vie de conteneur se termine. Il existe des processus longs, tels que les serveurs web et les processus de courte durée, telles que des traitements par lots, qui peuvent avoir été implémentés en tant que Microsoft Azure [WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/). Si le processus échoue, le conteneur prend fin et l’orchestrateur prend le contrôle. Si l’orchestrateur a été réglé pour conserver les cinq instances en cours d’exécution et un échoue, l’orchestrateur crée un autre conteneur pour remplacer le processus ayant échoué. Dans un programme de traitement par lots, le processus démarre avec des paramètres. Quand le processus prend fin, le travail est terminé.

Vous pouvez trouver un scénario dans lequel vous souhaitez plusieurs processus en cours d’exécution dans un seul conteneur. Dans n’importe quel document d’architecture, il n’est jamais un « jamais » ni aucune toujours une « toujours ». Pour les scénarios qui requièrent plusieurs processus, un modèle courant consiste à utiliser [superviseur](http://supervisord.org/).

>[!div class="step-by-step"]
>[Précédent](design-docker-applications.md)
>[Suivant](monolithic-applications.md)