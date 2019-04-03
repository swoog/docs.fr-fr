---
title: -baseaddress
ms.date: 08/09/2018
f1_keywords:
- /baseaddress
- baseaddress
helpviewer_keywords:
- -baseaddress compiler option [Visual Basic]
- /baseaddress compiler option [Visual Basic]
- baseaddress compiler option [Visual Basic]
ms.assetid: c982bcf2-46e5-47a2-bc8f-a5cc32b7dc47
ms.openlocfilehash: 0550e4ad700494c8773a5d9b5b282dfa116adfed
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58813364"
---
# <a name="-baseaddress"></a>-baseaddress
Spécifie une adresse de base par défaut lors de la création d’une DLL.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-baseaddress:address  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`address`|Obligatoire. Adresse de base de la DLL. Cette adresse doit être spécifiée comme un nombre hexadécimal.|  
  
## <a name="remarks"></a>Notes  
 L’adresse de base par défaut pour une DLL est définie par le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].  
  
 N’oubliez pas que le mot de poids faible de cette adresse est arrondi. Par exemple, si vous spécifiez 0 x 11110001, elle est arrondie à 0 x 11110000.  
  
 Pour terminer le processus de signature d’une DLL, utilisez la `–R` option de l’outil Strong Name (Sn.exe).  
  
 Cette option est ignorée si la cible n’est pas une DLL.  
  
|Pour définir - baseaddress dans l’IDE Visual Studio|  
|---|  
|1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet**, cliquez sur **Propriétés**. <br />2.  Cliquez sur l’onglet **Compiler**.<br />3.  Cliquez sur **Avancé**.<br />4.  Modifiez la valeur dans le **adresse de base de DLL :** boîte. **Remarque :**      Le **adresse de base de DLL :** zone est en lecture seule, sauf si la cible est une DLL.|  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))
