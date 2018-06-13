---
title: -refout (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [Visual Basic]
- /refout compiler option [Visual Basic]
- -refout compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 21cea76f31bdf2ac5fcf434ee759f874f917617b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653531"
---
# <a name="-refout-visual-basic"></a>-refout (Visual Basic)

L’option **-refout** spécifie un chemin de fichier où l’assembly de référence doit être généré.

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a>Syntaxe

```console
-refout:filepath
```

## <a name="arguments"></a>Arguments

 `filepath` Le chemin d’accès et le nom de l’assembly de référence. En règle générale, il doit être dans un sous-dossier de l’assembly principal. La convention recommandée (utilisée par MSBuild) consiste à placer l’assembly de référence dans un sous-dossier « ref/ » par rapport à l’assembly principal. Tous les dossiers dans `filepath` doit exister ; le compilateur ne pas les crée. 

## <a name="remarks"></a>Notes

Visual Basic prend en charge la `-refout` basculer depuis la version 15.3.

Les assemblys de référence sont uniquement des métadonnées des assemblys qui contiennent des métadonnées, mais aucun code d’implémentation. Elles incluent des informations de type et de membre pour tout sauf les types anonymes. Leurs corps de méthode sont remplacés par un seul `throw null` instruction. La raison de l’utilisation `throw null` des corps de méthode (par opposition à aucun corps) est afin que PEVerify peut exécuter et transmettre (par conséquent valider la conformité des métadonnées).

Incluent des assemblys de référence de niveau assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut. Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser). En raison de cet attribut, runtimes refuser de charger des assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement). Outils réfléchir les assemblys doivent s’assurer de que leur chargement des assemblys de référence en tant que de réflexion uniquement ; Sinon, le runtime lève une <xref:System.BadImageFormatException>.

Les options `-refout` et [`-refonly`](refonly-compiler-option.md) s’excluent mutuellement.

## <a name="see-also"></a>Voir aussi
[-refonly](refonly-compiler-option.md)   
[Compilateur de ligne de commande de Visual Basic](index.md)  
[Exemples de lignes de commande de compilation](sample-compilation-command-lines.md)  

