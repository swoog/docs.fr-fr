---
title: Sécurité du fournisseur de type
description: 'En savoir plus sur la sécurité du fournisseur de type en F #, notamment comment modifier les paramètres d’approbation pour un fournisseur de type.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 4f0b55062aec6c560112fe10ca4df77f42493011
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="type-provider-security"></a>Sécurité du fournisseur de type

Fournisseurs de type sont des assemblys (DLL) référencés par votre projet F # ou un script qui contiennent du code pour vous connecter aux sources de données externes et d’exposer ces informations de type dans l’environnement de type F #. En règle générale, le code dans les assemblys référencés s’exécute seulement lorsque vous compilez et exécutez le code (ou dans le cas d’un script, envoyez le code à F # Interactive). Toutefois, un assembly de fournisseur de type sera exécuté à l’intérieur de Visual Studio lorsque le code est simplement parcouru dans l’éditeur. Cela se produit, car les fournisseurs de type doivent exécuter pour ajouter des informations supplémentaires sur l’éditeur, telles que des info-bulles Info express, aux achèvements IntelliSense et ainsi de suite. Par conséquent, il existe des considérations de sécurité supplémentaires pour le type des assemblys de fournisseur, car ils s’exécuter automatiquement au sein du processus Visual Studio.


## <a name="security-warning-dialog"></a>Boîte de dialogue sécurité avertissement
Lorsque vous utilisez un assembly de fournisseur de type particulier pour la première fois, Visual Studio affiche une boîte de dialogue de sécurité qui vous avertit que le fournisseur de type est prêt à être exécuté. Avant Visual Studio charge le fournisseur de type, il vous donne la possibilité de décider si vous faites confiance à ce fournisseur. Si vous faites confiance à la source du fournisseur de type, puis sélectionnez « Je n’approuver ce fournisseur de type ». Si vous ne faites pas confiance à la source du fournisseur de type, puis sélectionnez « Je n’autorise pas ce fournisseur de type. » Approbation du fournisseur permet à exécuter à l’intérieur de Visual Studio et de fournir IntelliSense et de créer des fonctionnalités. Mais si le fournisseur de type lui-même est malveillant, son code en cours d’exécution susceptibles de compromettre votre ordinateur.

Si votre projet contient du code qui fait référence à des fournisseurs de type que vous avez choisi dans la boîte de dialogue ne pas à approuver, puis au moment de la compilation, le compilateur signale une erreur qui indique que le fournisseur de type n’est pas fiable. Tous les types qui en dépendent du fournisseur de type non approuvés sont indiquées par des soulignements ondulés rouges. Il est possible de parcourir le code dans l’éditeur.

Si vous décidez de modifier le paramètre de confiance directement dans Visual Studio, procédez comme suit.


#### <a name="to-change-the-trust-settings-for-type-providers"></a>Pour modifier les paramètres d’approbation pour les fournisseurs de type

1. Sur le `Tools` menu, sélectionnez `Options`, puis développez le `F# Tools` nœud.
<br />

2. Sélectionnez `Type Providers`, dans la liste des fournisseurs de type, sélectionnez la case à cocher pour les fournisseurs de type que vous faites confiance et désactivez la case à cocher pour ceux qui vous ne faites pas confiance.
<br />


## <a name="see-also"></a>Voir aussi
[Fournisseurs de type](index.md)
