---
title: Les instructions '#Region' et '#End Region' ne sont pas valides dans les expressions lambda multiligne de corps de méthode
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 2a2f5692518c6784dfc6e3be6302f1e8dcf2aaa7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55265569"
---
# <a name="region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a><span data-ttu-id="1c52e-102">Les instructions '#Region' et '#End Region' ne sont pas valides dans le corps des méthodes ou les expressions lambda multiligne</span><span class="sxs-lookup"><span data-stu-id="1c52e-102">'#Region' and '#End Region' statements are not valid within method bodies/multiline lambdas</span></span>
<span data-ttu-id="1c52e-103">Le `#Region` bloc doit être déclaré au niveau de la classe, module ou d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1c52e-103">The `#Region` block must be declared at a class, module, or namespace level.</span></span> <span data-ttu-id="1c52e-104">Une zone réductible peut inclure une ou plusieurs procédures, mais il ne peut pas commencer ou se terminer à l’intérieur d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="1c52e-104">A collapsible region can include one or more procedures, but it cannot begin or end inside of a procedure.</span></span>  
  
 <span data-ttu-id="1c52e-105">**ID d’erreur :** BC32025</span><span class="sxs-lookup"><span data-stu-id="1c52e-105">**Error ID:** BC32025</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1c52e-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1c52e-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="1c52e-107">Assurez-vous que la procédure précédente est correctement terminée avec un `End Function` ou `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="1c52e-107">Ensure that the preceding procedure is properly terminated with an `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="1c52e-108">Vérifiez que le `#Region` et `#End Region` sont des directives dans le même bloc de code.</span><span class="sxs-lookup"><span data-stu-id="1c52e-108">Ensure that the `#Region` and `#End Region` directives are in the same code block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c52e-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c52e-109">See also</span></span>
- [<span data-ttu-id="1c52e-110">#Region (directive)</span><span class="sxs-lookup"><span data-stu-id="1c52e-110">#Region Directive</span></span>](../../../visual-basic/language-reference/directives/region-directive.md)
