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
ms.openlocfilehash: 89139867cb0a207dbe82168015629fcb9e2fa6eb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601894"
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
  
 Pour plus d’informations sur la définition de cette option du compilateur par programmation, consultez <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs`, en créant `in.netmodule` :  
  
```console  
csc -target:module in.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [-target (Options du compilateur C#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)
- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
