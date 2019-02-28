---
title: 'Procédure : Faire référence à un membre d’énumération (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], referring to
- values [Visual Basic], associating constant values with names
- enumeration members
- constants [Visual Basic], enumerated
ms.assetid: bbb5c3cc-7cdb-4814-8d6a-a6d91546ed1e
ms.openlocfilehash: e4f7ede26329ed97c65be8218be78aa40b1294e9
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976263"
---
# <a name="how-to-refer-to-an-enumeration-member-visual-basic"></a><span data-ttu-id="e4ad1-102">Procédure : Faire référence à un membre d’énumération (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e4ad1-102">How to: Refer to an Enumeration Member (Visual Basic)</span></span>
<span data-ttu-id="e4ad1-103">Les énumérations offrent un moyen pratique d’utiliser des ensembles de constantes connexes et d’associer des valeurs constantes avec des noms.</span><span class="sxs-lookup"><span data-stu-id="e4ad1-103">Enumerations provide a convenient way to work with sets of related constants and to associate constant values with names.</span></span> <span data-ttu-id="e4ad1-104">Par exemple, vous pouvez déclarer une énumération pour un ensemble de constantes entières associées aux jours de la semaine puis utiliser les noms des jours au lieu de leur valeur entière dans votre code.</span><span class="sxs-lookup"><span data-stu-id="e4ad1-104">For example, you can declare an enumeration for a set of integer constants associated with the days of the week, and then use the names of the days rather than their integer values in your code.</span></span>  
  
 <span data-ttu-id="e4ad1-105">Vous pouvez éviter d’utiliser des noms qualifiés complets avec la `Imports` instruction.</span><span class="sxs-lookup"><span data-stu-id="e4ad1-105">You can avoid using fully qualified names with the `Imports` statement.</span></span> <span data-ttu-id="e4ad1-106">Pour plus d’informations, consultez [énumérations et Qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span><span class="sxs-lookup"><span data-stu-id="e4ad1-106">For more information, see [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span></span>  
  
### <a name="to-refer-to-an-enumeration-member"></a><span data-ttu-id="e4ad1-107">Pour faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="e4ad1-107">To refer to an enumeration member</span></span>  
  
-   <span data-ttu-id="e4ad1-108">Qualifier le nom du membre de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e4ad1-108">Qualify the member name with the enumeration.</span></span> <span data-ttu-id="e4ad1-109">Par exemple, l’exemple suivant affecte la `Saturday` membre de la `FirstDayOfWeek` énumération à la variable `DayValue`.</span><span class="sxs-lookup"><span data-stu-id="e4ad1-109">For example, the following example assigns the `Saturday` member of the `FirstDayOfWeek` enumeration to the variable `DayValue`.</span></span>  
  
     [!code-vb[VbEnumsTask#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#19)]  
  
## <a name="see-also"></a><span data-ttu-id="e4ad1-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ad1-110">See also</span></span>
- [<span data-ttu-id="e4ad1-111">Guide pratique pour Déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="e4ad1-111">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [<span data-ttu-id="e4ad1-112">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="e4ad1-112">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [<span data-ttu-id="e4ad1-113">Guide pratique pour Parcourir une énumération dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e4ad1-113">How to: Iterate Through An Enumeration in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [<span data-ttu-id="e4ad1-114">Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération</span><span class="sxs-lookup"><span data-stu-id="e4ad1-114">How to: Determine the String Associated with an Enumeration Value</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [<span data-ttu-id="e4ad1-115">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="e4ad1-115">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
