---
title: '&#39;&lt;MemberName&gt; &#39; ne peut pas exposer le type &#39; &lt;typename&gt; &#39; en dehors du projet via &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30909
- vbc30909
helpviewer_keywords:
- BC30909
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
ms.openlocfilehash: 36add48ebee2d1804921eeeec0b59cdd4cbafecc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588091"
---
# <a name="39ltmembernamegt39-cannot-expose-type-39lttypenamegt39-outside-the-project-through-ltcontainertypegt-39ltcontainertypenamegt39"></a>&#39;&lt;MemberName&gt; &#39; ne peut pas exposer le type &#39; &lt;typename&gt; &#39; en dehors du projet via &lt;containertype&gt; &#39; &lt;containertypename&gt;&#39;
Une variable, un paramètre de procédure ou un retour de fonction est exposé à l’extérieur de son conteneur, mais il est déclaré comme un type qui ne doit pas être exposé en dehors du conteneur.  
  
 Le squelette du code suivant illustre une situation qui génère cette erreur.  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 Un type qui est déclaré `Protected`, `Friend`, `Protected Friend`, ou `Private` est destiné à l’accès à l’extérieur de son contexte de déclaration est limité. L’utiliser comme données de type d’une variable avec un accès moins limité nuit à cet objectif. Dans le code squelette précédent, `exposedVar` est `Public` et expose `privateClass` au code que vous ne devez pas y accéder.  
  
 **ID d’erreur :** BC30909  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Modifier le niveau d’accès de la variable, un paramètre de procédure ou une fonction de retour pour être au moins aussi restrictif que le niveau d’accès de son type de données.  
  
## <a name="see-also"></a>Voir aussi  
 [Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
