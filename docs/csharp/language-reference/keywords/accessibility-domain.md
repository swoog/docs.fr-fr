---
title: Domaine d'accessibilité - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- accessibility domain [C#]
ms.assetid: 8af779c1-275b-44be-a864-9edfbca71bcc
ms.openlocfilehash: 6028ec3184d7b9e61a62bf185fd37072636c6bc5
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235687"
---
# <a name="accessibility-domain-c-reference"></a>Domaine d'accessibilité (référence C#)
Le domaine d’accessibilité d’un membre indique dans quelles sections du programme un membre peut être référencé. Si le membre est imbriqué dans un autre type, son domaine d’accessibilité est déterminé à la fois par le [niveau d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md) du membre et par le domaine d’accessibilité du type conteneur immédiat.  
  
 Le domaine d’accessibilité d’un type de niveau supérieur est au moins le texte du programme du projet dans lequel il est déclaré. Cela signifie que le domaine inclut tous les fichiers sources de ce projet. Le domaine d’accessibilité d’un type imbriqué est au moins le texte de programme du type dans lequel il est déclaré. Autrement dit, le domaine est le corps du type, qui inclut tous les types imbriqués. Le domaine d’accessibilité d’un type imbriqué ne dépasse jamais celui du type conteneur. Ces concepts sont illustrés dans l’exemple suivant.  
  
## <a name="example"></a>Exemple  
 Cet exemple comporte un type de niveau supérieur, `T1`, et deux classes imbriquées, `M1` et `M2`. Les classes contiennent des champs qui ont des accessibilités déclarées différentes. Dans la méthode `Main`, un commentaire suit chaque instruction pour indiquer le domaine d’accessibilité de chaque membre. Notez que les instructions qui tentent de référencer les membres inaccessibles sont commentées. Si vous voulez examiner les erreurs du compilateur causées par une référence à un membre inaccessible, supprimez les commentaires un à un.  
  
[!code-csharp[csrefKeywordsModifiers#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#4)]
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Modificateurs d’accès](../../../csharp/language-reference/keywords/access-modifiers.md)  
- [Niveaux d’accessibilité](../../../csharp/language-reference/keywords/accessibility-levels.md)  
- [Limitations sur l’utilisation des niveaux d’accessibilité](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)  
- [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
- [public](../../../csharp/language-reference/keywords/public.md)  
- [private](../../../csharp/language-reference/keywords/private.md)  
- [protected](../../../csharp/language-reference/keywords/protected.md)  
- [internal](../../../csharp/language-reference/keywords/internal.md)
