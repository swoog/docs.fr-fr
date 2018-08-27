---
title: -refonly (Visual Basic)
ms.date: 03/16/2018
f1_keywords:
- -refonly
helpviewer_keywords:
- /refonly compiler option [Visual Basic]
- -refonly compiler option [Visual Basic]
- refonly compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e8f6c15084ac9b1a07aef8a0311edfcc4a93337c
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932661"
---
# <a name="-refonly-visual-basic"></a>-refonly (Visual Basic)

Le **- refonly** option indique que la sortie principale de la compilation doit être un assembly de référence au lieu d’un assembly d’implémentation. Le paramètre `-refonly` désactive sans assistance la génération de fichiers PDB, car les assemblys de référence ne peuvent pas être exécutés.

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a>Syntaxe

```console
-refonly
```

## <a name="remarks"></a>Notes

Visual Basic prend en charge la `-refout` basculer à partir de la version 15.3.

Assemblys de référence sont des assemblys de métadonnées uniquement qui contiennent des métadonnées, mais aucun code d’implémentation. Elles incluent des informations de membre et de type pour tout sauf les types anonymes. L’utilisation de corps `throw null` (plutôt qu’aucun corps) permet la bonne exécution de PEVerify (et, par voie de conséquence, la validation de la conformité des métadonnées).

Assemblys de référence incluent un niveau de l’assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut. Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser). En raison de cet attribut, runtimes refusent de charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement). Les outils reflétés dans les assemblys doivent absolument que charger les assemblys de référence en mode réflexion uniquement ; Sinon, le runtime lève un <xref:System.BadImageFormatException>.

Les options `-refonly` et [`-refout`](refout-compiler-option.md) s’excluent mutuellement.

## <a name="see-also"></a>Voir aussi
[-refout](refout-compiler-option.md)   
[Compilateur de ligne de commande de Visual Basic](index.md)  
[Exemples de lignes de commande de compilation](sample-compilation-command-lines.md)   
