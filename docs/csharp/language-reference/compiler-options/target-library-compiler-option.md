---
title: -target:library (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /dll
helpviewer_keywords:
- -target compiler options [C#], /target:library
- target compiler options [C#], /target:library
- /target compiler options [C#], /target:library
ms.assetid: c5670e88-2126-47c1-8d1c-217923837d17
ms.openlocfilehash: 2e0935965e9225ab524290429803fe4c9ccc80c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59313643"
---
# <a name="-targetlibrary-c-compiler-options"></a>-target:library (Options du compilateur C#)
L’option **-target:library** indique au compilateur de créer une bibliothèque de liens dynamiques (DLL) à la place d’un fichier exécutable (EXE).  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-target:library  
```  
  
## <a name="remarks"></a>Remarques  
 La DLL est créée avec l’extension .dll.  
  
 Sauf spécification contraire avec l’option [-out](../../../csharp/language-reference/compiler-options/out-compiler-option.md), le fichier de sortie prend le nom du premier fichier d’entrée.  
  
 Quand ils sont spécifiés dans la ligne de commande, tous les fichiers jusqu’à l’option **-out** ou **-target:module** suivante sont utilisés pour créer le fichier .dll.  
  
 Lors de la création d’un fichier .dll, une méthode [Main](../../../csharp/programming-guide/main-and-command-args/index.md) n’est pas obligatoire.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1. Ouvrez la page **Propriétés** du projet.  
  
2. Cliquez sur la page de propriétés **Application**.  
  
3. Modifiez la propriété **Type de sortie**.  
  
 Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs`, en créant `in.dll` :  
  
```console  
csc -target:library in.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [-target (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
