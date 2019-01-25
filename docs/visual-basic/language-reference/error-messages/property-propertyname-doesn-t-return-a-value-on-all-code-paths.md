---
title: Propriété &#39; &lt;propertyname&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code
ms.date: 07/20/2015
f1_keywords:
- bc42107
- vbc42107
helpviewer_keywords:
- BC42107
ms.assetid: 06800966-9c3b-4844-9f13-83ac95607d32
ms.openlocfilehash: b8059ebc9b6c1de685f2f04c3ee362ab8cf6d05e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611252"
---
# <a name="property-39ltpropertynamegt39-doesn39t-return-a-value-on-all-code-paths"></a>Propriété &#39; &lt;propertyname&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code
Propriété '\<nom_propriété >' ne retourne pas une valeur pour tous les chemins de code. Une exception de référence null peut se produire au moment de l'exécution lorsque le résultat est utilisé.  
  
 Une propriété `Get` procédure a au moins un chemin d’accès possible via son code qui ne retourne pas de valeur.  
  
 Vous pouvez retourner une valeur d’une propriété `Get` procédure dans une des manières suivantes :  
  
-   Affectez la valeur au nom de propriété, puis effectuez une `Exit Property` instruction.  
  
-   Assignez la valeur au nom de propriété, puis exécutez le `End Get` instruction.  
  
-   Inclure la valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).  
  
 Si le contrôle passe à `Exit Property` ou `End Get` et vous n’avez pas affectés n’importe quelle valeur au nom de propriété, le `Get` procédure retourne la valeur par défaut de la propriété type de données. Pour plus d’informations, consultez « Comportement » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42107  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Vérifiez votre logique de flux de contrôle et assurez-vous que vous assignez une valeur avant chaque instruction qui provoque un retour.  
  
     Il est plus facile de garantir que chaque retour de la procédure retourne une valeur si vous utilisez toujours la `Return` instruction. Si vous le faites, la dernière instruction avant `End Get` doit être un `Return` instruction.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures de propriété](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)
- [Get (instruction)](../../../visual-basic/language-reference/statements/get-statement.md)
