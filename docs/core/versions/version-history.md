---
title: Historique des versions de .NET Core
description: Consultez la chronologie des versions du runtime .NET Core, du kit SDK .NET Core, du compilateur C# et du compilateur VB.NET.
ms.date: 07/26/2018
ms.openlocfilehash: 90fd4ba57620a3a005f2148c0335a76a6fa54a30
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519063"
---
# <a name="net-core-version-history"></a>Historique des versions de .NET Core

Les numéros de version de .NET Core sont complexes, car les versions du kit SDK .NET Core et du runtime .NET Core ne sont pas publiées à la même cadence. Cela signifie que l’équipe a été contrainte d’effectuer seulement deux des trois actions suivantes :

1. Publier de manière indépendante, en particulier permettre aux outils, à C# et à VB d’avancer plus rapidement que le runtime .NET Core
2. Conserver l’alignement des numéros de version entre le kit SDK .NET Core et le runtime .NET Core
3. Utiliser la gestion sémantique de version pour le kit SDK .NET Core et le runtime .NET Core

La version 2.0.0 a forcé l’alignement de version et s’est poursuivie sans heurts pour une mise en production. En décembre 2017, une publication de fonctionnalités a été ajoutée dans le kit SDK .NET Core, sans aucune publication correspondante dans le runtime .NET Core. L’équipe a choisi les objectifs 1 et 3, perdant ainsi l’alignement entre le SDK et le runtime .NET Core. Plusieurs versions du kit SDK .NET Core 2.1.x ont été publiées avant le runtime .NET Core 2.1. Le SDK ne bénéficiant pas de compatibilité ascendante, ces versions du SDK 2.1.x ne peuvent pas cibler le runtime .NET Core 2.1. L’équipe a répondu à la grande confusion en passant aux objectifs 1 et 2, abandonnant la gestion sémantique de version comme décrit dans [Gestion des versions de .NET Core](index.md#versioning-details).

Avant que la décision d’abandonner la gestion sémantique de version ne soit prise, des versions transitoires ont été publiées dans les plages de numéros de version 2.1.10x et 2.1.20x qui ne peuvent pas non plus cibler le runtime .NET Core 2.1.

Les deux premiers chiffres des numéros de version permettent un réalignement avec la version 2.1.0 du runtime .NET Core et la version 2.1.300 du kit SDK .NET Core.

Vous trouverez des informations détaillées sur les versions des différents composants, notamment les versions du compilateur de langage et du framework, dans la [page de téléchargements de .NET Core](https://www.microsoft.com/net/download/dotnet-core/current). Pour plus d’informations sur les versions antérieures, sélectionnez la version demandée dans la [page d’archives de téléchargements de .NET Core](https://www.microsoft.com/net/download/archives). Vous trouverez des informations de support détaillées dans l’article décrivant la [stratégie officielle de support de .NET](https://www.microsoft.com/net/Support/Policy).