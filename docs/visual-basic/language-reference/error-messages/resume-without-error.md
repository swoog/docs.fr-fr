---
title: Reprendre sans gestion d'erreur
ms.date: 07/20/2015
f1_keywords:
- vbrID20
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
ms.openlocfilehash: 61332486b20af66af24eac06b222a38353578c16
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62055158"
---
# <a name="resume-without-error"></a><span data-ttu-id="88ebf-102">Reprendre sans gestion d'erreur</span><span class="sxs-lookup"><span data-stu-id="88ebf-102">Resume without error</span></span>
<span data-ttu-id="88ebf-103">Un `Resume` instruction est apparue en dehors du code de gestion des erreurs ou le code est passé dans un gestionnaire d’erreurs, même si aucune erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="88ebf-103">A `Resume` statement appeared outside error-handling code, or the code jumped into an error handler even though there was no error.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="88ebf-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="88ebf-104">To correct this error</span></span>  
  
1. <span data-ttu-id="88ebf-105">Déplacer le `Resume` instruction dans un gestionnaire d’erreurs, ou supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="88ebf-105">Move the `Resume` statement into an error handler, or delete it.</span></span>  
  
2. <span data-ttu-id="88ebf-106">Passages à des étiquettes ne peut pas se produire entre procédures, recherchez dans la procédure pour l’étiquette qui identifie le Gestionnaire d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="88ebf-106">Jumps to labels cannot occur across procedures, so search the procedure for the label that identifies the error handler.</span></span> <span data-ttu-id="88ebf-107">Si vous trouvez une étiquette dupliquée spécifiée comme cible d’un `GoTo` instruction qui n’est pas un `On Error GoTo` instruction, modifiez l’étiquette de ligne pour correspondre à la cible attendue.</span><span class="sxs-lookup"><span data-stu-id="88ebf-107">If you find a duplicate label specified as the target of a `GoTo` statement that isn't an `On Error GoTo` statement, change the line label to agree with its intended target.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88ebf-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88ebf-108">See also</span></span>

- [<span data-ttu-id="88ebf-109">Resume (instruction)</span><span class="sxs-lookup"><span data-stu-id="88ebf-109">Resume Statement</span></span>](../../../visual-basic/language-reference/statements/resume-statement.md)
- [<span data-ttu-id="88ebf-110">On Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="88ebf-110">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)
