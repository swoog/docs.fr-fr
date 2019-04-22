---
title: 'Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- examples [Visual Basic], arrays
- examples [Visual Basic], Char data type
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
ms.openlocfilehash: 1f72cb86ffa38dc929062fab2f5592a781f2de27
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58831824"
---
# <a name="how-to-create-a-string-from-an-array-of-char-values-visual-basic"></a><span data-ttu-id="bd827-102">Procédure : Créer une chaîne à partir d’un tableau de valeurs Char (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bd827-102">How to: Create a String from An Array of Char Values (Visual Basic)</span></span>
<span data-ttu-id="bd827-103">Cet exemple crée la chaîne « abcd » à partir de différents caractères.</span><span class="sxs-lookup"><span data-stu-id="bd827-103">This example creates the string "abcd" from individual characters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd827-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd827-104">Example</span></span>  
 [!code-vb[VbVbalrStrings#61](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#61)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bd827-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bd827-105">Compiling the Code</span></span>  
 <span data-ttu-id="bd827-106">Cette méthode n’a aucune exigence particulière.</span><span class="sxs-lookup"><span data-stu-id="bd827-106">This method has no special requirements.</span></span>  
  
 <span data-ttu-id="bd827-107">La syntaxe `"a"c`, où un seul `c` suit un caractère unique entre guillemets, est utilisé pour créer un caractère littéral.</span><span class="sxs-lookup"><span data-stu-id="bd827-107">The syntax `"a"c`, where a single `c` follows a single character in quotation marks, is used to create a character literal.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="bd827-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="bd827-108">Robust Programming</span></span>  
 <span data-ttu-id="bd827-109">Les caractères null (équivalent à `Chr(0)`) dans la chaîne de produire des résultats inattendus lors de l’utilisation de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bd827-109">Null characters (equivalent to `Chr(0)`) in the string lead to unexpected results when using the string.</span></span> <span data-ttu-id="bd827-110">Le caractère null sera inclus dans la chaîne, mais pas les caractères qui suivent le caractère null seront affichera dans certaines situations.</span><span class="sxs-lookup"><span data-stu-id="bd827-110">The null character will be included with the string, but characters following the null character will not be displayed in some situations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd827-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd827-111">See also</span></span>

- <xref:System.String>
- [<span data-ttu-id="bd827-112">Char (type de données)</span><span class="sxs-lookup"><span data-stu-id="bd827-112">Char Data Type</span></span>](../../../../visual-basic/language-reference/data-types/char-data-type.md)
- [<span data-ttu-id="bd827-113">Types de données</span><span class="sxs-lookup"><span data-stu-id="bd827-113">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
