---
title: Caractéristiques d'éléments déclarés (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declared elements [Visual Basic], lifetime
- access levels, declared elements
- declared elements [Visual Basic], scope
- visibility [Visual Basic], declared elements
- elements [Visual Basic], programming
- scope [Visual Basic], declared elements
- lifetime [Visual Basic], declared elements
- declared elements [Visual Basic], access level
- data types [Visual Basic], declared elements
- declared elements [Visual Basic], visibility
ms.assetid: 1bc40fb8-b67c-4428-90a4-76b630ae2583
ms.openlocfilehash: c34175a90c2c9c247a37ac186a415a585d1d7e97
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582253"
---
# <a name="declared-element-characteristics-visual-basic"></a>Caractéristiques d'éléments déclarés (Visual Basic)
Un *caractéristique* d’un élément déclaré est un aspect de l’élément qui affecte la façon dont le code peut interagir avec elle. Chaque élément déclaré a un ou plusieurs des caractéristiques suivantes, il est associés :  
  
-   *Type de données* — les valeurs de l’élément peut contenir, et comment il stocke ces valeurs. Pour plus d’informations, consultez [Types de données](../../../../visual-basic/language-reference/data-types/index.md).  
  
-   *Durée de vie* — la période d’exécution au cours de laquelle l’élément est disponible pour utilisation. Pour plus d’informations, consultez [durée de vie dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md).  
  
-   *Étendue* — l’ensemble du code qui peut faire référence à l’élément sans qualifier son nom. Pour plus d'informations, voir [Procédure : Contrôler la portée d’une Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-control-the-scope-of-a-variable.md).  
  
-   *Niveau d’accès* — l’autorisation pour le code d’utiliser l’élément. Pour plus d'informations, voir [Procédure : Contrôler la disponibilité d’une Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-control-the-availability-of-a-variable.md).  
  
## <a name="characteristics-of-the-elements"></a>Caractéristiques des éléments  
 Le tableau suivant présente les éléments déclarés et les caractéristiques qui s’appliquent à chacun d’eux.  
  
|Élément|Type de données|Durée de vie|Étendue <sup>1</sup>|Niveau d’accès|  
|-------------|---------------|--------------|------------------------|------------------|  
|Variable|Oui|Oui|Oui|Oui|  
|Constante|Oui|Non|Oui|Oui|  
|Énumération|Oui|Non|Oui|Oui|  
|Structure|Aucune|Non|Oui|Oui|  
|Propriété|Oui|Oui|Oui|Oui|  
|Méthode|Aucune|Oui|Oui|Oui|  
|Procédure (`Sub` ou `Function`)|Aucune|Oui|Oui|Oui|  
|Paramètre de procédure|Oui|Oui|Oui|Aucune|  
|Retour de fonction|Oui|Oui|Oui|Aucune|  
|Opérateur|Oui|Non|Oui|Oui|  
|Interface|Aucune|Non|Oui|Oui|  
|Classe|Aucune|Non|Oui|Oui|  
|Événement|Aucune|Non|Oui|Oui|  
|délégué|Aucune|Non|Oui|Oui|  
  
 <sup>1</sup> étendue est parfois appelée *visibilité*.  
  
## <a name="see-also"></a>Voir aussi
- [Éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/index.md)
- [Noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Durée de vie en Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [Niveaux d’accès dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
