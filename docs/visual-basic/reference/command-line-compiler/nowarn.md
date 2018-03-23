---
title: -nowarn
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- nowarn compiler option [Visual Basic]
- /nowarn compiler option [Visual Basic]
- -nowarn compiler option [Visual Basic]
ms.assetid: 7ebf2106-0652-4fdc-bf60-70fc86465d83
caps.latest.revision: ''
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d2f3f15ef12b24b8baedc9db59e772aa9eb073bc
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-nowarn"></a>-nowarn
Supprime la capacité du compilateur à générer des avertissements.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-nowarn[:numberList]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`numberList`|Facultatif. Liste délimitée les ID des numéros d’avertissement que le compilateur doit supprimer. Si l’ID d’avertissement ne sont pas spécifié, tous les avertissements sont supprimés.|  
  
## <a name="remarks"></a>Notes  
 La `-nowarn` option, le compilateur ne génère ne pas les avertissements. Pour supprimer un avertissement, fournissez l’ID d’avertissement pour le `-nowarn` option suit le signe deux-points. Séparez plusieurs numéros d’avertissement par des virgules.  
  
 Vous devez spécifier uniquement la partie numérique de l’identificateur d’avertissement. Par exemple, si vous souhaitez supprimer BC42024, numéro d’avertissement pour les variables locales inutilisées, spécifiez `-nowarn:42024`.  
  
 Pour plus d’informations sur les numéros d’avertissement, consultez [configuration des avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
|Pour définir /nowarn - dans l’environnement de développement intégré Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Sélectionnez le **désactiver tous les avertissements** case à cocher pour désactiver tous les avertissements.<br />     ou<br />     Pour désactiver un avertissement particulier, cliquez sur **aucun** dans la liste déroulante adjacente à l’avertissement.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et n’affiche pas les avertissements.  
  
```console
vbc -nowarn t2.vb  
```  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et n’affiche pas les avertissements pour les variables locales inutilisées (42024).  
  
```console
vbc -nowarn:42024 t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Configuration d’avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)
