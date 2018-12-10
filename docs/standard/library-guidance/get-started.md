---
title: Bien démarrer la création de bibliothèques .NET de haute qualité
description: Bien démarrer la création de bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 05466de1469fc765570b8250301e8404cd5df173
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53145723"
---
# <a name="get-started"></a>Prise en main

## <a name="cross-platform-targetingcross-platform-targetingmd"></a>[Ciblage multiplateforme](./cross-platform-targeting.md)

Comment utiliser .NET Standard et le multi-ciblage pour créer des bibliothèques interplateformes. .NET s’exécute dans de nombreux endroits, et les bibliothèques .NET de bonne qualité doivent s’efforcer de prendre en charge autant de plateformes et de développeurs que possible.

## <a name="strong-namingstrong-namingmd"></a>[Affectation de noms forts](./strong-naming.md)

Découvrez l’affectation de noms forts, ses avantages et ses inconvénients. L’affectation d’un nom fort à une bibliothèque .NET permet à un maximum de développeurs de l’utiliser. En outre, c’est une pratique recommandée.

## <a name="nuget-and-open-source-librariesnugetmd"></a>[Bibliothèques open source et NuGet](./nuget.md)

La meilleure façon de créer des packages NuGet pour les bibliothèques .NET open source, notamment les métadonnées recommandées pour tous les packages publiés publiquement sur NuGet.org.

### <a name="dependenciesdependenciesmd"></a>[Dépendances](./dependencies.md)

NuGet facilite l’utilisation des packages existants lors de la création d’une bibliothèque .NET. Découvrez les sources courantes de friction entre les dépendances NuGet et comment les éviter.

### <a name="sourcelinksourcelinkmd"></a>[SourceLink](./sourcelink.md)

SourceLink est un excellent outil qui permet aux utilisateurs de votre bibliothèque .NET de parcourir son code source pendant le débogage. Cet article est une vue d’ensemble de SourceLink et des raisons pour lesquelles vous devriez l’utiliser.

### <a name="publishingpublish-nuget-packagemd"></a>[Publication](./publish-nuget-package.md)

Bien que NuGet.org soit le référentiel le plus largement connu et utilisé, il existe de nombreux endroits où publier des packages NuGet. Découvrez les différents référentiels de package NuGet disponibles et les meilleures pratiques de sécurité pour la publication d’une bibliothèque .NET.

## <a name="versioningversioningmd"></a>[Gestion des versions](./versioning.md)

Les bonnes bibliothèques .NET évoluent au fil du temps, avec l’ajout de fonctionnalités, la résolution de bogues et l’amélioration des performances dans les versions ultérieures. Découvrez les différents numéros de version et comment communiquer les modifications avec rupture aux développeurs.

### <a name="breaking-changesbreaking-changesmd"></a>[Modifications avec rupture](./breaking-changes.md)

Il est important pour une bibliothèque .NET de trouver un équilibre entre la stabilité pour les utilisateurs existants et l’innovation pour l’avenir. Découvrez les différents types de modifications avec rupture et de stratégies pour l’ajout de nouvelles fonctionnalités tout en conservant une compatibilité descendante.

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](cross-platform-targeting.md)