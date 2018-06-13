---
title: 'Comment : valider des chaînes qui représentent des dates ou des heures (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 411c8517783421b2472c3e4aa77287f8252f179b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647860"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a><span data-ttu-id="1b1af-102">Comment : valider des chaînes qui représentent des dates ou des heures (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1b1af-102">How to: Validate Strings That Represent Dates or Times (Visual Basic)</span></span>
<span data-ttu-id="1b1af-103">Le code suivant exemple définit un `Boolean` valeur qui indique si une chaîne représente une date ou heure valide.</span><span class="sxs-lookup"><span data-stu-id="1b1af-103">The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1b1af-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1b1af-104">Example</span></span>  
 [!code-vb[VbVbcnRegEx#2](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/how-to-validate-strings-that-represent-dates-or-times_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1b1af-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="1b1af-105">Compiling the Code</span></span>  
 <span data-ttu-id="1b1af-106">Remplacez `("01/01/03")` et `"9:30 PM"` avec la date et l’heure que vous souhaitez valider.</span><span class="sxs-lookup"><span data-stu-id="1b1af-106">Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate.</span></span> <span data-ttu-id="1b1af-107">Vous pouvez remplacer la chaîne par une autre chaîne codée en dur, avec un `String` ou variable, avec une méthode qui retourne une chaîne, telle que `InputBox`.</span><span class="sxs-lookup"><span data-stu-id="1b1af-107">You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="1b1af-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="1b1af-108">Robust Programming</span></span>  
 <span data-ttu-id="1b1af-109">Utilisez cette méthode pour valider la chaîne avant d’essayer de convertir le `String` à un `DateTime` variable.</span><span class="sxs-lookup"><span data-stu-id="1b1af-109">Use this method to validate the string before trying to convert the `String` to a `DateTime` variable.</span></span> <span data-ttu-id="1b1af-110">En vérifiant tout d’abord la date ou l’heure, vous pouvez éviter de générer une exception au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b1af-110">By checking the date or time first, you can avoid generating an exception at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b1af-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b1af-111">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Information.IsDate%2A>  
 <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>  
 [<span data-ttu-id="1b1af-112">Validation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1b1af-112">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
