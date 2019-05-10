---
title: "'<methodname>' a plusieurs définitions comportant des signatures identiques"
ms.date: 07/20/2015
f1_keywords:
- vbc30269
- bc30269
helpviewer_keywords:
- BC30269
ms.assetid: 39489621-6617-4e5c-9b24-c2faf8273891
ms.openlocfilehash: b884220053bbcec633c964a41892bc8df42f41c7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64602438"
---
# <a name="methodname-has-multiple-definitions-with-identical-signatures"></a>'\<nom_méthode >' a plusieurs définitions comportant des signatures identiques
Un `Function` ou `Sub` déclaration de procédure utilise la liste de nom et l’argument de procédure identiques comme une déclaration précédente. Une des causes possibles sont une tentative de surcharge de la procédure d’origine. Procédures surchargées doivent avoir des listes d’arguments différentes.  
  
 **ID d’erreur :** BC30269  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Modifier le nom de la procédure ou la liste d’arguments, ou supprimez la déclaration en double.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Considérations sur les surcharges de procédures](../../../visual-basic/programming-guide/language-features/procedures/considerations-in-overloading-procedures.md)
