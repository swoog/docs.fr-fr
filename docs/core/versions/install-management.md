---
title: Gérer les installations de .NET Core
description: Découvrez comment gérer les multiples versions du SDK et du Runtime .NET Core installées sur votre machine par les stratégies d’installation côte à côte.
author: leecow
ms.author: wiwagn
ms.date: 08/22/2018
ms.openlocfilehash: 06c3f43e7917efb8fd31898044d8f5d920c2cada
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485442"
---
# <a name="manage-net-core-installations"></a>Gérer les installations de .NET Core

.NET Core prend en charge l’installation côte à côte de versions différentes du SDK et du Runtime, rendant ainsi la dépendance de version plus flexible pour créer et exécuter des applications .NET Core. Ces comportements d’installation et de restauration de version par progression automatique offrent des avantages indéniables, mais ils présentent un gros inconvénient. Après l’installation de nouvelles mises à jour du SDK ou du Runtime .NET Core, les versions antérieures restent installées sur le disque. La coexistence de multiples versions conduit à une surutilisation du disque au fil du temps. Plus de 50 mises à jour du SDK .NET Core ont été publiées. Votre système comporte peut-être beaucoup de versions du SDK et du Runtime qui ne sont plus utiles.

## <a name="safe-to-remove"></a>Pouvez-vous les supprimer sans risque ?

Compte tenu des comportements de [sélection de la version de .NET Core](selection.md) et de la compatibilité des Runtimes .NET Core entre les mises à jour, vous pouvez supprimer en toute sécurité les versions précédentes. Les mises à jour du Runtime .NET Core sont toutes compatibles au sein d’une même version principale (par exemple, 1.x et 2.x). De plus, avec les versions récentes du SDK .NET Core, vous pouvez généralement continuer à créer des applications qui ciblent des versions précédentes du Runtime de manière compatible.

En règle générale, vous avez uniquement besoin de la dernière version du SDK et de la dernière version des correctifs pour les Runtimes requis par votre application. Dans certains cas, vous devez conserver des versions antérieures du SDK ou du Runtime, par exemple, pour tenir à jour des applications basées sur project.json.  Si votre application ne nécessite pas de versions antérieures du SDK ou du Runtime pour une raison particulière, vous pouvez supprimer les versions antérieures en toute sécurité.

Les méthodes de suppression de .NET Core varient selon la plateforme utilisée, et elles diffèrent aussi légèrement entre les différentes versions de .NET Core. Pour plus d’informations sur la suppression des versions de .NET Core qui ne sont plus utiles, consultez [Guide pratique pour supprimer le SDK et le Runtime .NET Core](remove-runtime-sdk-versions.md) dans la [documentation .NET Core](../index.md).
