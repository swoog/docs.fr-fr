---
title: Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: 253e7ff1d457827a2e1cb9f64eae4bfa971a3798
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645871"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a>Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
Une opération cyclique a échoué. Les opérations cycliques se répètent et, par conséquent, ne peuvent pas s’achever. Par exemple, l’objet A peut essayer d’hériter de l’objet B qui hérite, à son tour, de l’objet A.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Lors d’un héritage, vérifiez qu’il n’existe aucune référence cyclique.  
  
## <a name="see-also"></a>Voir aussi
- [Types d’erreurs](../../visual-basic/programming-guide/language-features/error-types.md)
- [Principes de base pour le débogage : Points d’arrêt](https://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
