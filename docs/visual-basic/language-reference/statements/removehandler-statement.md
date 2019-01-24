---
title: RemoveHandler, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.RemoveHandlerMethod
- vb.RemoveHandler
- RemoveHandler
helpviewer_keywords:
- RemoveHandler keyword [Visual Basic]
- RemoveHandler statement [Visual Basic]
ms.assetid: 647cd825-e877-4910-b4f1-8d168beebe6a
ms.openlocfilehash: 27cdd2753507c6fc4d5c5041607e2ccb425b81b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560618"
---
# <a name="removehandler-statement"></a>RemoveHandler, instruction
Supprime l’association entre un événement et un gestionnaire d’événements.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
RemoveHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`event`|Le nom de l’événement géré.|  
|`eventhandler`|Le nom de la procédure actuellement gérant l’événement.|  
  
## <a name="remarks"></a>Notes  
 Le `AddHandler` et `RemoveHandler` vous permettent de démarrer et arrêter la gestion des événements pour un événement spécifique à tout moment pendant l’exécution du programme.  
  
> [!NOTE]
>  Pour les événements personnalisés, le `RemoveHandler` instruction appelle de l’événement `RemoveHandler` accesseur. Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrEvents#17](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/removehandler-statement_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [AddHandler (instruction)](../../../visual-basic/language-reference/statements/addhandler-statement.md)
- [Handles](../../../visual-basic/language-reference/statements/handles-clause.md)
- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
