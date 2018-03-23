---
title: -highentropyva (Visual Basic)
ms.date: 03/10/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- highentropyva compiler option (Visual Basic)
- /highentropyva compiler option (Visual Basic)
ms.assetid: ff25f20a-6ca2-467b-9e52-5cf439f5028e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 12d40e5acda73786ee88d16bacd9bc5f69400be8
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-highentropyva-visual-basic"></a>-highentropyva (Visual Basic)
Indique si un exécutable 64 bits ou qui est marquée par le [/Platform : anycpu](../../../visual-basic/reference/command-line-compiler/platform.md) option du compilateur prend en charge la randomisation du format de mise en page espace adresse (ASLR) de forte entropie.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-highentropyva[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 Facultatif. L’option est désactivée par défaut ou si vous spécifiez `-highentropyva-`. L’option est activée si vous spécifiez `-highentropyva` ou `-highentropyva+`.  
  
## <a name="remarks"></a>Notes  
 Si vous spécifiez cette option, les versions compatibles du noyau Windows peuvent utiliser un degré d’entropie lorsque le noyau rend aléatoire la disposition de l’espace adresse d’un processus dans le cadre de l’ASLR. Si le noyau utilise un degré d’entropie, un plus grand nombre d’adresses peut être alloué à des régions de mémoire telles que les piles et de segments de mémoire. Par conséquent, il est plus difficile de deviner l’emplacement d’une zone de mémoire.  
  
 Lorsque l’option est activée, l’exécutable cible et tous les modules sur dont il dépend doit être en mesure de gérer les valeurs de pointeur qui sont supérieures à 4 gigaoctets (Go) lorsque ces modules sont exécutent en tant que processus 64 bits.  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
