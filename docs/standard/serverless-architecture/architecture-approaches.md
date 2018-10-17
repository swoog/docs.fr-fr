---
title: Approches d’architecture - applications sans serveur
description: Introduction à l’architecture approches pour créer des applications d’entreprise basée sur le cloud, à partir des architectures multicouches pour sans serveur.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 21e191f17e7d0b4f2d64454fb14c46a4831a8375
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "49370019"
---
# <a name="architecture-approaches"></a>Approches de l’architecture

Présentation des approches existantes à l’architecture des applications d’entreprise vous aide à clarifier le rôle joué par sans serveur. Il existe plusieurs approches et modèles évolué au fil des décennies de développement logiciel et que tous ont leurs propres avantages et inconvénients. Dans de nombreux cas, la solution ultime pas, vous devrez choisir une approche unique, mais peut intégrer plusieurs approches. Scénarios de migration impliquent souvent un décalage à partir de l’approche d’une architecture à un autre via une approche hybride.

Ce chapitre fournit une vue d’ensemble de ces deux modèles d’architecture logique et physique pour les applications d’entreprise.

## <a name="architecture-patterns"></a>Modèles d’architecture

Les applications métier modernes suivent une variété de modèles d’architecture. Cette section représente une enquête des modèles courants. Les modèles répertoriés ici ne sont pas nécessairement toutes les meilleures pratiques, mais illustrent différentes approches.

Pour plus d’informations, consultez [guide d’architecture Azure application](https://docs.microsoft.com/azure/architecture/guide/).

## <a name="monoliths"></a>Monolithes

De nombreuses applications métier suivent un modèle de MONOLITHE. Les applications héritées sont souvent implémentées comme des monolithes. Dans le modèle d’application monolithique, tous les problèmes d’application sont contenus dans un déploiement unique. Tous les éléments à partir de l’interface utilisateur pour les appels de base de données sont inclus dans la même base de code.

![Architecture de l’application monolithique](./media/monolith-architecture.png)

Il existe plusieurs avantages à l’approche monolithique. Il est souvent facile extraire une seule base de code et commencer à travailler. Temps d’accélération peut être inférieur et création d’environnements de test est aussi simple que de fournir une nouvelle copie. Au modèle monolithique peut être conçu pour inclure plusieurs composants et applications.

Malheureusement, le modèle MONOLITHE tend à décomposer à grande échelle. Principaux inconvénients de l’approche monolithique :

* Il est difficile de travailler en parallèle dans le même code base.
* Toute modification, quelle que soit la façon dont trivial, requiert le déploiement d’une nouvelle version de l’application entière.
* Refactorisation potentiellement a un impact sur l’application entière.
* Souvent la seule solution à l’échelle consiste à créer plusieurs copies gourmandes en ressources du modèle monolithique.
* Développez des systèmes ou d’autres systèmes sont acquis, intégration peut être difficile.
* Il peut être difficile à tester en raison de la nécessité de configurer le MONOLITHE entière.
* Il est difficile de réutilisation du code et autres applications finissent souvent leurs propres copies de code.

De nombreuses entreprises rechercher vers le cloud comme une opportunité de migration d’applications de MONOLITHE et en même temps les refactoriser à davantage de modèles utilisables. Il est courant de séparer les applications individuelles et les composants pour leur permettre d’être conservées, déployés et mis à l’échelle séparément.

## <a name="n-layer-applications"></a>Applications de couche N

Logique d’application partition N couches application en couches spécifiques. Les couches plus courantes sont les suivantes :

* Interface utilisateur
* logique métier
* Accès aux données

Autres couches peuvent inclure intergiciel (middleware), traitement par lots et API. Il est important de noter que les couches sont logiques. Même si elles sont développées de manière isolée, ils peuvent tous être déployés à la même plateforme cible.

![Architecture de couche N](./media/n-layer-architecture.png)

Il existe plusieurs avantages à l’approche à N couches, y compris :

* La refactorisation est isolée sur une couche.
* Indépendamment, équipes peuvent créer, tester, déployer et maintenir des couches distinctes.
* Couches peuvent être échangées, par exemple la couche données peut accéder à plusieurs bases de données sans nécessiter de modifications de la couche d’interface utilisateur.

Sans serveur peut servir à implémenter une ou plusieurs couches.

## <a name="microservices"></a>Microservices

**[Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)**  architectures contiennent des caractéristiques communes qui incluent :

* Les applications sont composées de plusieurs petits services.
* Chaque service s’exécute dans son propre processus.
* Les services sont alignées autour des domaines d’activité.
* Services communiquent via des API légères, généralement à l’aide de HTTP comme transport.
* Services peuvent être déployés et mis à niveau indépendamment.
* Services ne sont pas dépendants sur un seul magasin de données.
* Le système est conçu par un échec à l’esprit, et l’application peut toujours s’exécuter même si certains services échouent.

Microservices n’êtes pas obligé d’être mutuellement exclusifs aux autres approches d’architecture. Par exemple, une architecture multiniveau peut utiliser des microservices pour la couche intermédiaire. Il est également possible d’implémenter des microservices de plusieurs façons, à partir de répertoires virtuels sur les hôtes IIS aux conteneurs. Caractéristiques des microservices idéales en particulier pour les implémentations sans serveur.

![Architecture en microservices](./media/microservices-architecture.png)

Les professionnels des architectures de microservices sont les suivantes :

* Il est souvent isolée sur un seul service de refactorisation.
* Les services peuvent être mis à niveau indépendamment les uns des autres.
* La résilience et l’élasticité peuvent être paramétrés pour les demandes de services individuels.
* Développement peut se produire en parallèle sur différentes plateformes et des équipes disparates.
* Il est plus facile d’écrire des tests complets pour les services isolés.

Microservices sont fournis avec leurs propres problèmes, notamment :

* Déterminer quels services sont disponibles et comment les appeler.
* La gestion du cycle de vie des services.
* Comprendre comment les services s’assemblent dans l’application globale.
* Complète du système de test d’appels effectués entre des services disparates.

En fin de compte il existe des solutions pour répondre à tous ces défis, y compris qui exploite les avantages de sans serveur qui sont décrits plus loin.

>[!div class="step-by-step"]
[Précédent](index.md)
[Suivant](architecture-deployment-approaches.md)
