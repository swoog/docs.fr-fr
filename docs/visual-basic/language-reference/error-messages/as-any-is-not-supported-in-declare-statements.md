---
title: '&#39;En tant que&#39; n’est pas pris en charge dans &#39;Declare&#39; instructions'
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: 34beaeb7178645d5a167d1b7b969bb3e4f500e1a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588224"
---
# <a name="39as-any39-is-not-supported-in-39declare39-statements"></a>&#39;En tant que&#39; n’est pas pris en charge dans &#39;Declare&#39; instructions
Le `Any` type de données a été utilisé avec `Declare` instructions dans Visual Basic 6.0 et versions antérieures pour permettre l’utilisation d’arguments qui peut contenir n’importe quel type de données. Visual Basic prend en charge la surcharge, toutefois et rend ainsi le `Any` de type de données obsolète.  
  
 **ID d’erreur :** BC30828  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarer des paramètres du type spécifique que vous souhaitez utiliser. par exemple.  
  
     [!code-vb[VbVbalrStatements#95](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_1.vb)]  
  
2.  Utilisez le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour spécifier `As Any` lorsque `Void*` est attendue par la procédure appelée.  
  
     [!code-vb[VbVbalrStatements#96](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [Procédure pas à pas : appel des API Windows](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
 [Création de prototypes dans du code managé](../../../framework/interop/creating-prototypes-in-managed-code.md)
