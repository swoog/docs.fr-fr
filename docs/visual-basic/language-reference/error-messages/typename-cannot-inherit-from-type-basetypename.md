---
title: '&#39;&lt;TypeName&gt; &#39; ne peut pas hériter &lt;type&gt; &#39; &lt;nom_type_base&gt; &#39; , car il étend l’accès de la base de &lt;type&gt; à l’extérieur de l’assembly'
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: f747b2b24f5fecc22b9e1fbc6ba26b634e9ead2c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="39lttypenamegt39-cannot-inherit-from-lttypegt-39ltbasetypenamegt39-because-it-expands-the-access-of-the-base-lttypegt-outside-the-assembly"></a>&#39;&lt;TypeName&gt; &#39; ne peut pas hériter &lt;type&gt; &#39; &lt;nom_type_base&gt; &#39; , car il étend l’accès de la base de &lt;type&gt; à l’extérieur de l’assembly
Une classe ou interface hérite d’une classe de base ou interface, mais ne comporte un niveau d’accès moins restrictif.  
  
 Par exemple, un `Public` interface hérite d’un `Friend` interface, ou un `Protected` hérite de la classe une `Private` classe. Cela expose la classe de base ou une interface pour accéder aux au-delà du niveau prévu.  
  
 **ID d’erreur :** BC30910  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Modifier le niveau d’accès de la classe dérivée ou une interface soit au moins aussi restrictif que celui de la classe de base ou l’interface.  
  
     - ou -  
  
-   Si le niveau d’accès moins restrictif, supprimez le `Inherits` instruction. Vous ne peut pas hériter d’une classe de base plus restreinte ou une interface.  
  
## <a name="see-also"></a>Voir aussi  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
 [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [Inherits (instruction)](../../../visual-basic/language-reference/statements/inherits-statement.md)  
 [Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
