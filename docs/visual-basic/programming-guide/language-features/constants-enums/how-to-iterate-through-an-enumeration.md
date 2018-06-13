---
title: "Comment : itérer au sein d'une énumération dans Visual Basic"
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [Visual Basic], iterating
- enumerations [Visual Basic], iterating
- ListBox control [Windows Forms], populating from an enumeration
ms.assetid: e5aa10eb-cfcd-4a3b-8e76-f06b8f2002be
ms.openlocfilehash: 06609d38c805e5f073a2f3a299ecc3aa7cf7be01
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646576"
---
# <a name="how-to-iterate-through-an-enumeration-in-visual-basic"></a><span data-ttu-id="7ff65-102">Comment : itérer au sein d'une énumération dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7ff65-102">How to: Iterate Through An Enumeration in Visual Basic</span></span>
<span data-ttu-id="7ff65-103">Les énumérations offrent un moyen pratique de travailler avec des ensembles de constantes connexes et d’associer des valeurs de constantes à des noms.</span><span class="sxs-lookup"><span data-stu-id="7ff65-103">Enumerations provide a convenient way to work with sets of related constants, and to associate constant values with names.</span></span> <span data-ttu-id="7ff65-104">Pour parcourir une énumération, vous pouvez le déplacer vers un tableau à l’aide de la <xref:System.Enum.GetValues%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7ff65-104">To iterate through an enumeration, you can move it into an array using the <xref:System.Enum.GetValues%2A> method.</span></span> <span data-ttu-id="7ff65-105">Vous pourriez également itérer d’une énumération à l’aide un `For...Each` instruction, à l’aide de la <xref:System.Enum.GetNames%2A> ou <xref:System.Enum.GetValues%2A> méthode pour extraire la valeur de chaîne ou numérique.</span><span class="sxs-lookup"><span data-stu-id="7ff65-105">You could also iterate through an enumeration using a `For...Each` statement, using the <xref:System.Enum.GetNames%2A> or <xref:System.Enum.GetValues%2A> method to extract the string or numeric value.</span></span>  
  
### <a name="to-iterate-through-an-enumeration"></a><span data-ttu-id="7ff65-106">Pour une itération au sein d’une énumération</span><span class="sxs-lookup"><span data-stu-id="7ff65-106">To iterate through an enumeration</span></span>  
  
-   <span data-ttu-id="7ff65-107">Déclarez un tableau et convertissez l’énumération avec la <xref:System.Enum.GetValues%2A> méthode avant de passer le tableau en tant que vous feriez toute autre variable.</span><span class="sxs-lookup"><span data-stu-id="7ff65-107">Declare an array and convert the enumeration to it with the <xref:System.Enum.GetValues%2A> method before passing the array as you would any other variable.</span></span> <span data-ttu-id="7ff65-108">L’exemple suivant affiche chaque membre de l’énumération <xref:Microsoft.VisualBasic.FirstDayOfWeek> itère l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7ff65-108">The following example displays each member of the enumeration <xref:Microsoft.VisualBasic.FirstDayOfWeek> as it iterates through the enumeration.</span></span>  
  
     [!code-vb[VbEnumsTask#7](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-iterate-through-an-enumeration_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="7ff65-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ff65-109">See Also</span></span>  
 [<span data-ttu-id="7ff65-110">Vue d’ensemble des énumérations</span><span class="sxs-lookup"><span data-stu-id="7ff65-110">Enumerations Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)  
 [<span data-ttu-id="7ff65-111">Comment : déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="7ff65-111">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)  
 [<span data-ttu-id="7ff65-112">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="7ff65-112">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)  
 [<span data-ttu-id="7ff65-113">Guide pratique : déterminer la chaîne associée à une valeur d’énumération</span><span class="sxs-lookup"><span data-stu-id="7ff65-113">How to: Determine the String Associated with an Enumeration Value</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)  
 [<span data-ttu-id="7ff65-114">Guide pratique : faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="7ff65-114">How to: Refer to an Enumeration Member</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)  
 [<span data-ttu-id="7ff65-115">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="7ff65-115">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [<span data-ttu-id="7ff65-116">Tableaux</span><span class="sxs-lookup"><span data-stu-id="7ff65-116">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
