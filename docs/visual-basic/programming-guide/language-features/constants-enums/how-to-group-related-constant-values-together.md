---
title: 'Procédure : Regrouper des valeurs de constante connexes ensemble (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], constants
- constants [Visual Basic], grouping together
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
ms.openlocfilehash: a4f74e48cfdd5c0bc0f745d0f32eb39442f5bd83
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59333325"
---
# <a name="how-to-group-related-constant-values-together-visual-basic"></a><span data-ttu-id="fffd5-102">Procédure : Regrouper des valeurs de constante connexes ensemble (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fffd5-102">How to: Group Related Constant Values Together (Visual Basic)</span></span>
<span data-ttu-id="fffd5-103">Une énumération est la meilleure façon de regrouper des constantes connexes.</span><span class="sxs-lookup"><span data-stu-id="fffd5-103">An enumeration is the best way to group related constants together.</span></span> <span data-ttu-id="fffd5-104">Vous créez une énumération avec la `Enum` instruction dans la section des déclarations d’une classe ou un module.</span><span class="sxs-lookup"><span data-stu-id="fffd5-104">You create an enumeration with the `Enum` statement in the declarations section of a class or a module.</span></span> <span data-ttu-id="fffd5-105">Pour plus d'informations, voir [Procédure : Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="fffd5-105">For more information, see [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).</span></span>  
  
### <a name="to-group-related-constant-values"></a><span data-ttu-id="fffd5-106">Groupe les valeurs de constante connexes</span><span class="sxs-lookup"><span data-stu-id="fffd5-106">To group related constant values</span></span>  
  
1. <span data-ttu-id="fffd5-107">Écrivez une déclaration qui inclut un niveau d’accès de code, le `Enum` mot clé et un nom valide.</span><span class="sxs-lookup"><span data-stu-id="fffd5-107">Write a declaration that includes a code access level, the `Enum` keyword, and a valid name.</span></span> <span data-ttu-id="fffd5-108">Cet exemple crée la `Private` énumération, `temperatureValues`.</span><span class="sxs-lookup"><span data-stu-id="fffd5-108">This example creates the `Private` enumeration, `temperatureValues`.</span></span>  
  
     [!code-vb[VbEnumsTask#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#21)]  
  
2. <span data-ttu-id="fffd5-109">Définissez les constantes dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="fffd5-109">Define the constants in the enumeration.</span></span> <span data-ttu-id="fffd5-110">Cet exemple crée la `Public` énumération `temperatureValues` et assigne ses valeurs.</span><span class="sxs-lookup"><span data-stu-id="fffd5-110">This example creates the `Public` enumeration `temperatureValues` and assigns its values.</span></span>  
  
     [!code-vb[VbEnumsTask#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="fffd5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fffd5-111">See also</span></span>

- [<span data-ttu-id="fffd5-112">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="fffd5-112">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [<span data-ttu-id="fffd5-113">Procédure : faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="fffd5-113">How to: Refer to an Enumeration Member</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [<span data-ttu-id="fffd5-114">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="fffd5-114">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [<span data-ttu-id="fffd5-115">Vue d’ensemble des constantes</span><span class="sxs-lookup"><span data-stu-id="fffd5-115">Constants Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [<span data-ttu-id="fffd5-116">Constantes et types de données littérales</span><span class="sxs-lookup"><span data-stu-id="fffd5-116">Constant and Literal Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [<span data-ttu-id="fffd5-117">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="fffd5-117">Constants and Enumerations</span></span>](../../../../visual-basic/language-reference/constants-and-enumerations.md)
