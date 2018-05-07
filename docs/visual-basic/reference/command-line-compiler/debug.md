---
title: /debug (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- debug compiler switches
- /debug compiler option [Visual Basic]
- -debug compiler option [Visual Basic]
- debug compiler option [Visual Basic]
ms.assetid: c2b0bea5-1d5e-499f-9bd5-4f6c6b715ea2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 18d74b8f0a7b319e08780a8db9175c7be16d932e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="-debug-visual-basic"></a>-debug (Visual Basic)
Indique au compilateur de générer des informations de débogage et les placer dans les fichiers de sortie.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-debug[+ | -]  
' -or-  
-debug:[full | pdbonly]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`+` &#124; `-`|Facultatif. Spécification de `+` ou `/debug` indique au compilateur de générer des informations de débogage et les placer dans un fichier .pdb. Spécification de `-` a le même effet que de ne pas spécifier `/debug`.|  
|`full` &#124; `pdbonly`|Facultatif. Indique le type d'informations de débogage générées par le compilateur. Si vous ne spécifiez pas `/debug:pdbonly`, la valeur par défaut est `full`, ce qui vous permet d’associer un débogueur au programme en cours d’exécution. Le `pdbonly` argument permet le débogage du code source lorsque le programme est démarré dans le débogueur, mais affiche du code en langage assembleur uniquement lorsque le programme en cours d’exécution est attaché au débogueur.|  
  
## <a name="remarks"></a>Notes  
 Utilisez cette option pour créer des versions Debug. Si vous ne spécifiez pas `/debug`, `/debug+`, ou `/debug:full`, vous ne pouvez pas déboguer le fichier de sortie de votre programme.  
  
 Par défaut, les informations de débogage ne sont pas émises (`/debug-`). Pour émettre des informations de débogage, spécifiez `/debug` ou `/debug+`.  
  
 Pour plus d’informations sur la configuration des performances de débogage d’une application, consultez [Simplification du débogage d’une image](../../../framework/debug-trace-profile/making-an-image-easier-to-debug.md).  
  
|Pour définir - déboguez dans l’environnement de développement intégré Visual Studio|  
|---|  
|1.  Après avoir sélectionné un projet dans l’ **Explorateur de solutions**, dans le menu **Projet** , cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Cliquez sur **Options avancées de compilation**.<br />4.  Modifiez la valeur dans la **générer des infos de débogage** boîte.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant place des informations de débogage dans le fichier de sortie `App.exe`.  
  
```  
vbc -debug -out:app.exe test.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
