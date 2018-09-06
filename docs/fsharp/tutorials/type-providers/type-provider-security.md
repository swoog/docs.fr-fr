---
title: Sécurité du fournisseur de type
description: 'En savoir plus sur la sécurité de fournisseur de type en F #, notamment comment modifier les paramètres d’approbation pour un fournisseur de type.'
ms.date: 05/16/2016
ms.openlocfilehash: 26f95ad3950b37a668c497f293b9941ed13a18c7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861905"
---
# <a name="type-provider-security"></a>Sécurité du fournisseur de type

Fournisseurs de type sont des assemblys (DLL) référencés par votre projet F # ou un script qui contiennent du code pour se connecter aux sources de données externes et de faire apparaître ces informations de type à l’environnement de type F #. En règle générale, le code dans les assemblys référencés s’exécute seulement lorsque vous compilez et puis exécutez le code (ou dans le cas d’un script, envoyez le code à F # Interactive). Toutefois, un assembly de fournisseur de type sera exécuté à l’intérieur de Visual Studio lorsque le code est simplement naviguer dans l’éditeur. Cela se produit, car les fournisseurs de type doivent exécuter pour ajouter des informations supplémentaires à l’éditeur, telles que des info-bulles Info express, les saisies semi-automatiques IntelliSense et ainsi de suite. Par conséquent, il existe des considérations de sécurité supplémentaire pour le type des assemblys de fournisseur, car ils s’exécutent automatiquement à l’intérieur du processus Visual Studio.

## <a name="security-warning-dialog"></a>Boîte de dialogue sécurité

Lorsque vous utilisez un assembly de fournisseur de type particulier pour la première fois, Visual Studio affiche une boîte de dialogue de sécurité qui vous avertit que le fournisseur de type est prêt à être exécuté. Avant Visual Studio charge le fournisseur de type, il vous donne la possibilité de décider si vous faites confiance à ce fournisseur. Si vous faites confiance à la source du fournisseur de type, puis sélectionnez « J’ai confiance ce fournisseur de type ». Si vous ne faites pas confiance à la source du fournisseur de type, puis sélectionnez « Je n’autorise pas ce fournisseur de type. » Approbation du fournisseur lui permet d’exécuter à l’intérieur de Visual Studio et de fournir IntelliSense et de générer des fonctionnalités. Mais si le fournisseur de type proprement dit est malveillant, son code en cours d’exécution susceptibles de compromettre votre ordinateur.

Si votre projet contient du code qui fait référence à des fournisseurs de type que vous avez choisi dans la boîte de dialogue ne pas faire confiance, puis au moment de la compilation, le compilateur signale une erreur qui indique que le fournisseur de type n’est pas approuvé. Tous les types qui sont dépendantes sur le fournisseur de type non approuvés sont indiquées par des soulignements ondulés rouges. Il est possible de parcourir le code dans l’éditeur.

Si vous décidez de modifier le paramètre d’approbation directement dans Visual Studio, procédez comme suit.

### <a name="to-change-the-trust-settings-for-type-providers"></a>Pour modifier les paramètres d’approbation pour les fournisseurs de type

1. Sur le `Tools` menu, sélectionnez `Options`, puis développez le `F# Tools` nœud.

2. Sélectionnez `Type Providers`, dans la liste des fournisseurs de type, sélectionnez la case à cocher pour les fournisseurs de type vous faites confiance et désactivez la case à cocher pour ceux qui vous ne faites pas confiance.

## <a name="see-also"></a>Voir aussi

- [Fournisseurs de type](index.md)
