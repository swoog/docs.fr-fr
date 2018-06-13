---
title: '&#39;AddressOf&#39; opérande doit être le nom d’une méthode (sans parenthèses)'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 701d86e03d9b14236eec8436d99ec40cebbbcd44
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33583810"
---
# <a name="39addressof39-operand-must-be-the-name-of-a-method-without-parentheses"></a>&#39;AddressOf&#39; opérande doit être le nom d’une méthode (sans parenthèses)
L’opérateur `AddressOf` crée une instance de délégué de procédure qui fait référence à une procédure spécifique. La syntaxe est la suivante.  
  
 `AddressOf` `procedurename`  
  
 Vous avez inséré des parenthèses autour de l’argument qui suit `AddressOf`, où aucune n’est nécessaire.  
  
 **ID d’erreur :** BC30577  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Supprimez les parenthèses autour de l’argument qui suit `AddressOf`.  
  
2.  Assurez-vous que l’argument est un nom de méthode.  
  
## <a name="see-also"></a>Voir aussi  
 [AddressOf (opérateur)](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [Délégués](../../../visual-basic/programming-guide/language-features/delegates/index.md)
