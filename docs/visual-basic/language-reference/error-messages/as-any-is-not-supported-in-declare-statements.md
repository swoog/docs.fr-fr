---
title: "'As Any' n'est pas pris en charge dans les instructions 'Declare'"
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: 3593f238c72cbcce911c72e42552d6a75188b628
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61935328"
---
# <a name="as-any-is-not-supported-in-declare-statements"></a>'As Any' n'est pas pris en charge dans les instructions 'Declare'
Le `Any` type de données a été utilisé avec `Declare` instructions dans Visual Basic 6.0 et versions antérieures pour permettre l’utilisation d’arguments pouvant contenir tout type de données. Prend en charge de Visual Basic surcharge, toutefois et rend ainsi la `Any` de type de données obsolète.  
  
 **ID d’erreur :** BC30828  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Déclarer des paramètres du type spécifique que vous souhaitez utiliser. par exemple.  
  
     [!code-vb[VbVbalrStatements#95](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class5.vb#95)]  
  
2. Utilisez le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour spécifier `As Any` lorsque `Void*` est attendu par la procédure appelée.  
  
     [!code-vb[VbVbalrStatements#96](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class5.vb#96)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [Procédure pas à pas : Appel des API Windows](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
- [Création de prototypes dans du code managé](../../../framework/interop/creating-prototypes-in-managed-code.md)
