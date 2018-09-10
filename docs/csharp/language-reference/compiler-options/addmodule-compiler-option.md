---
title: -addmodule (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /addmodule
helpviewer_keywords:
- /addmodule compiler option [C#]
- -addmodule compiler option [C#]
- addmodule compiler option [C#]
ms.assetid: ed604546-0dc2-4bd4-9a3e-610a8d973e58
ms.openlocfilehash: 39955d86085b49ef503ea9ed531df9feafa648ac
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43524586"
---
# <a name="-addmodule-c-compiler-options"></a>-addmodule (Options du compilateur C#)
Cette option ajoute un module créé avec le commutateur target:module à la compilation actuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-addmodule:file[;file2]  
```  
  
## <a name="arguments"></a>Arguments  
 `file`, `file2`  
 Fichier de sortie qui contient des métadonnées. Le fichier ne peut pas contenir un manifeste d’assembly. Pour importer plusieurs fichiers, séparez les noms des fichiers par une virgule ou un point-virgule.  
  
## <a name="remarks"></a>Notes  
 Tous les modules ajoutés par **-addmodule** doivent se trouver dans le même répertoire que le fichier de sortie au moment de l’exécution. Vous pouvez donc spécifier un module dans n’importe quel répertoire au moment de la compilation, mais le module doit se trouver dans le répertoire de l’application au moment de l’exécution. Si le module n’est pas dans le répertoire de l’application au moment de l’exécution, vous obtiendrez <xref:System.TypeLoadException>.  
  
 `file` ne peut pas contenir un assembly. Si, par exemple, le fichier de sortie a été créé avec [-target:module](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md), ses métadonnées peuvent être importées avec **-addmodule**.  
  
 Si le fichier de sortie a été créé avec une option **-target** autre que **-target:module**, ses métadonnées ne peuvent pas être importées avec **-addmodule**, mais peuvent l’être avec [-reference](../../../csharp/language-reference/compiler-options/reference-compiler-option.md).  
  
 Cette option du compilateur n’est pas disponible dans Visual Studio ; un projet ne peut pas référencer un module. Par ailleurs, cette option du compilateur ne peut pas être changée par programmation.  
  
## <a name="example"></a>Exemple  
 Compilez le fichier source `input.cs` et ajoutez les métadonnées de `metad1.netmodule` et `metad2.netmodule` pour produire `out.exe` :  
  
```console  
csc -addmodule:metad1.netmodule;metad2.netmodule -out:out.exe input.cs  
```  
  
## <a name="see-also"></a>Voir aussi  

- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)  
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)  
- [Assemblys multifichiers](../../../framework/app-domains/multifile-assemblies.md)  
- [Guide pratique pour générer un assembly multifichier](../../../framework/app-domains/how-to-build-a-multifile-assembly.md)
