---
title: -target:module (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /target:module
helpviewer_keywords:
- -target compiler options [C#], /target:module
- target compiler options [C#], /target:module
- /target compiler options [C#], /target:module
ms.assetid: 9af1e4fa-c749-44e7-ae58-90a3d05d4e72
ms.openlocfilehash: 7cc0e48a7a4a3ec3f28c89e80fadf6aa7e1130f2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43393124"
---
# <a name="-targetmodule-c-compiler-options"></a>-target:module (Options du compilateur C#)
Cette option empêche le compilateur de générer un manifeste d’assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-target:module  
```  
  
## <a name="remarks"></a>Notes  
 Par défaut, le fichier de sortie créé en effectuant une compilation avec cette option porte l’extension .netmodule.  
  
 Un fichier ne disposant pas d’un manifeste d’assembly ne peut pas être chargé par le Common Language Runtime (CLR) .NET Framework. Cependant, un tel fichier peut être incorporé dans le manifeste d’un assembly au moyen de [-addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md).  
  
 Si plusieurs modules sont créés dans une seule compilation, les types [internal](../../../csharp/language-reference/keywords/internal.md) d’un module sont accessibles à d’autres modules dans la compilation. Quand le code d’un module référence des types `internal` dans un autre module, les deux modules doivent être incorporés dans un manifeste d’assembly au moyen de **-addmodule**.  
  
 La création d’un module n’est pas prise en charge dans l’environnement de développement Visual Studio.  
  
 Pour plus d’informations sur la façon de définir cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs`, en créant `in.netmodule` :  
  
```console  
csc -target:module in.cs  
```  
  
## <a name="see-also"></a>Voir aussi  

- [-target (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)  
- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
