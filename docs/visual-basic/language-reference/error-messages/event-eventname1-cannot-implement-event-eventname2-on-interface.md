---
title: Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur interface &#39; &lt;interface&gt; &#39; car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas
ms.date: 07/20/2015
f1_keywords:
- vbc31423
- bc31423
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
ms.openlocfilehash: 024e260f12d3497d64f26e59521f016ad439ebb6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638209"
---
# <a name="event-39lteventname1gt39-cannot-implement-event-39lteventname2gt39-on-interface-39ltinterfacegt39-because-their-delegate-types-39ltdelegate1gt39-and-39ltdelegate2gt39-do-not-match"></a>Événement &#39; &lt;nom_événement1&gt; &#39; ne peut pas implémenter l’événement &#39; &lt;nom_événement2&gt; &#39; sur interface &#39; &lt;interface&gt; &#39; car leurs types délégués &#39; &lt;delegate1&gt; &#39; et &#39; &lt;delegate2&gt; &#39; ne correspondent pas
Visual Basic ne peut pas implémenter un événement, car le type de délégué de l’événement ne correspond pas au type de délégué de l’événement dans l’interface. Cette erreur peut se produire quand vous définissez plusieurs événements dans une interface et essayez ensuite de les implémenter ensemble avec le même événement. Un événement peut implémenter deux événements ou plus seulement si tous les événements implémentés sont déclarés à l’aide de la syntaxe `As` et s’ils spécifient le même type délégué.  
  
 **ID d’erreur :** BC31423  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Implémentez les événements séparément.  
  
     - ou -  
  
-   Définissez les événements dans l’interface à l’aide de la `As` syntaxe et spécifient le même type délégué.  
  
## <a name="see-also"></a>Voir aussi
- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
