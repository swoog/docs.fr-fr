---
title: Les instructions '#Region' et '#End Region' ne sont pas valides dans les expressions lambda multiligne de corps de méthode
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: c41b95da7e3565ae7aaf332fe49361336e79f7c7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59303906"
---
# <a name="region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a>Les instructions '#Region' et '#End Region' ne sont pas valides dans le corps des méthodes ou les expressions lambda multiligne
Le `#Region` bloc doit être déclaré au niveau de la classe, module ou d’espace de noms. Une zone réductible peut inclure une ou plusieurs procédures, mais il ne peut pas commencer ou se terminer à l’intérieur d’une procédure.  
  
 **ID d’erreur :** BC32025  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Assurez-vous que la procédure précédente est correctement terminée avec un `End Function` ou `End Sub` instruction.  
  
2. Vérifiez que le `#Region` et `#End Region` sont des directives dans le même bloc de code.  
  
## <a name="see-also"></a>Voir aussi

- [#Region (directive)](../../../visual-basic/language-reference/directives/region-directive.md)
