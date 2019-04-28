---
title: Fin d'instruction attendue
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: 1ce5c793a09df34ac17e70e3253e98108bf76fb8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803317"
---
# <a name="end-of-statement-expected"></a><span data-ttu-id="0e0e8-102">Fin d'instruction attendue</span><span class="sxs-lookup"><span data-stu-id="0e0e8-102">End of statement expected</span></span>
<span data-ttu-id="0e0e8-103">L’instruction est syntaxiquement complète, mais un élément de programmation supplémentaire suit l’élément qui termine l’instruction.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-103">The statement is syntactically complete, but an additional programming element follows the element that completes the statement.</span></span> <span data-ttu-id="0e0e8-104">Un terminateur de ligne est nécessaire à la fin de chaque instruction.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-104">A line terminator is required at the end of every statement.</span></span>
  
 <span data-ttu-id="0e0e8-105">Un terminateur de ligne divise les caractères d’un fichier source Visual Basic en lignes.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-105">A line terminator divides the characters of a Visual Basic source file into lines.</span></span> <span data-ttu-id="0e0e8-106">Exemples d’indicateurs de fin de ligne sont le Unicode chariot retour (& HD), le Unicode saut de ligne (& haute disponibilité), et Unicode retour chariot suivi du caractère de saut de ligne Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-106">Examples of line terminators are the Unicode carriage return character (&HD), the Unicode linefeed character (&HA), and the Unicode carriage return character followed by the Unicode linefeed character.</span></span> <span data-ttu-id="0e0e8-107">Pour plus d’informations sur les indicateurs de fin de ligne, consultez le [spécification du langage Visual Basic](~/_vblang/spec/lexical-grammar.md#line-terminators).</span><span class="sxs-lookup"><span data-stu-id="0e0e8-107">For more information about line terminators, see the [Visual Basic Language Specification](~/_vblang/spec/lexical-grammar.md#line-terminators).</span></span>
  
 <span data-ttu-id="0e0e8-108">**ID d’erreur :** BC30205</span><span class="sxs-lookup"><span data-stu-id="0e0e8-108">**Error ID:** BC30205</span></span>
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0e0e8-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0e0e8-109">To correct this error</span></span>
  
1. <span data-ttu-id="0e0e8-110">Vérifiez si deux instructions différentes ont été placées par inadvertance sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-110">Check to see if two different statements have inadvertently been put on the same line.</span></span>
  
2. <span data-ttu-id="0e0e8-111">Insérer un terminateur de ligne après l’élément qui se termine l’instruction.</span><span class="sxs-lookup"><span data-stu-id="0e0e8-111">Insert a line terminator after the element that completes the statement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e0e8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e0e8-112">See also</span></span>

- [<span data-ttu-id="0e0e8-113">Guide pratique pour diviser et combiner des instructions dans le code</span><span class="sxs-lookup"><span data-stu-id="0e0e8-113">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [<span data-ttu-id="0e0e8-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="0e0e8-114">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
