---
title: Espace de pile insuffisant (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID28
ms.assetid: bfcd792b-ac29-4158-81fc-ea0c13f4ffa2
ms.openlocfilehash: e39be5913fe877cf7b3396e4f13f4440288cb8f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593283"
---
# <a name="out-of-stack-space-visual-basic"></a>Espace de pile insuffisant (Visual Basic)
La pile est une zone de travail de la mémoire augmente et se réduit dynamiquement aux demandes de votre programme en cours d’exécution. Ses limites ont été dépassées.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez que les procédures ne sont pas imbriquées trop profondément.  
  
2.  Assurez-vous que les procédures récursives se terminent correctement.  
  
3.  Si les variables locales requièrent davantage d’espace de variable locale qu’il n’est disponible, essayez de déclarer des variables au niveau du module. Vous pouvez également déclarer toutes les variables dans la procédure statique en faisant précéder le `Property`, `Sub`, ou `Function` mot clé with `Static`. Vous pouvez également utiliser la `Static` instruction pour déclarer des variables statiques individuelles au sein de procédures.  
  
4.  Redéfinissez certaines de vos chaînes de longueur fixe en tant que chaînes de longueur variable, comme les chaînes de longueur fixe utilisent davantage d’espace de pile que les chaînes de longueur variable. Vous pouvez également définir la chaîne au niveau du module où elle ne requiert aucun espace de pile.  
  
5.  Vérifiez le nombre d’imbriquée `DoEvents` appels de fonctions, à l’aide de la `Calls` boîte de dialogue pour afficher les procédures actives sur la pile.  
  
6.  Assurez-vous que vous n’avez pas provoqué une « cascade d’événements » en déclenchant un événement qui appelle une procédure événementielle déjà sur la pile. Une cascade d’événements est similaire à un appel de procédure récursive inachevé, mais elle est moins évidente, étant donné que l’appel est effectué en Visual Basic, plutôt qu’un appel explicite dans le code. Utilisez le `Calls` boîte de dialogue pour afficher les procédures actives sur la pile.  
  
## <a name="see-also"></a>Voir aussi  
 [Fenêtres Mémoire](/visualstudio/debugger/memory-windows)
