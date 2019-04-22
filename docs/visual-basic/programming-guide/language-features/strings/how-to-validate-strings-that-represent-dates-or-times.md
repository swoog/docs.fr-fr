---
title: 'Procédure : Valider des chaînes qui représentent des Dates ou des heures (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: f24ff05e48327c21c02eb92b07db17266f743a80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58815228"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a><span data-ttu-id="efa7e-102">Procédure : Valider des chaînes qui représentent des Dates ou des heures (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="efa7e-102">How to: Validate Strings That Represent Dates or Times (Visual Basic)</span></span>
<span data-ttu-id="efa7e-103">Le code suivant exemple définit un `Boolean` valeur qui indique si une chaîne représente une date ou heure valide.</span><span class="sxs-lookup"><span data-stu-id="efa7e-103">The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="efa7e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="efa7e-104">Example</span></span>  
 [!code-vb[VbVbcnRegEx#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="efa7e-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="efa7e-105">Compiling the Code</span></span>  
 <span data-ttu-id="efa7e-106">Remplacez `("01/01/03")` et `"9:30 PM"` avec la date et l’heure que vous souhaitez valider.</span><span class="sxs-lookup"><span data-stu-id="efa7e-106">Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate.</span></span> <span data-ttu-id="efa7e-107">Vous pouvez remplacer la chaîne par une autre chaîne codée en dur, avec un `String` variable, ou avec une méthode qui retourne une chaîne, tel que `InputBox`.</span><span class="sxs-lookup"><span data-stu-id="efa7e-107">You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="efa7e-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="efa7e-108">Robust Programming</span></span>  
 <span data-ttu-id="efa7e-109">Utilisez cette méthode pour valider la chaîne avant d’essayer de convertir le `String` à un `DateTime` variable.</span><span class="sxs-lookup"><span data-stu-id="efa7e-109">Use this method to validate the string before trying to convert the `String` to a `DateTime` variable.</span></span> <span data-ttu-id="efa7e-110">En vérifiant la date ou heure tout d’abord, vous pouvez éviter de générer une exception au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="efa7e-110">By checking the date or time first, you can avoid generating an exception at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efa7e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efa7e-111">See also</span></span>

- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [<span data-ttu-id="efa7e-112">Validation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="efa7e-112">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
