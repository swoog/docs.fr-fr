---
title: Machine learning automatisé avec ML.NET
description: Vue d’ensemble de la sélection et de l’entraînement automatiques d’un modèle
author: natke
ms.date: 05/01/2019
ms.topic: overview
ms.custom: mvc
ms.author: nakersha
ms.openlocfilehash: e6654718f174c9d8b628b05d85d74952c222eb66
ms.sourcegitcommit: 4c10802ad003374641a2c2373b8a92e3c88babc8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2019
ms.locfileid: "65452734"
---
# <a name="automated-machine-learning-with-mlnet"></a>Machine learning automatisé avec ML.NET

Le machine learning automatisé est une fonctionnalité de ML.NET qui sélectionne et entraîne un modèle automatiquement. Vous spécifiez la tâche de machine learning et fournissez un jeu de données, après quoi le machine learning automatisé choisit pour vous le modèle présentant les meilleures métriques. Il génère :
- un fichier de modèle qui peut être chargé dans votre application de prédiction
- le code d’application nécessaire pour effectuer des prédictions
- le code source utilisé pour la sélection des caractéristiques et l’entraînement du modèle (pour comprendre le modèle)

> [!NOTE]
> Cette fonctionnalité étant en préversion, elle est susceptible d’être modifiée. 

Le ML automatisé est actuellement disponible uniquement pour les [tâches](resources/tasks.md) de machine learning de classification binaire, de classification multiclasse et de régression. Les autres tâches de machine learning seront prises en charge dans les versions ultérieures.

Il y a trois manières d’utiliser le ML automatisé :
1. À partir de la ligne de commande, avec l’interface [CLI ML.NET](automate-training-with-cli.md)
1. Par le biais d’une application, avec l’[API de ML automatisé](how-to-guides/how-to-use-the-automl-api.md)
1. Dans une interface graphique utilisateur, avec le Générateur de modèles ML.NET
