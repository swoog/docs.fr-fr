---
title: Key (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AnonymousKey
helpviewer_keywords:
- anonymous types [Visual Basic], key
- Key [Visual Basic]
- Key keyword [Visual Basic]
ms.assetid: 7697a928-7d14-4430-a72a-c9e96e8d6c11
ms.openlocfilehash: e13a773f0b585a5c8803a77c7aaad441d90dfe75
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58842302"
---
# <a name="key-visual-basic"></a>Key (Visual Basic)
Le `Key` mot clé vous permet de spécifier le comportement des propriétés de types anonymes. Seules les propriétés que vous désignez comme propriétés de clé participent aux tests d’égalité entre les instances de type anonyme ou un calcul de valeurs de code de hachage. Les valeurs des propriétés de clé ne peut pas être modifiés.  
  
 Vous désignez une propriété d’un type anonyme comme propriété de clé en plaçant le mot clé `Key` devant sa déclaration dans la liste d’initialisation. Dans l’exemple suivant, `Airline` et `FlightNo` sont des propriétés de clé, mais `Gate` n’est pas.  
  
 [!code-vb[VbVbalrAnonymousTypes#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#26)]  
  
 Lorsqu’un nouveau type anonyme est créé, il hérite directement de <xref:System.Object>. Le compilateur substitue trois membres hérités : <xref:System.Object.Equals%2A>, <xref:System.Object.GetHashCode%2A>, et <xref:System.Object.ToString%2A>. Le code de substitution qui est généré pour <xref:System.Object.Equals%2A> et <xref:System.Object.GetHashCode%2A> est basée sur les propriétés de clé. S’il en existe aucune propriété de clé dans le type, <xref:System.Object.GetHashCode%2A> et <xref:System.Object.Equals%2A> ne sont pas remplacées.  
  
## <a name="equality"></a>Égalité  
 Deux instances de type anonyme sont égales si elles sont des instances du même type et si les valeurs de leurs propriétés de clé sont égales. Dans les exemples suivants, `flight2` est égal à `flight1` à partir de l’exemple précédent, car ce sont des instances du même anonyme type et ils ont des valeurs correspondantes pour leurs propriétés de clé. Toutefois, `flight3` n’est pas égal à `flight1` , car il a une valeur différente pour une propriété de clé, `FlightNo`. Instance `flight4` n’est pas du même type que `flight1` , car ils désignent des propriétés différentes comme propriétés de clé.  
  
 [!code-vb[VbVbalrAnonymousTypes#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#27)]  
  
 Si deux instances sont déclarées avec uniquement propriétés non-clé, identiques dans nom, type, ordre et valeur, les deux instances ne sont pas égaux. Une instance sans propriété de clé est uniquement égale à elle-même.  
  
 Pour plus d’informations sur les conditions sous lesquelles deux instances de type anonyme sont des instances du même type anonyme, consultez [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
  
## <a name="hash-code-calculation"></a>Calcul de Code de hachage  
 Comme <xref:System.Object.Equals%2A>, la fonction de hachage qui est définie dans <xref:System.Object.GetHashCode%2A> pour un type anonyme est basé sur les propriétés de clé du type. Les exemples suivants montrent l’interaction entre les propriétés de clé et le hachage des valeurs de code.  
  
 Les instances d’un type anonyme qui ont les mêmes valeurs pour toutes les propriétés de clé ont la même valeur de code de hachage, même si les propriétés non-clé n’ont pas de valeurs correspondantes. L’instruction suivante retourne `True`.  
  
 [!code-vb[VbVbalrAnonymousTypes#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#37)]  
  
 Les instances d’un type anonyme qui ont des valeurs différentes pour une ou plusieurs propriétés de clé ont des valeurs de code de hachage différente. L’instruction suivante retourne `False`.  
  
 [!code-vb[VbVbalrAnonymousTypes#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#38)]  
  
 Instances de types anonymes qui désignent des propriétés différentes comme propriétés de clé ne sont pas des instances du même type. Elles ont des valeurs de code de hachage différente même lorsque les noms et valeurs de toutes les propriétés sont identiques. L’instruction suivante retourne `False`.  
  
 [!code-vb[VbVbalrAnonymousTypes#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#39)]  
  
## <a name="read-only-values"></a>Valeurs en lecture seule  
 Les valeurs des propriétés de clé ne peut pas être modifiés. Par exemple, dans `flight1` dans les exemples précédents, le `Airline` et `FlightNo` champs sont en lecture seule, mais `Gate` peut être modifié.  
  
 [!code-vb[VbVbalrAnonymousTypes#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes/VB/Class2.vb#28)]  
  
## <a name="see-also"></a>Voir aussi

- [Définition du type anonyme](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md)
- [Guide pratique pour Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
- [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
