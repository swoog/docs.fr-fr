---
title: -refout (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [Visual Basic]
- /refout compiler option [Visual Basic]
- -refout compiler option [Visual Basic]
ms.openlocfilehash: 8a8068c467f9066af3153434187749fa80d254ca
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50048396"
---
# <a name="-refout-visual-basic"></a>-refout (Visual Basic)

L’option **-refout** spécifie un chemin de fichier où l’assembly de référence doit être généré.

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a>Syntaxe

```console
-refout:filepath
```

## <a name="arguments"></a>Arguments

 `filepath` Le chemin d’accès et le nom de l’assembly de référence. En règle générale, il doit être dans un sous-dossier de l’assembly principal. La convention recommandée (utilisée par MSBuild) consiste à placer l’assembly de référence dans un sous-dossier « ref/ » par rapport à l’assembly principal. Tous les dossiers `filepath` doit exister ; le compilateur ne crée pas les. 

## <a name="remarks"></a>Notes

Visual Basic prend en charge la `-refout` basculer à partir de la version 15.3.

Assemblys de référence sont des assemblys de métadonnées uniquement qui contiennent des métadonnées, mais aucun code d’implémentation. Elles incluent des informations de membre et de type pour tout sauf les types anonymes. Leurs corps de méthode sont remplacés par un seul `throw null` instruction. La raison pour l’utilisation de `throw null` corps de méthode (par opposition à aucun corps) est de pouvoir les PEVerify peut exécuter et passer (valider ainsi l’exhaustivité des métadonnées).

Assemblys de référence incluent un niveau de l’assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut. Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser). En raison de cet attribut, runtimes refusent de charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement). Les outils reflétés dans les assemblys doivent absolument que charger les assemblys de référence en mode réflexion uniquement ; Sinon, le runtime lève un <xref:System.BadImageFormatException>.

Les options `-refout` et [`-refonly`](refonly-compiler-option.md) s’excluent mutuellement.

## <a name="see-also"></a>Voir aussi
[-refonly](refonly-compiler-option.md)   
[Compilateur de ligne de commande de Visual Basic](index.md)  
[Exemples de lignes de commande de compilation](sample-compilation-command-lines.md)  

