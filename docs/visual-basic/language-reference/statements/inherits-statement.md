---
title: Inherits, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Inherits
- Inherits
helpviewer_keywords:
- Inherits statement [Visual Basic]
- Inherits statement [Visual Basic], syntax
ms.assetid: 9e6fe042-9af3-4341-8093-fc3537770cf2
ms.openlocfilehash: 4a98ada39a04730b46f40fe139e72d1855d9b067
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43463865"
---
# <a name="inherits-statement"></a>Inherits Statement
Provoque la classe en cours ou interface hérite des attributs, variables, propriétés, procédures et événements d’une autre classe ou ensemble d’interfaces.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Inherits basetypenames  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`basetypenames`|Obligatoire. Le nom de la classe à partir de laquelle cette classe est dérivée.<br /><br /> - ou -<br /><br /> Les noms des interfaces à partir de laquelle cette interface est dérivée. Utilisez des virgules pour séparer plusieurs noms.|  
  
## <a name="remarks"></a>Notes  
 Si utilisé, le `Inherits` instruction doit être la première ligne non vide, sans commentaire dans une définition de classe ou interface. Elle doit suivre immédiatement le `Class` ou `Interface` instruction.  
  
 Vous pouvez utiliser `Inherits` uniquement dans une classe ou interface. Cela signifie que le contexte de déclaration pour un héritage ne peut pas être un fichier source, espace de noms, de structure, module, procédure ou bloc.  
  
## <a name="rules"></a>Règles  
  
-   **Héritage de classes.** Si une classe utilise le `Inherits` instruction, vous pouvez spécifier qu’une seule classe de base.  
  
     Une classe ne peut pas hériter d’une classe imbriquée dans celui-ci.  
  
-   **Héritage de l’interface.** Si une interface utilise le `Inherits` instruction, vous pouvez spécifier une ou plusieurs interfaces de base. Vous pouvez hériter de deux interfaces même si chacune définit un membre portant le même nom. Si vous procédez ainsi, le code d’implémentation doit utiliser qualification de noms pour spécifier le membre qu’il implémente.  
  
     Une interface ne peut pas hériter d’une autre interface avec un niveau d’accès plus restrictif. Par exemple, un `Public` interface ne peut pas hériter d’un `Friend` interface.  
  
     Une interface ne peut pas hériter d’une interface imbriquée dans celui-ci.  
  
 Un exemple d’héritage de classe dans le .NET Framework est la <xref:System.ArgumentException> (classe), qui hérite de la <xref:System.SystemException> classe. Cela fournit à <xref:System.ArgumentException> toutes les propriétés prédéfinies et les procédures requises par les exceptions système, telles que la <xref:System.Exception.Message%2A> propriété et la <xref:System.Exception.ToString%2A> (méthode).  
  
 Un exemple d’héritage d’interface dans le .NET Framework est la <xref:System.Collections.ICollection> interface qui hérite de la <xref:System.Collections.IEnumerable> interface. Cela entraîne <xref:System.Collections.ICollection> d’hériter de la définition de l’énumérateur permettant de parcourir une collection.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Inherits` instruction pour montrer comment une classe nommée `thisClass` peut hériter de tous les membres d’une classe de base nommée `anotherClass`.  
  
 [!code-vb[VbVbalrStatements#37](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/inherits-statement_1.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre l’héritage de plusieurs interfaces.  
  
 [!code-vb[VbVbalrStatements#38](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/inherits-statement_2.vb)]  
  
 L’interface nommée `thisInterface` inclut désormais toutes les définitions dans le <xref:System.IComparable>, <xref:System.IDisposable>, et <xref:System.IFormattable> interfaces que les membres hérités fournissent respectivement pour comparaison spécifique au type de deux objets, libérer les ressources allouées. et l’expression de la valeur d’un objet comme un `String`. Une classe qui implémente `thisInterface` doit implémenter chaque membre de chaque interface de base.  
  
## <a name="see-also"></a>Voir aussi  
 [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md)  
 [NotInheritable](../../../visual-basic/language-reference/modifiers/notinheritable.md)  
 [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)  
 [Éléments fondamentaux de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)  
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
