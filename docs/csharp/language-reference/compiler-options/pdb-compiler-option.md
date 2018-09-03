---
title: -pdb (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /pdb
helpviewer_keywords:
- -pdb compiler option [C#]
- pdb compiler option [C#]
- /pdb compiler option [C#]
ms.assetid: e9d0f96a-5b75-45d6-9765-92538dd5f823
ms.openlocfilehash: dc7ea6aae6aa429efdf1a2dca23a3d679cb21fb7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43418463"
---
# <a name="-pdb-c-compiler-options"></a>-pdb (Options du compilateur C#)
L’option de compilateur **-pdb** spécifie le nom et l’emplacement du fichier de symboles de débogage.  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-pdb:filename  
```  
  
## <a name="arguments"></a>Arguments  
 `filename`  
 Nom et emplacement du fichier de symboles de débogage.  
  
## <a name="remarks"></a>Notes  
 Quand vous spécifiez [-debug (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/debug-compiler-option.md), le compilateur crée un fichier .pdb dans le même répertoire que celui dans lequel le compilateur va créer le fichier de sortie (.exe ou .dll) avec un nom de fichier identique à celui du fichier de sortie.  
  
 **-pdb** vous permet de spécifier un nom de fichier autre que celui par défaut et un emplacement pour le fichier .pdb.  
  
 Cette option du compilateur ne peut pas être définie dans l’environnement de développement Visual Studio, ni être modifiée par programmation.  
  
## <a name="example"></a>Exemple  
 Compilez `t.cs` et créez un fichier .pdb sous le nom tt.pdb :  
  
```console  
csc -debug -pdb:tt t.cs  
```  
  
## <a name="see-also"></a>Voir aussi  

- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)  
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
