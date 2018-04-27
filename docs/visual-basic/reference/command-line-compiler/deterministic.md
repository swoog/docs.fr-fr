---
title: -déterministe
ms.date: 04/11/2018
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- deterministic compiler option [Visual Basic]
- -deterministic compiler option [Visual Basic]
- -deterministic compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 273abf8811f04cd7f58599ce3421ca1f17c740d9
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="-deterministic"></a>-déterministe

Indique au compilateur de produire un assembly dont la sortie octet est identique sur les compilations pour des entrées identiques. 

## <a name="syntax"></a>Syntaxe

```
-deterministic
```

## <a name="remarks"></a>Notes

Par défaut, les résultats de la compilation à partir d’un ensemble donné d’entrées est unique, étant donné que le compilateur ajoute un horodateur et un GUID qui est généré à partir de nombres aléatoires. Vous utilisez la `-deterministic` option pour générer un *assembly déterministe*, dont le contenu binaire est identique entre les compilations tant que l’entrée reste le même.

Le compilateur considère les entrées suivantes à des fins de déterminisme :

- La séquence de paramètres de ligne de commande.
- Le contenu du fichier de réponse du compilateur .rsp.
- La version précise du compilateur utilisé et ses assemblys référencés.
- Le chemin du répertoire actuel.
- Le contenu binaire de tous les fichiers explicitement passé au compilateur directement ou indirectement, y compris : 
    - Fichiers sources
    - assemblys référencés
    - Modules référencés
    - Ressources
    - Le fichier de clé de nom fort
    - @ fichiers réponse
    - Analyseurs
    - Groupes de règles
    - Fichiers supplémentaires qui peuvent être utilisées par des analyseurs
- La culture actuelle (pour le langage dans lequel les tests de diagnostic et exception messages sont produites).
- L’encodage par défaut (ou la page de codes en cours) si l’encodage n’est pas spécifié.
- L’existence, la non existence et le contenu des fichiers sur les chemins de recherche du compilateur (spécifié, par exemple, en `/lib` ou `/recurse`).
- La plateforme CLR sur lequel est exécuté le compilateur.
- La valeur de `%LIBPATH%`, qui peut affecter le chargement de dépendance analyzer.

Lorsque les sources sont accessibles, compilation déterministe peut servir pour établir si un fichier binaire est compilé à partir d’une source approuvée. Il peut également être utile dans un système de build en continu pour déterminer si les étapes de génération qui sont dépendantes des modifications apportées à un fichier binaire doivent être exécutée. 

## <a name="see-also"></a>Voir aussi
[Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
[Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
