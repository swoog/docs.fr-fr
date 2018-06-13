---
title: Nombre non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 12d73b33e3c025b40c98d84e3507af7be1e1e91a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593601"
---
# <a name="ordinal-is-not-valid"></a><span data-ttu-id="ae682-102">Nombre non valide</span><span class="sxs-lookup"><span data-stu-id="ae682-102">Ordinal is not valid</span></span>
<span data-ttu-id="ae682-103">Votre appel à une bibliothèque de liens dynamiques (DLL) indiqué à utiliser un nombre au lieu d’un nom de procédure, à l’aide de la `#num` syntaxe.</span><span class="sxs-lookup"><span data-stu-id="ae682-103">Your call to a dynamic-link library (DLL) indicated to use a number instead of a procedure name, using the `#num` syntax.</span></span> <span data-ttu-id="ae682-104">Cette erreur a les causes possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae682-104">This error has the following possible causes:</span></span>  
  
-   <span data-ttu-id="ae682-105">Une tentative de convertir le `#num` expression à un nombre a échoué.</span><span class="sxs-lookup"><span data-stu-id="ae682-105">An attempt to convert the `#num` expression to an ordinal failed.</span></span>  
  
-   <span data-ttu-id="ae682-106">Le `#num` spécifié n’indique pas de fonction dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="ae682-106">The `#num` specified does not specify any function in the DLL.</span></span>  
  
-   <span data-ttu-id="ae682-107">Une bibliothèque de types possède une déclaration non valide, ce qui provoque une utilisation interne d’un nombre ordinal non valide.</span><span class="sxs-lookup"><span data-stu-id="ae682-107">A type library has an invalid declaration resulting in internal use of an invalid ordinal number.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ae682-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="ae682-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="ae682-109">Assurez-vous que l’expression représente un nombre valide ou appelez la procédure par nom.</span><span class="sxs-lookup"><span data-stu-id="ae682-109">Make sure the expression represents a valid number, or call the procedure by name.</span></span>  
  
2.  <span data-ttu-id="ae682-110">Assurez-vous que `#num` identifie une fonction valide dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="ae682-110">Make sure `#num` identifies a valid function in the DLL.</span></span>  
  
3.  <span data-ttu-id="ae682-111">Isoler la cause du problème en supprimant le code de l’appel de procédure.</span><span class="sxs-lookup"><span data-stu-id="ae682-111">Isolate the procedure call causing the problem by commenting out the code.</span></span> <span data-ttu-id="ae682-112">Écrire un `Declare` instruction de la procédure et signalez le problème au fournisseur de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="ae682-112">Write a `Declare` statement for the procedure, and report the problem to the type library vendor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae682-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae682-113">See Also</span></span>  
 [<span data-ttu-id="ae682-114">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="ae682-114">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
