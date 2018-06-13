---
title: Handles, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- Handles
- vb.Handles
helpviewer_keywords:
- Handles keyword [Visual Basic]
ms.assetid: 1b051c0e-f499-42f6-acb5-6f4f27824b40
ms.openlocfilehash: 15ce6a25aa5f403a2e55beb57b3693095743e52f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603715"
---
# <a name="handles-clause-visual-basic"></a>Handles, clause (Visual Basic)
Déclare qu'une procédure gère un événement spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
proceduredeclaration Handles eventlist  
```  
  
## <a name="parts"></a>Composants  
 `proceduredeclaration`  
 Déclaration de procédure `Sub` pour la procédure qui gérera l'événement.  
  
 `eventlist`  
 Liste des événements pour `proceduredeclaration` à gérer, séparés par des virgules. Les événements doivent être déclenchés par la classe de base pour la classe en cours ou par un objet déclaré à l'aide du mot clé `WithEvents`.  
  
## <a name="remarks"></a>Notes  
 Utilisez le mot clé `Handles` à la fin d'une déclaration de procédure pour que celle-ci gère les événements déclenchés par une variable objet déclarée à l'aide du mot clé `WithEvents` . Le mot clé `Handles` peut également être utilisé dans une classe dérivée pour gérer des événements à partir d'une classe de base.  
  
 Le mot clé `Handles` et l'instruction `AddHandler` vous permettent de spécifier que des procédures particulières gèrent des événements particuliers, mais il existe des différences. Utilisez le mot clé `Handles` quand vous définissez une procédure pour indiquer qu'elle gère un événement particulier. L'instruction `AddHandler` connecte les procédures aux événements au moment de l'exécution. Pour plus d’informations, consultez [AddHandler, instruction](../../../visual-basic/language-reference/statements/addhandler-statement.md).  
  
 Pour les événements personnalisés, l'application appelle l'accesseur `AddHandler` de l'événement quand elle ajoute la procédure comme gestionnaire d'événements. Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrEvents#2](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_1.vb)]  
  
 L'exemple suivant montre comment une classe dérivée peut utiliser l'instruction `Handles` pour gérer un événement à partir d'une classe de base.  
  
 [!code-vb[VbVbalrEvents#3](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_2.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant contient deux gestionnaires d’événements de bouton pour un **Application WPF** projet.  
  
 [!code-vb[VbVbalrEvents#41](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_3.vb)]  
  
## <a name="example"></a>Exemple  
 L'exemple suivant est équivalent à l'exemple précédent. La liste `eventlist` dans la clause `Handles` contient les événements pour les deux boutons.  
  
 [!code-vb[VbVbalrEvents#42](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_4.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)  
 [AddHandler (instruction)](../../../visual-basic/language-reference/statements/addhandler-statement.md)  
 [RemoveHandler (instruction)](../../../visual-basic/language-reference/statements/removehandler-statement.md)  
 [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)  
 [RaiseEvent (instruction)](../../../visual-basic/language-reference/statements/raiseevent-statement.md)  
 [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
