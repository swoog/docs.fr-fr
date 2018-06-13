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
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653044"
---
# <a name="-refonly-visual-basic"></a>-refonly (Visual Basic)

Le **- refonly** option indique que la sortie principale de la compilation doit être un assembly de référence au lieu d’un assembly de l’implémentation. Le paramètre `-refonly` désactive sans assistance la génération de fichiers PDB, car les assemblys de référence ne peuvent pas être exécutés.

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a>Syntaxe

```console
-refonly
```

## <a name="remarks"></a>Notes

Visual Basic prend en charge la `-refout` basculer depuis la version 15.3.

Les assemblys de référence sont uniquement des métadonnées des assemblys qui contiennent des métadonnées, mais aucun code d’implémentation. Elles incluent des informations de type et de membre pour tout sauf les types anonymes. L’utilisation de corps `throw null` (plutôt qu’aucun corps) permet la bonne exécution de PEVerify (et, par voie de conséquence, la validation de la conformité des métadonnées).

Incluent des assemblys de référence de niveau assembly [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribut. Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser). En raison de cet attribut, runtimes refuse charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés dans un contexte de réflexion uniquement). Outils réfléchir les assemblys doivent s’assurer de que leur chargement des assemblys de référence en tant que de réflexion uniquement ; Sinon, le runtime lève une <xref:System.BadImageFormatException>.

Les options `-refonly` et [`-refout`](refout-compiler-option.md) s’excluent mutuellement.

## <a name="see-also"></a>Voir aussi
[-refout](refout-compiler-option.md)   
[Compilateur de ligne de commande de Visual Basic](index.md)  
[Exemples de lignes de commande de compilation](sample-compilation-command-lines.md)   
