---
title: '&#39;AddressOf&#39; opérande doit être le nom d’une méthode (sans parenthèses)'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 6f9827d885996ffab8bdab91d0f774a57073e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565148"
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
- [AddressOf (opérateur)](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Délégués](../../../visual-basic/programming-guide/language-features/delegates/index.md)
