---
title: -optimiser
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- optimize compiler option [Visual Basic]
- /optimize compiler option [Visual Basic]
- optimization [Visual Basic], enabling
- -optimize compiler option [Visual Basic]
ms.assetid: fcba4a97-3622-4b87-a891-0f77deab4998
caps.latest.revision: ''
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 7df1c873c166def9fde1bedc139470263e3e4437
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-optimize"></a>-optimiser
Active ou désactive les optimisations du compilateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-optimize[ + | - ]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`+` &#124; `-`|Facultatif. Le `-optimize-` option désactive les optimisations du compilateur. Le `-optimize+` option active les optimisations. Par défaut, les optimisations sont désactivées.|  
  
## <a name="remarks"></a>Notes  
 Les optimisations du compilateur diminuent la taille du fichier de sortie, le rendent plus rapide et plus efficace. Toutefois, étant donné que les optimisations entraînent une réorganisation du code dans le fichier de sortie `-optimize+` peut compliquer le débogage.  
  
 Tous les modules générés avec `-target:module` pour un assembly doit utiliser le même `-optimize` paramètres que l’assembly. Pour plus d’informations, consultez [-cible (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md).  
  
 Vous pouvez combiner la `-optimize` et `-debug` options.  
  
|Pour définir - optimiser dans l’environnement de développement intégré Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**.<br />     <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Cliquez sur le bouton **Avancées** .<br />4.  Modifier la **activer les optimisations** case à cocher.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et Active les optimisations du compilateur.  
  
```console
vbc t2.vb -optimize  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [-debug (Visual Basic)](../../../visual-basic/reference/command-line-compiler/debug.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
