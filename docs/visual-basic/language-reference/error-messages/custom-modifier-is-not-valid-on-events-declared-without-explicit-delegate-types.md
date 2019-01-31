---
title: Le modificateur 'Custom' n'est pas valide pour les événements déclarés sans types délégués explicites
ms.date: 07/20/2015
f1_keywords:
- vbc31122
- bc31122
helpviewer_keywords:
- BC31122
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
ms.openlocfilehash: c1b57ccdaa9e04c837ecf7572bc164683a934b2d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273515"
---
# <a name="custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a>Le modificateur 'Custom' n'est pas valide pour les événements déclarés sans types délégués explicites
Contrairement à un événement non personnalisé, un `Custom Event` déclaration nécessite un `As` clause après le nom de l’événement qui spécifie explicitement le type de délégué pour l’événement.  
  
 Les événements non personnalisés peuvent être défini avec un `As` clause et explicite type délégué, ou avec un paramètre de liste immédiatement après le nom de l’événement.  
  
 **ID d’erreur :** BC31122  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Définissez un délégué avec la même liste de paramètres que l’événement personnalisé.  
  
     Par exemple, si le `Custom Event` a été défini par `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, puis le délégué correspondant est la suivante.  
  
     [!code-vb[VbVbalrEventError#18](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_1.vb)]  
  
2.  Remplacez la liste des paramètres de l’événement personnalisé avec un `As` clause qui spécifie le type de délégué.  
  
     Poursuivre avec l’exemple, `Custom Event` déclaration réécrite comme suit.  
  
     [!code-vb[VbVbalrEventError#19](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_2.vb)]  
  
## <a name="example"></a>Exemple  
 Cet exemple déclare un `Custom Event` et spécifie le texte requis `As` clause avec un type délégué.  
  
 [!code-vb[VbVbalrEventError#2](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types_3.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
