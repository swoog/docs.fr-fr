---
title: "Comment : faire référence à un membre d'énumération (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], referring to
- values [Visual Basic], associating constant values with names
- enumeration members
- constants [Visual Basic], enumerated
ms.assetid: bbb5c3cc-7cdb-4814-8d6a-a6d91546ed1e
ms.openlocfilehash: f995a0ef69c503360a5d709551a7f0ccfd67ce40
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646299"
---
# <a name="how-to-refer-to-an-enumeration-member-visual-basic"></a><span data-ttu-id="dca2b-102">Comment : faire référence à un membre d'énumération (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dca2b-102">How to: Refer to an Enumeration Member (Visual Basic)</span></span>
<span data-ttu-id="dca2b-103">Les énumérations offrent un moyen pratique d’utiliser des ensembles de constantes associées et pour associer des valeurs constantes avec des noms.</span><span class="sxs-lookup"><span data-stu-id="dca2b-103">Enumerations provide a convenient way to work with sets of related constants and to associate constant values with names.</span></span> <span data-ttu-id="dca2b-104">Par exemple, vous pouvez déclarer une énumération pour un ensemble de constantes entières associées aux jours de la semaine puis utiliser les noms des jours au lieu de leur valeur entière dans votre code.</span><span class="sxs-lookup"><span data-stu-id="dca2b-104">For example, you can declare an enumeration for a set of integer constants associated with the days of the week, and then use the names of the days rather than their integer values in your code.</span></span>  
  
 <span data-ttu-id="dca2b-105">Vous pouvez éviter d’utiliser des noms qualifiés complets avec la `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="dca2b-105">You can avoid using fully qualified names with the `Imports` statement.</span></span> <span data-ttu-id="dca2b-106">Pour plus d’informations, consultez [énumérations et Qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span><span class="sxs-lookup"><span data-stu-id="dca2b-106">For more information, see [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span></span>  
  
### <a name="to-refer-to-an-enumeration-member"></a><span data-ttu-id="dca2b-107">Pour faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="dca2b-107">To refer to an enumeration member</span></span>  
  
-   <span data-ttu-id="dca2b-108">Qualifier le nom du membre de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="dca2b-108">Qualify the member name with the enumeration.</span></span> <span data-ttu-id="dca2b-109">Par exemple, l’exemple suivant affecte la `Saturday` membre de la `FirstDayOfWeek` énumération à la variable `DayValue`.</span><span class="sxs-lookup"><span data-stu-id="dca2b-109">For example, the following example assigns the `Saturday` member of the `FirstDayOfWeek` enumeration to the variable `DayValue`.</span></span>  
  
     [!code-vb[VbEnumsTask#19](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-refer-to-an-enumeration-member_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="dca2b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca2b-110">See Also</span></span>  
 [<span data-ttu-id="dca2b-111">Comment : déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="dca2b-111">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)  
 [<span data-ttu-id="dca2b-112">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="dca2b-112">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [<span data-ttu-id="dca2b-113">Comment : parcourir une énumération dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dca2b-113">How to: Iterate Through An Enumeration in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)  
 [<span data-ttu-id="dca2b-114">Guide pratique : déterminer la chaîne associée à une valeur d’énumération</span><span class="sxs-lookup"><span data-stu-id="dca2b-114">How to: Determine the String Associated with an Enumeration Value</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)  
 [<span data-ttu-id="dca2b-115">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="dca2b-115">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
