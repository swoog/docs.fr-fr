---
title: Nombre non valide
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: f3207c2cc237ae22c295c2b3ed56f18601625226
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58822248"
---
# <a name="ordinal-is-not-valid"></a><span data-ttu-id="c0fff-102">Nombre non valide</span><span class="sxs-lookup"><span data-stu-id="c0fff-102">Ordinal is not valid</span></span>
<span data-ttu-id="c0fff-103">Votre appel à une bibliothèque de liens dynamiques (DLL) spécifie d’utiliser un nombre au lieu d’un nom de procédure, à l’aide de la `#num` syntaxe.</span><span class="sxs-lookup"><span data-stu-id="c0fff-103">Your call to a dynamic-link library (DLL) indicated to use a number instead of a procedure name, using the `#num` syntax.</span></span> <span data-ttu-id="c0fff-104">Cette erreur a les causes possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0fff-104">This error has the following possible causes:</span></span>  
  
-   <span data-ttu-id="c0fff-105">Une tentative de convertir le `#num` expression à un nombre a échoué.</span><span class="sxs-lookup"><span data-stu-id="c0fff-105">An attempt to convert the `#num` expression to an ordinal failed.</span></span>  
  
-   <span data-ttu-id="c0fff-106">Le `#num` spécifié ne spécifie pas de n’importe quelle fonction dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="c0fff-106">The `#num` specified does not specify any function in the DLL.</span></span>  
  
-   <span data-ttu-id="c0fff-107">Une bibliothèque de types a une déclaration non valide, ce qui entraîne une utilisation interne d’un nombre ordinal non valide.</span><span class="sxs-lookup"><span data-stu-id="c0fff-107">A type library has an invalid declaration resulting in internal use of an invalid ordinal number.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c0fff-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c0fff-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="c0fff-109">Assurez-vous que l’expression représente un nombre valide, ou appelez la procédure par nom.</span><span class="sxs-lookup"><span data-stu-id="c0fff-109">Make sure the expression represents a valid number, or call the procedure by name.</span></span>  
  
2.  <span data-ttu-id="c0fff-110">Assurez-vous que `#num` identifie une fonction valide dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="c0fff-110">Make sure `#num` identifies a valid function in the DLL.</span></span>  
  
3.  <span data-ttu-id="c0fff-111">Isoler la cause du problème en commentant le code de l’appel de procédure.</span><span class="sxs-lookup"><span data-stu-id="c0fff-111">Isolate the procedure call causing the problem by commenting out the code.</span></span> <span data-ttu-id="c0fff-112">Écrire un `Declare` instruction de la procédure et signaler le problème pour le fournisseur de bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="c0fff-112">Write a `Declare` statement for the procedure, and report the problem to the type library vendor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0fff-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0fff-113">See also</span></span>

- [<span data-ttu-id="c0fff-114">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="c0fff-114">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
