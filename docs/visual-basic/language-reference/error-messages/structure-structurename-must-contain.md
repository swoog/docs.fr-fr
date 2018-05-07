---
title: Structure &#39; &lt;nom_structure&gt; &#39; doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme &#39;personnalisé&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: 85a4babc808e274a99f2c9faf08a02abf8aa4e93
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="structure-39ltstructurenamegt39-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-39custom39"></a>Structure &#39; &lt;nom_structure&gt; &#39; doit contenir au moins une variable membre d’instance ou une déclaration d’événement au moins une instance non marquée comme &#39;personnalisé&#39;
Une définition de structure n’inclut pas toutes les variables non partagées ou des événements non personnalisés non partagées.  
  
 Chaque structure doit avoir une variable ou un événement qui s’applique à chaque instance spécifique (non partagée) et non à toutes les instances collectivement ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)). Les procédures, les propriétés et les constantes non partagées ne répondent pas à cette exigence. En outre, s’il y a aucune variable non partagée et qu’un seul événement non partagé, cet événement ne peut pas être un `Custom` événement.  
  
 **ID d’erreur :** BC30941  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Définissez au moins une variable ou un événement qui n’est pas `Shared`. Si vous définissez un seul événement, il doit être non personnalisés ainsi que non partagée.  
  
## <a name="see-also"></a>Voir aussi  
 [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
 [Guide pratique : déclarer une structure](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
