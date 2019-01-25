---
title: Fonction &#39; &lt;nom_procédure&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code
ms.date: 07/20/2015
f1_keywords:
- bc42105
- vbc42105
helpviewer_keywords:
- BC42105
ms.assetid: b6929bf4-a365-4a70-8dc9-6b0fc09e1468
ms.openlocfilehash: b6cc5143aafb6c2554b183a1fc5fb3b1331ec5d0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552188"
---
# <a name="function-39ltprocedurenamegt39-doesn39t-return-a-value-on-all-code-paths"></a>Fonction &#39; &lt;nom_procédure&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code
Fonction '\<nom_procédure >' ne retourne pas une valeur pour tous les chemins de code. Une instruction 'Return' est-elle manquante ?  
  
 Un `Function` procédure a au moins un chemin d’accès possible via son code qui ne retourne pas de valeur.  
  
 Vous pouvez retourner une valeur à partir d’un `Function` procédure dans une des manières suivantes :  
  
-   Inclure la valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).  
  
-   Affectez la valeur pour le `Function` procédure nommez, puis effectuez une `Exit Function` instruction.  
  
-   Affectez la valeur pour le `Function` procédure nommez, puis effectuez la `End Function` instruction.  
  
 Si le contrôle passe à `Exit Function` ou `End Function` et vous n’avez pas affectés n’importe quelle valeur pour le nom de la procédure, la procédure retourne la valeur par défaut du type de retour de données. Pour plus d’informations, consultez « Comportement » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42105  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Vérifiez votre logique de flux de contrôle et assurez-vous que vous assignez une valeur avant chaque instruction qui provoque un retour.  
  
     Il est plus facile de garantir que chaque retour de la procédure retourne une valeur si vous utilisez toujours la `Return` instruction. Si vous le faites, la dernière instruction avant `End Function` doit être un `Return` instruction.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures Function](../../../visual-basic/programming-guide/language-features/procedures/function-procedures.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Page Compiler, Concepteur de projet (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)
