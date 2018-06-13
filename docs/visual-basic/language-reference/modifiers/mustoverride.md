---
title: MustOverride (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.MustOverride
- MustOverride
helpviewer_keywords:
- virtual elements [Visual Basic], pure
- elements [Visual Basic], pure virtual
- properties [Visual Basic], redefining
- procedures [Visual Basic], overriding
- overriding, MustOverride keyword
- procedures [Visual Basic], redefining
- pure virtual elements [Visual Basic]
- MustOverride keyword [Visual Basic]
- properties [Visual Basic], overriding
ms.assetid: 6e9d9ad6-bb64-433f-b32b-3ef84293bf96
ms.openlocfilehash: 5dabd90d29bc41d017436876af24a67fa87e8e17
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33599868"
---
# <a name="mustoverride-visual-basic"></a>MustOverride (Visual Basic)
Spécifie qu’une propriété ou procédure n’est pas implémentée dans cette classe et doit être substituée dans une classe dérivée, avant de pouvoir être utilisé.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser `MustOverride` uniquement dans une instruction de déclaration de propriété ou de procédure. La propriété ou procédure spécifie `MustOverride` doit être un membre d’une classe, et la classe doit être marquée [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md).  
  
## <a name="rules"></a>Règles  
  
-   **Déclaration incomplète.** Lorsque vous spécifiez `MustOverride`, vous ne fournissez pas de lignes supplémentaires de code pour la propriété ou procédure, pas même le `End Function`, `End Property`, ou `End Sub` instruction.  
  
-   **Modificateurs combinés.** Vous ne pouvez pas spécifier `MustOverride` avec `NotOverridable`, `Overridable`, ou `Shared` dans la même déclaration.  
  
-   **Occultation et substitution.** L'occultation et la substitution redéfinissent toutes les deux un élément hérité, mais il existe des différences importantes entre ces deux approches. Pour plus d’informations, consultez [occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).  
  
-   **Autres termes.** Un élément qui ne peut pas être utilisé sauf dans une substitution est parfois appelé un *pure virtuel* élément.  
  
 Le modificateur `MustOverride` peut être utilisé dans les contextes suivants :  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi  
 [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md)  
 [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)  
 [Overrides](../../../visual-basic/language-reference/modifiers/overrides.md)  
 [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md)  
 [Mots clés](../../../visual-basic/language-reference/keywords/index.md)  
 [Occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
