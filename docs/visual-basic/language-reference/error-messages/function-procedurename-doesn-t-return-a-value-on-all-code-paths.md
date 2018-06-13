---
title: Fonction &#39; &lt;nom_procédure&gt; &#39; ne&#39;t retournent une valeur sur tous les chemins de code
ms.date: 07/20/2015
f1_keywords:
- bc42105
- vbc42105
helpviewer_keywords:
- BC42105
ms.assetid: b6929bf4-a365-4a70-8dc9-6b0fc09e1468
ms.openlocfilehash: 4c18c6229eb170e8a688aaa2734ae8fbfa081061
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33589982"
---
# <a name="function-39ltprocedurenamegt39-doesn39t-return-a-value-on-all-code-paths"></a>Fonction &#39; &lt;nom_procédure&gt; &#39; ne&#39;t retournent une valeur sur tous les chemins de code
Fonction '\<nom_procédure >' ne retourne pas une valeur pour tous les chemins de code. Une instruction 'Return' est-elle manquante ?  
  
 A `Function` procédure possède au moins un chemin possible du code qui ne retourne pas de valeur.  
  
 Vous pouvez retourner une valeur depuis une `Function` procédure dans une des manières suivantes :  
  
-   Inclure la valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).  
  
-   Assigner la valeur à la `Function` procédure nom, puis effectuez une `Exit Function` instruction.  
  
-   Assigner la valeur à la `Function` procédure nom, puis effectuez la `End Function` instruction.  
  
 Si le contrôle passe à `Exit Function` ou `End Function` et que vous n’avez pas affecté n’importe quelle valeur pour le nom de la procédure, la procédure retourne la valeur par défaut du type de données de retour. Pour plus d’informations, consultez « Comportement » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [configuration des avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42105  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Vérifiez votre logique de flux de contrôle et assurez-vous que vous assignez une valeur avant chaque instruction qui provoque un retour.  
  
     Il est plus facile de garantir que chaque retour de la procédure retourne une valeur si vous utilisez toujours la `Return` instruction. Dans ce cas, la dernière instruction avant `End Function` doit être un `Return` instruction.  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures Function](../../../visual-basic/programming-guide/language-features/procedures/function-procedures.md)  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
 [Page Compiler, Concepteur de projet (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)
