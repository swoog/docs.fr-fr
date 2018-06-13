---
title: -warnaserror (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- warnaserror compiler option [Visual Basic]
- /warnaserror compiler option [Visual Basic]
- -warnaserror compiler option [Visual Basic]
ms.assetid: 49819f1d-a1bd-4201-affe-5afe6d9712e1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6c04bff4070b0f1c288c8853e5045fbf670d8e9e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33655667"
---
# <a name="-warnaserror-visual-basic"></a>-warnaserror (Visual Basic)
Indique au compilateur de traiter la première occurrence d’un avertissement comme une erreur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-warnaserror[+ | -][:numberList]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|+ &#124; -|Facultatif. Par défaut, `-warnaserror-` est en vigueur ; les avertissements n’empêchent pas le compilateur de générer un fichier de sortie. Le `-warnaserror` option, qui est le même que `-warnaserror+`, génère des avertissements à traiter comme des erreurs.|  
|`numberList`|Facultatif. Liste délimitée par des virgules l’ID d’avertissement numéros à laquelle le `-warnaserror` option s’applique. Si aucun ID d’avertissement n’est spécifié, le `-warnaserror` option s’applique à tous les avertissements.|  
  
## <a name="remarks"></a>Notes  
 Le `-warnaserror` option traite tous les avertissements comme des erreurs. Les messages qui seraient normalement signalés comme avertissements apparaissent comme des erreurs. Le compilateur signale les autres occurrences du même avertissement en tant qu’avertissements.  
  
 Par défaut, `-warnaserror-` est en vigueur, ce qui provoque les avertissements d’information uniquement. Le `-warnaserror` option, qui est le même que `-warnaserror+`, génère des avertissements à traiter comme des erreurs.  
  
 Si vous souhaitez que seuls certains avertissements spécifiques à traiter comme des erreurs, vous pouvez spécifier une liste séparée par des virgules des numéros d’avertissement à traiter comme des erreurs.  
  
> [!NOTE]
>  Le `-warnaserror` option ne contrôle pas l’affichage des avertissements. Utilisez le [- nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) option pour désactiver les avertissements.  
  
|Pour définir /warnaserror - pour traiter tous les avertissements comme des erreurs dans l’IDE de Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Assurez-vous que le **désactiver tous les avertissements** case à cocher est désactivée.<br />4.  Vérifiez le **traiter tous les avertissements comme des erreurs** case à cocher.|  
  
|Pour définir /warnaserror - pour traiter certains avertissements comme des erreurs dans l’IDE de Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**.<br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Assurez-vous que le **désactiver tous les avertissements** case à cocher est désactivée.<br />4.  Assurez-vous que le **traiter tous les avertissements comme des erreurs** case à cocher est désactivée.<br />5.  Sélectionnez **erreur** à partir de la **Notification** colonne adjacente à l’avertissement qui doit être traitée comme une erreur.|  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `In.vb` et indique au compilateur d’afficher une erreur pour la première occurrence de chaque avertissement rencontré.  
  
```console
vbc -warnaserror in.vb  
```  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et traite uniquement l’avertissement pour les variables locales inutilisées (42024) comme une erreur.  
  
```console
vbc -warnaserror:42024 t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Configuration d’avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)
