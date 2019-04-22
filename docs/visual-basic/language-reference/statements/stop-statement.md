---
title: Stop, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Stop
helpviewer_keywords:
- breakpoints, Stop statements
- Stop statements [Visual Basic], syntax
- Stop statements [Visual Basic]
- execution [Visual Basic], suspending
- processing, interrupting
- processes, interrupting
- execution [Visual Basic], stopping
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
ms.openlocfilehash: 80d6734945324f3f517b256051486273f6b687ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58827989"
---
# <a name="stop-statement-visual-basic"></a><span data-ttu-id="515b4-102">Stop, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="515b4-102">Stop Statement (Visual Basic)</span></span>
<span data-ttu-id="515b4-103">Suspend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="515b4-103">Suspends execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="515b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="515b4-104">Syntax</span></span>  
  
```  
Stop  
```  
  
## <a name="remarks"></a><span data-ttu-id="515b4-105">Notes</span><span class="sxs-lookup"><span data-stu-id="515b4-105">Remarks</span></span>  
 <span data-ttu-id="515b4-106">Vous pouvez placer `Stop` instructions n’importe où dans les procédures pour suspendre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="515b4-106">You can place `Stop` statements anywhere in procedures to suspend execution.</span></span> <span data-ttu-id="515b4-107">À l’aide de la `Stop` instruction est similaire à la définition d’un point d’arrêt dans le code.</span><span class="sxs-lookup"><span data-stu-id="515b4-107">Using the `Stop` statement is similar to setting a breakpoint in the code.</span></span>  
  
 <span data-ttu-id="515b4-108">Le `Stop` instruction interrompt l’exécution, mais contrairement à `End`, il ne pas fermer tous les fichiers ou effacer toutes les variables, sauf si elle est placée dans un fichier exécutable compilé (.exe).</span><span class="sxs-lookup"><span data-stu-id="515b4-108">The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="515b4-109">Si le `Stop` est rencontrée dans le code qui s’exécute en dehors de l’environnement de développement intégré (IDE), le débogueur est appelé.</span><span class="sxs-lookup"><span data-stu-id="515b4-109">If the `Stop` statement is encountered in code that is running outside of the integrated development environment (IDE), the debugger is invoked.</span></span> <span data-ttu-id="515b4-110">Cela est vrai quel que soit que le code a été compilé en mode débogage ou de la vente au détail.</span><span class="sxs-lookup"><span data-stu-id="515b4-110">This is true regardless of whether the code was compiled in debug or retail mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="515b4-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="515b4-111">Example</span></span>  
 <span data-ttu-id="515b4-112">Cet exemple utilise le `Stop` instruction pour interrompre l’exécution à chaque itération du `For...Next` boucle.</span><span class="sxs-lookup"><span data-stu-id="515b4-112">This example uses the `Stop` statement to suspend execution for each iteration through the `For...Next` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#56](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#56)]  
  
## <a name="see-also"></a><span data-ttu-id="515b4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="515b4-113">See also</span></span>

- [<span data-ttu-id="515b4-114">End (instruction)</span><span class="sxs-lookup"><span data-stu-id="515b4-114">End Statement</span></span>](../../../visual-basic/language-reference/statements/end-statement.md)
