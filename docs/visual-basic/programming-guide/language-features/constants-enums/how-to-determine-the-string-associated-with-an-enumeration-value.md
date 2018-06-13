---
title: "Comment : déterminer la chaîne associée à une valeur d'énumération (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic]
- strings [Visual Basic], enumeration values
- values [Visual Basic], enumeration members
ms.assetid: 9253e7c8-579c-49a2-8f26-392b20ea99eb
ms.openlocfilehash: c14ea61feba7d7d85f9a4fc377aefdd8fa240c45
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33651698"
---
# <a name="how-to-determine-the-string-associated-with-an-enumeration-value-visual-basic"></a><span data-ttu-id="2a9a3-102">Comment : déterminer la chaîne associée à une valeur d'énumération (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2a9a3-102">How to: Determine the String Associated with an Enumeration Value (Visual Basic)</span></span>
<span data-ttu-id="2a9a3-103">Le <xref:System.Enum.GetValues%2A> et <xref:System.Enum.GetNames%2A> méthodes permettent de déterminer les chaînes et les valeurs associées aux membres de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2a9a3-103">The <xref:System.Enum.GetValues%2A> and <xref:System.Enum.GetNames%2A> methods allow you to determine the strings and values associated with enumeration members.</span></span>  
  
### <a name="to-determine-the-string-associated-with-an-enumeration"></a><span data-ttu-id="2a9a3-104">Pour déterminer la chaîne associée à une énumération</span><span class="sxs-lookup"><span data-stu-id="2a9a3-104">To determine the string associated with an enumeration</span></span>  
  
-   <span data-ttu-id="2a9a3-105">Utilisez la <xref:System.Enum.GetNames%2A> méthode pour récupérer les chaînes associées aux membres de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2a9a3-105">Use the <xref:System.Enum.GetNames%2A> method to retrieve the strings associated with the enumeration members.</span></span> <span data-ttu-id="2a9a3-106">Cet exemple déclare une énumération, `flavorEnum`, puis utilise la <xref:System.Enum.GetNames%2A> méthode pour afficher les chaînes associées à chaque membre.</span><span class="sxs-lookup"><span data-stu-id="2a9a3-106">This example declares an enumeration, `flavorEnum`, then uses the <xref:System.Enum.GetNames%2A> method to display the strings associated with each member.</span></span>  
  
     [!code-vb[VbEnumsTask#2](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-determine-the-string-associated-with-an-enumeration-value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="2a9a3-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a9a3-107">See Also</span></span>  
 <xref:System.Enum.GetValues%2A>  
 <xref:System.Enum.GetNames%2A>  
 <xref:System.Enum>  
 [<span data-ttu-id="2a9a3-108">Comment : déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="2a9a3-108">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)  
 [<span data-ttu-id="2a9a3-109">Guide pratique : faire référence à un membre d’énumération</span><span class="sxs-lookup"><span data-stu-id="2a9a3-109">How to: Refer to an Enumeration Member</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)  
 [<span data-ttu-id="2a9a3-110">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="2a9a3-110">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [<span data-ttu-id="2a9a3-111">Comment : parcourir une énumération dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2a9a3-111">How to: Iterate Through An Enumeration in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)  
 [<span data-ttu-id="2a9a3-112">Quand utiliser une énumération</span><span class="sxs-lookup"><span data-stu-id="2a9a3-112">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)  
 [<span data-ttu-id="2a9a3-113">Enum (instruction)</span><span class="sxs-lookup"><span data-stu-id="2a9a3-113">Enum Statement</span></span>](../../../../visual-basic/language-reference/statements/enum-statement.md)
