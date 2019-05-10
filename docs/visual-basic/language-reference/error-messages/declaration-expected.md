---
title: Déclaration attendue
ms.date: 07/20/2015
f1_keywords:
- vbc30188
- bc30188
helpviewer_keywords:
- BC30188
ms.assetid: da6b1df3-fe6b-4415-88e6-0977e5189e0b
ms.openlocfilehash: e6f8bf2b4ce9789a1715971b8262bdd162ba8035
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64619531"
---
# <a name="declaration-expected"></a><span data-ttu-id="0b640-102">Déclaration attendue</span><span class="sxs-lookup"><span data-stu-id="0b640-102">Declaration expected</span></span>
<span data-ttu-id="0b640-103">Une instruction non déclarative, comme une assignation ou une instruction de boucle, se trouve en dehors de toute procédure.</span><span class="sxs-lookup"><span data-stu-id="0b640-103">A nondeclarative statement, such as an assignment or loop statement, occurs outside any procedure.</span></span> <span data-ttu-id="0b640-104">Seules les déclarations sont autorisées en dehors des procédures.</span><span class="sxs-lookup"><span data-stu-id="0b640-104">Only declarations are allowed outside procedures.</span></span>  
  
 <span data-ttu-id="0b640-105">Vous pouvez également un élément de programmation est déclaré sans mot clé de déclaration, tel que `Dim` ou `Const`.</span><span class="sxs-lookup"><span data-stu-id="0b640-105">Alternatively, a programming element is declared without a declaration keyword such as `Dim` or `Const`.</span></span>  
  
 <span data-ttu-id="0b640-106">**ID d’erreur :** BC30188</span><span class="sxs-lookup"><span data-stu-id="0b640-106">**Error ID:** BC30188</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0b640-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0b640-107">To correct this error</span></span>  
  
- <span data-ttu-id="0b640-108">Déplacez l’instruction non déclarative vers le corps d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="0b640-108">Move the nondeclarative statement to the body of a procedure.</span></span>  
  
- <span data-ttu-id="0b640-109">Commencez la déclaration avec un mot clé de déclaration approprié.</span><span class="sxs-lookup"><span data-stu-id="0b640-109">Begin the declaration with an appropriate declaration keyword.</span></span>  
  
- <span data-ttu-id="0b640-110">Assurez-vous qu’un mot clé de déclaration n’est pas mal orthographié.</span><span class="sxs-lookup"><span data-stu-id="0b640-110">Ensure that a declaration keyword is not misspelled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b640-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b640-111">See also</span></span>

- [<span data-ttu-id="0b640-112">Procédures</span><span class="sxs-lookup"><span data-stu-id="0b640-112">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="0b640-113">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="0b640-113">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
