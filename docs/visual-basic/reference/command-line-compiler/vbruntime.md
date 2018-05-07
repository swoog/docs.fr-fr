---
title: -vbruntime
ms.date: 03/13/2018
f1_keywords:
- vbruntime
- -vbruntime
helpviewer_keywords:
- vbruntime compiler option [Visual Basic]
- -vbruntime compiler option [Visual Basic]
- /vbruntime compiler option [Visual Basic]
ms.assetid: 1aa0239e-511a-4c29-957d-fd72877b350a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d28d0556a662099e4e5e74b22583fc3c8b4c313f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="-vbruntime"></a>-vbruntime
Spécifie que le compilateur doit compiler sans référence à la bibliothèque runtime Visual Basic, ou avec une référence à une bibliothèque runtime spécifique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-vbruntime:{ - | + | * | path }  
```  
  
## <a name="arguments"></a>Arguments  
 \-  
 Compiler sans référence à la bibliothèque Runtime Visual Basic.  
  
 \+  
 Compiler avec une référence à la bibliothèque Runtime Visual Basic par défaut.  
  
 \*  
 Compiler sans référence à la bibliothèque Runtime Visual Basic et incorporer la fonctionnalité principale de la bibliothèque Runtime Visual Basic dans l’assembly.  
  
 `path`  
 Compilez avec une référence à la bibliothèque spécifiée (DLL).  
  
## <a name="remarks"></a>Notes  
 Le `-vbruntime` option du compilateur permet de spécifier que le compilateur doit compiler sans référence à la bibliothèque Runtime Visual Basic. Si vous compilez sans référence à la bibliothèque Runtime Visual Basic, erreurs ou avertissements sont consignés sur les constructions de code ou de langage qui génèrent un appel à une application d’assistance du runtime Visual Basic. (A *le programme d’assistance de Visual Basic runtime* est une fonction définie dans Microsoft.VisualBasic.dll, qui est appelée pendant l’exécution pour exécuter une sémantique de langue spécifique.)  
  
 Le `-vbruntime+` option produit le même comportement se produit si aucun `-vbruntime` commutateur est spécifié. Vous pouvez utiliser la `-vbruntime+` option permettant de remplacer la précédente `-vbruntime` commutateurs.  
  
 La plupart des objets de la `My` type ne sont pas disponibles lorsque vous utilisez la `-vbruntime-` ou `-vbruntime:path` options.  
  
## <a name="embedding-visual-basic-runtime-core-functionality"></a>L’incorporation de fonctionnalités principales Runtime de Visual Basic  
 Le `-vbruntime*` option vous permet de compiler sans référence à une bibliothèque runtime. Au lieu de cela, les fonctionnalités de base à partir de la bibliothèque Runtime Visual Basic sont incorporées dans l’assembly de l’utilisateur. Vous pouvez utiliser cette option si votre application s’exécute sur les plateformes qui ne contiennent pas le runtime Visual Basic.  
  
 Les membres du runtime suivants sont incorporés :  
  
-   Classe <xref:Microsoft.VisualBasic.CompilerServices.Conversions>  
  
-   Méthode <xref:Microsoft.VisualBasic.Strings.AscW%28System.Char%29>  
  
-   Méthode <xref:Microsoft.VisualBasic.Strings.AscW%28System.String%29>  
  
-   Méthode <xref:Microsoft.VisualBasic.Strings.ChrW%28System.Int32%29>  
  
-   <xref:Microsoft.VisualBasic.Constants.vbBack> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbCr> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbCrLf> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbFormFeed> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbLf> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbNewLine> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbNullChar> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbNullString> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbTab> Constante  
  
-   <xref:Microsoft.VisualBasic.Constants.vbVerticalTab> Constante  
  
-   Certains objets de la `My` type  
  
 Si vous compilez à l’aide de la `-vbruntime*` option et votre code fait référence à un membre de la bibliothèque Runtime Visual Basic qui ne sont pas incorporées avec la fonctionnalité principale, le compilateur renvoie une erreur indiquant que le membre n’est pas disponible.  
  
## <a name="referencing-a-specified-library"></a>Fait référence à une bibliothèque spécifiée  
 Vous pouvez utiliser la `path` argument compilé avec une référence à une bibliothèque de runtime personnalisé au lieu de la bibliothèque Runtime Visual Basic par défaut.  
  
 Si la valeur de la `path` argument est un chemin d’accès complet à une DLL, le compilateur utilisera ce fichier comme bibliothèque runtime. Si la valeur de la `path` argument n’est pas un chemin d’accès complet à une DLL, le compilateur Visual Basic recherchera la DLL identifiée dans le dossier actif tout d’abord. Il recherche ensuite dans le chemin d’accès que vous avez spécifié à l’aide de la [- sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md) option du compilateur. Si le `-sdkpath` option du compilateur n’est pas utilisée, le compilateur recherche la DLL identifiée dans le dossier .NET Framework (`%systemroot%\Microsoft.NET\Framework\versionNumber`).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `-vbruntime` possibilité de compiler avec une référence à une bibliothèque personnalisée.  
  
```console
vbc -vbruntime:C:\VBLibraries\CustomVBLibrary.dll  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Visual Basic Core – nouveau mode de compilation dans Visual Studio 2010 SP1](http://blogs.msdn.com/b/vbteam/archive/2011/01/10/vb-core-new-compilation-mode-in-visual-studio-2010-sp1.aspx)  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [-sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md)
