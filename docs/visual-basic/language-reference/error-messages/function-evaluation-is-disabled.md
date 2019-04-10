---
title: L'évaluation de la fonction est désactivée, car une évaluation de fonction précédente a expiré
ms.date: 07/20/2015
f1_keywords:
- bc30957
- vbc30957
helpviewer_keywords:
- BC30957
ms.assetid: 561e593a-f50a-4b72-a708-4cab60ec7b28
ms.openlocfilehash: bc4d05e52434cf62fa90671d29b407c83114b5d2
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59315775"
---
# <a name="function-evaluation-is-disabled-because-a-previous-function-evaluation-timed-out"></a>L'évaluation de la fonction est désactivée, car une évaluation de fonction précédente a expiré
Évaluation de la fonction est désactivée, car une évaluation de fonction précédente a expiré. Pour réactiver l’évaluation de fonction, pas à pas, ou redémarrer le débogage.  
  
 Dans le débogueur Visual Studio, une expression spécifie un appel de procédure, mais une autre version d’évaluation a expiré.  
  
 Causes possibles d’un appel de procédure à délai d’expiration sont une boucle infinie ou *boucle sans fin*. Pour plus d’informations, consultez [pour... L’instruction suivante](../../../visual-basic/language-reference/statements/for-next-statement.md).  
  
 Un cas particulier d’une boucle infinie est *récursivité*. Pour plus d’informations, consultez [procédures récursives](../../../visual-basic/programming-guide/language-features/procedures/recursive-procedures.md).  
  
 **ID d’erreur :** BC30957  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Si possible, déterminez quel était l’évaluation de fonction précédente et la cause de son délai d’expiration. Sinon, vous pouvez rencontrer cette erreur à nouveau.  
  
2. Soit à nouveau, l’étape du débogueur ou arrêter et redémarrer le débogage.  
  
## <a name="see-also"></a>Voir aussi

- [Débogage dans Visual Studio](/visualstudio/debugger/debugging-in-visual-studio)
- [Naviguer dans le code avec le débogueur](/visualstudio/debugger/navigating-through-code-with-the-debugger)
