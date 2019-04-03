---
title: Le constructeur '<name>' ne peut pas s'appeler lui-même
ms.date: 07/20/2015
f1_keywords:
- bc30298
- vbc30298
helpviewer_keywords:
- BC30298
ms.assetid: 2d77b7f4-0640-4f89-9c65-f101fd2847c0
ms.openlocfilehash: ef20f74055a07071ef9634973c6852ac58c3143c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824705"
---
# <a name="constructor-name-cannot-call-itself"></a>Constructeur '\<nom >' ne peut pas s’appeler lui-même
Un `Sub New` procédure dans une classe ou structure s’appelle elle-même.  
  
 L’objectif d’un constructeur doit initialiser une instance d’une classe ou structure lors de sa création. Une classe ou structure peut avoir plusieurs constructeurs, fournies ont tous des listes de paramètres différentes. Un constructeur est autorisé à appeler un autre constructeur pour exécuter ses fonctionnalités en plus de son propre. Mais il n’a aucune signification pour un constructeur s’appelle elle-même, et en fait il entraînerait une récurrence infinie si autorisé.  
  
 **ID d’erreur :** BC30298  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez la liste des paramètres du constructeur appelé. Il doit être différent de celui du constructeur qui effectue l’appel.  
  
2.  Si vous ne souhaitez pas appeler un autre constructeur, supprimez le `Sub New` intégralité de l’appel.  
  
## <a name="see-also"></a>Voir aussi

- [Durée de vie d’objet : Comment les objets sont créés et détruits](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
