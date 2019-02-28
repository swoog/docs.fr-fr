---
title: 'Procédure : Déterminer la chaîne associée à une valeur d’énumération (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic]
- strings [Visual Basic], enumeration values
- values [Visual Basic], enumeration members
ms.assetid: 9253e7c8-579c-49a2-8f26-392b20ea99eb
ms.openlocfilehash: 74dff310ccba0bebcf96576d769bf50420ca7397
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56971687"
---
# <a name="how-to-determine-the-string-associated-with-an-enumeration-value-visual-basic"></a><span data-ttu-id="fc448-102">Procédure : Déterminer la chaîne associée à une valeur d’énumération (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fc448-102">How to: Determine the String Associated with an Enumeration Value (Visual Basic)</span></span>
<span data-ttu-id="fc448-103">Le <xref:System.Enum.GetValues%2A> et <xref:System.Enum.GetNames%2A> méthodes permettent de déterminer les chaînes et les valeurs associées aux membres de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="fc448-103">The <xref:System.Enum.GetValues%2A> and <xref:System.Enum.GetNames%2A> methods allow you to determine the strings and values associated with enumeration members.</span></span>  
  
### <a name="to-determine-the-string-associated-with-an-enumeration"></a><span data-ttu-id="fc448-104">Pour déterminer la chaîne associée à une énumération</span><span class="sxs-lookup"><span data-stu-id="fc448-104">To determine the string associated with an enumeration</span></span>  
  
-   <span data-ttu-id="fc448-105">Utilisez le <xref:System.Enum.GetNames%2A> méthode pour récupérer les chaînes associées aux membres de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="fc448-105">Use the <xref:System.Enum.GetNames%2A> method to retrieve the strings associated with the enumeration members.</span></span> <span data-ttu-id="fc448-106">Cet exemple déclare une énumération, `flavorEnum`, puis utilise le <xref:System.Enum.GetNames%2A> méthode pour afficher les chaînes associées à chaque membre.</span><span class="sxs-lookup"><span data-stu-id="fc448-106">This example declares an enumeration, `flavorEnum`, then uses the <xref:System.Enum.GetNames%2A> method to display the strings associated with each member.</span></span>  
  
     [!code-vb[VbEnumsTask#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="fc448-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc448-107">See also</span></span>
- <xref:System.Enum.GetValues%2A>
- <xref:System.Enum.GetNames%2A>
- <xref:System.Enum>
- [<span data-ttu-id="fc448-108">Guide pratique pour Déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="fc448-108">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [<span data-ttu-id="fc448-109">Guide pratique pour Faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="fc448-109">How to: Refer to an Enumeration Member</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [<span data-ttu-id="fc448-110">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="fc448-110">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [<span data-ttu-id="fc448-111">Guide pratique pour Parcourir une énumération dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc448-111">How to: Iterate Through An Enumeration in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [<span data-ttu-id="fc448-112">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="fc448-112">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [<span data-ttu-id="fc448-113">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="fc448-113">Enum Statement</span></span>](../../../../visual-basic/language-reference/statements/enum-statement.md)
