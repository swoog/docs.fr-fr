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
ms.openlocfilehash: fa9a1942903dff6f673d87b67ebcad047a410425
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624780"
---
# <a name="stop-statement-visual-basic"></a><span data-ttu-id="8f49b-102">Stop, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8f49b-102">Stop Statement (Visual Basic)</span></span>
<span data-ttu-id="8f49b-103">Suspend l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8f49b-103">Suspends execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f49b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f49b-104">Syntax</span></span>  
  
```  
Stop  
```  
  
## <a name="remarks"></a><span data-ttu-id="8f49b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8f49b-105">Remarks</span></span>  
 <span data-ttu-id="8f49b-106">Vous pouvez placer `Stop` instructions n’importe où dans les procédures pour suspendre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8f49b-106">You can place `Stop` statements anywhere in procedures to suspend execution.</span></span> <span data-ttu-id="8f49b-107">À l’aide de la `Stop` instruction est similaire à la définition d’un point d’arrêt dans le code.</span><span class="sxs-lookup"><span data-stu-id="8f49b-107">Using the `Stop` statement is similar to setting a breakpoint in the code.</span></span>  
  
 <span data-ttu-id="8f49b-108">Le `Stop` instruction interrompt l’exécution, mais contrairement à `End`, il ne pas fermer tous les fichiers ou effacer toutes les variables, sauf si elle est placée dans un fichier exécutable compilé (.exe).</span><span class="sxs-lookup"><span data-stu-id="8f49b-108">The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8f49b-109">Si le `Stop` est rencontrée dans le code qui s’exécute en dehors de l’environnement de développement intégré (IDE), le débogueur est appelé.</span><span class="sxs-lookup"><span data-stu-id="8f49b-109">If the `Stop` statement is encountered in code that is running outside of the integrated development environment (IDE), the debugger is invoked.</span></span> <span data-ttu-id="8f49b-110">Cela est vrai quel que soit que le code a été compilé en mode débogage ou de la vente au détail.</span><span class="sxs-lookup"><span data-stu-id="8f49b-110">This is true regardless of whether the code was compiled in debug or retail mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f49b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f49b-111">Example</span></span>  
 <span data-ttu-id="8f49b-112">Cet exemple utilise le `Stop` instruction pour interrompre l’exécution à chaque itération du `For...Next` boucle.</span><span class="sxs-lookup"><span data-stu-id="8f49b-112">This example uses the `Stop` statement to suspend execution for each iteration through the `For...Next` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#56](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/stop-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="8f49b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f49b-113">See also</span></span>
- [<span data-ttu-id="8f49b-114">End (instruction)</span><span class="sxs-lookup"><span data-stu-id="8f49b-114">End Statement</span></span>](../../../visual-basic/language-reference/statements/end-statement.md)
