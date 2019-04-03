---
title: Fin d'instruction attendue
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: ab6a4a0e6736e2af9c1fa0dd170b6aa4c42d9e4a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817148"
---
# <a name="end-of-statement-expected"></a><span data-ttu-id="cfd87-102">Fin d'instruction attendue</span><span class="sxs-lookup"><span data-stu-id="cfd87-102">End of statement expected</span></span>
<span data-ttu-id="cfd87-103">L’instruction est syntaxiquement complète, mais un élément de programmation supplémentaire suit l’élément qui termine l’instruction.</span><span class="sxs-lookup"><span data-stu-id="cfd87-103">The statement is syntactically complete, but an additional programming element follows the element that completes the statement.</span></span> <span data-ttu-id="cfd87-104">Un terminateur de ligne est nécessaire à la fin de chaque instruction.</span><span class="sxs-lookup"><span data-stu-id="cfd87-104">A line terminator is required at the end of every statement.</span></span>
  
 <span data-ttu-id="cfd87-105">Un terminateur de ligne divise les caractères d’un fichier source Visual Basic en lignes.</span><span class="sxs-lookup"><span data-stu-id="cfd87-105">A line terminator divides the characters of a Visual Basic source file into lines.</span></span> <span data-ttu-id="cfd87-106">Exemples d’indicateurs de fin de ligne sont le Unicode chariot retour (& HD), le Unicode saut de ligne (& haute disponibilité), et Unicode retour chariot suivi du caractère de saut de ligne Unicode.</span><span class="sxs-lookup"><span data-stu-id="cfd87-106">Examples of line terminators are the Unicode carriage return character (&HD), the Unicode linefeed character (&HA), and the Unicode carriage return character followed by the Unicode linefeed character.</span></span> <span data-ttu-id="cfd87-107">Pour plus d’informations sur les indicateurs de fin de ligne, consultez le [spécification du langage Visual Basic](~/_vblang/spec/lexical-grammar.md#line-terminators).</span><span class="sxs-lookup"><span data-stu-id="cfd87-107">For more information about line terminators, see the [Visual Basic Language Specification](~/_vblang/spec/lexical-grammar.md#line-terminators).</span></span>
  
 <span data-ttu-id="cfd87-108">**ID d’erreur :** BC30205</span><span class="sxs-lookup"><span data-stu-id="cfd87-108">**Error ID:** BC30205</span></span>
  
## <a name="to-correct-this-error"></a><span data-ttu-id="cfd87-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="cfd87-109">To correct this error</span></span>
  
1.  <span data-ttu-id="cfd87-110">Vérifiez si deux instructions différentes ont été placées par inadvertance sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="cfd87-110">Check to see if two different statements have inadvertently been put on the same line.</span></span>
  
2.  <span data-ttu-id="cfd87-111">Insérer un terminateur de ligne après l’élément qui se termine l’instruction.</span><span class="sxs-lookup"><span data-stu-id="cfd87-111">Insert a line terminator after the element that completes the statement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfd87-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfd87-112">See also</span></span>

- [<span data-ttu-id="cfd87-113">Guide pratique pour diviser et combiner des instructions dans le code</span><span class="sxs-lookup"><span data-stu-id="cfd87-113">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [<span data-ttu-id="cfd87-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="cfd87-114">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
