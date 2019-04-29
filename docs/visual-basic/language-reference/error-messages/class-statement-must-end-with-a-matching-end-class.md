---
title: Une instruction 'Class' doit se terminer par une 'End Class' correspondante
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 0619db618abd562bda86836bdd41bbcd6caee0f9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61649892"
---
# <a name="class-statement-must-end-with-a-matching-end-class"></a><span data-ttu-id="dbc95-102">Une instruction 'Class' doit se terminer par une 'End Class' correspondante</span><span class="sxs-lookup"><span data-stu-id="dbc95-102">'Class' statement must end with a matching 'End Class'</span></span>
<span data-ttu-id="dbc95-103">`Class` permet de lancer un `Class` bloquer ; il ne peut donc apparaître au début du bloc, avec une mise en correspondance `End Class` instruction fin du bloc.</span><span class="sxs-lookup"><span data-stu-id="dbc95-103">`Class` is used to initiate a `Class` block; hence it can only appear at the beginning of the block, with a matching `End Class` statement ending the block.</span></span> <span data-ttu-id="dbc95-104">Soit vous avez un redondant `Class` instruction, ou vous n’avez pas terminé votre `Class` bloc avec `End Class`.</span><span class="sxs-lookup"><span data-stu-id="dbc95-104">Either you have a redundant `Class` statement, or you have not ended your `Class` block with `End Class`.</span></span>  
  
 <span data-ttu-id="dbc95-105">**ID d’erreur :** BC30481</span><span class="sxs-lookup"><span data-stu-id="dbc95-105">**Error ID:** BC30481</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dbc95-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="dbc95-106">To correct this error</span></span>  
  
- <span data-ttu-id="dbc95-107">Recherchez et supprimez l’instruction `Class` inutile.</span><span class="sxs-lookup"><span data-stu-id="dbc95-107">Locate and remove the unnecessary `Class` statement.</span></span>  
  
- <span data-ttu-id="dbc95-108">Conclure le `Class` bloc avec une mise en correspondance `End Class`.</span><span class="sxs-lookup"><span data-stu-id="dbc95-108">Conclude the `Class` block with a matching `End Class`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbc95-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbc95-109">See also</span></span>

- [<span data-ttu-id="dbc95-110">Fin \<mot clé > instruction</span><span class="sxs-lookup"><span data-stu-id="dbc95-110">End \<keyword> Statement</span></span>](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [<span data-ttu-id="dbc95-111">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="dbc95-111">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
