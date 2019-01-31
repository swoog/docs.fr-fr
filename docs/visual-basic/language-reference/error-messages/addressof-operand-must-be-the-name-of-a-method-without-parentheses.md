---
title: L’opérande 'AddressOf' doit être le nom d’une méthode (sans parenthèses)
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 37b02ab76730458b757835fda37b8cb145ed93ad
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262112"
---
# <a name="addressof-operand-must-be-the-name-of-a-method-without-parentheses"></a>L’opérande 'AddressOf' doit être le nom d’une méthode (sans parenthèses)
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
