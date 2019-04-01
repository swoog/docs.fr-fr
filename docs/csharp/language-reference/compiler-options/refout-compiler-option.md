---
title: -refout (Options du compilateur C#)
ms.date: 08/08/2017
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [C#]
- /refout compiler option [C#]
- -refout compiler option [C#]
ms.openlocfilehash: 06d21843c6e2d7aeb1858c3ce72426d080f73595
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58410210"
---
# <a name="-refout-c-compiler-options"></a>-refout (Options du compilateur C#)

L’option **-refout** spécifie un chemin de fichier où l’assembly de référence doit être généré. Cela se traduit par `metadataPeStream` dans l’API Emit.

## <a name="syntax"></a>Syntaxe

```console
-refout:filepath
```

## <a name="arguments"></a>Arguments

 `filepath` Chemin de l’assembly de référence. Il doit généralement correspondre à celui de l’assembly principal. La convention recommandée (utilisée par MSBuild) consiste à placer l’assembly de référence dans un sous-dossier « ref/ » par rapport à l’assembly principal.

## <a name="remarks"></a>Remarques

Les assemblys de métadonnées uniquement ont leurs corps de méthode remplacés par un corps `throw null` unique, mais incluent tous les membres à l’exception des types anonymes. L’utilisation de corps `throw null` (plutôt qu’aucun corps) permet la bonne exécution de PEVerify (et, par voie de conséquence, la validation de la conformité des métadonnées).

Les assemblys de référence incluent un attribut `ReferenceAssembly` de niveau assembly. Cet attribut peut être spécifié dans la source (le compilateur n’a plus alors besoin de le synthétiser). En raison de cet attribut, les runtimes refusent de charger les assemblys de référence pour l’exécution (mais ils peuvent toujours être chargés en mode de réflexion uniquement). Les outils reflétés dans les assemblys doivent absolument charger les assemblys de référence en mode réflexion uniquement, sinon ils reçoivent une erreur de chargement de type de la part du runtime.

En outre, les assemblys de référence suppriment les métadonnées (membres privés) des assemblys de métadonnées uniquement :

- Un assembly de référence a uniquement des références pour ce dont il a besoin dans la surface de l’API. L’assembly réel peut avoir des références supplémentaires relatives à des implémentations spécifiques. Par exemple, l’assembly de référence pour `class C { private void M() { dynamic d = 1; ... } }` ne référence aucun des types requis pour `dynamic`.
- Les membres de fonction privés (méthodes, propriétés et événements) sont supprimés si leur suppression n’affecte pas la compilation sensiblement. S’il n’y a aucun attribut <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>, faites de même pour les membres de fonction internes.
- Toutefois, tous les types (y compris les types privés ou imbriqués) sont conservés dans les assemblys de référence. Tous les attributs sont conservés (même les attributs internes).
- Toutes les méthodes virtuelles sont conservées. Les implémentations d’interface explicite sont conservées. Les propriétés et les événements implémentés explicitement sont conservés, car leurs accesseurs sont virtuels (et donc conservés).
- Tous les champs d’un struct sont conservés. (Candidat pour une optimisation future de C# 7.1)

Les options `-refout` et [`-refonly`](refonly-compiler-option.md) s’excluent mutuellement.

## <a name="see-also"></a>Voir aussi

- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
