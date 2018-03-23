---
title: -/langversion (Visual Basic)
ms.date: 03/10/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- /langversion compiler option [Visual Basic]
- langversion compiler option [Visual Basic]
- -langversion compiler option [Visual Basic]
ms.assetid: 59b7b0c8-2dde-4e9b-94e7-0237f7e0bafb
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d9b91bf8efa6fabd21d257e51062dc881ab288f5
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-langversion-visual-basic"></a>-/langversion (Visual Basic)
Entraîne le compilateur à accepter uniquement la syntaxe qui est incluse dans la version du langage Visual Basic spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-langversion:version  
```  
  
## <a name="arguments"></a>Arguments  
 `version`  
 Obligatoire. La langue à utiliser lors de la compilation. Valeurs acceptées sont `9`, `9.0`, `10`, et `10.0`.  
  
## <a name="remarks"></a>Notes  
 Le `-langversion` option spécifie la syntaxe acceptée par le compilateur. Par exemple, si vous spécifiez que la version est 9.0, le compilateur génère des erreurs de syntaxe qui est valide uniquement dans la version 10.0 et versions ultérieures.  
  
 Vous pouvez utiliser cette option lorsque vous développez des applications qui ciblent des versions différentes du .NET Framework. Par exemple, si vous ciblez .NET Framework 3.5, vous pouvez utiliser cette option pour vous assurer que vous n’utilisez pas la syntaxe de la version de langage 10.0.  
  
 Vous pouvez définir `-langversion` directement uniquement à l’aide de la ligne de commande. Pour plus d’informations, consultez [Ciblage d’une version spécifique du .NET Framework](/visualstudio/ide/targeting-a-specific-dotnet-framework-version).  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `sample.vb` pour Visual Basic 9.0.  
  
```console  
vbc -langversion:9.0 sample.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Cibler une version spécifique du .NET Framework](/visualstudio/ide/targeting-a-specific-dotnet-framework-version)
