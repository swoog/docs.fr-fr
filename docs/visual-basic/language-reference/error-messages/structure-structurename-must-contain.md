---
title: La structure '<structurename>' doit contenir au moins une variable membre d'instance ou au moins une déclaration d'événement d'instance non marquée comme 'Custom'.
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: 598aef3943a53ee6eb97064819c9128de1839f52
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58813936"
---
# <a name="structure-structurename-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-custom"></a>Structure '\<nom_structure >' doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme 'Custom'
Une définition de structure n’inclut pas les variables non partagées ou des événements non personnalisés non partagées.  
  
 Chaque structure doit avoir une variable ou un événement qui s’applique à chaque instance spécifique (non partagée) et non à toutes les instances collectivement ([partagé](../../../visual-basic/language-reference/modifiers/shared.md)). Les procédures, les propriétés et les constantes non partagées ne répondent pas à cette exigence. En outre, s’il y a aucune variable non partagée et qu’un seul événement non partagé, cet événement ne peut pas être un `Custom` événement.  
  
 **ID d’erreur :** BC30941  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Définissez au moins une variable ou un événement qui n’est pas `Shared`. Si vous définissez un seul événement, il doit être non personnalisés, ainsi que non partagée.  
  
## <a name="see-also"></a>Voir aussi

- [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Guide pratique pour déclarer une structure](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
