---
title: "Comment : créer des chaînes à l'aide de StringBuilder en Visual Basic"
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 49f3271d41e9e858c6ecafe1dde5330ebff767f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647730"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a><span data-ttu-id="4df30-102">Comment : créer des chaînes à l'aide de StringBuilder en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4df30-102">How to: Create Strings Using a StringBuilder in Visual Basic</span></span>
<span data-ttu-id="4df30-103">Cet exemple construit une longue chaîne à partir de plusieurs chaînes plus petites à l’aide de la <xref:System.Text.StringBuilder> classe.</span><span class="sxs-lookup"><span data-stu-id="4df30-103">This example constructs a long string from many smaller strings using the <xref:System.Text.StringBuilder> class.</span></span> <span data-ttu-id="4df30-104">Le <xref:System.Text.StringBuilder> classe est plus efficace que la `&=` opérateur pour concaténer plusieurs chaînes.</span><span class="sxs-lookup"><span data-stu-id="4df30-104">The <xref:System.Text.StringBuilder> class is more efficient than the `&=` operator for concatenating many strings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4df30-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="4df30-105">Example</span></span>  
 <span data-ttu-id="4df30-106">L’exemple suivant crée une instance de la <xref:System.Text.StringBuilder> (classe), ajoute 1 000 chaînes à cette instance, puis retourne sa représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4df30-106">The following example creates an instance of the <xref:System.Text.StringBuilder> class, appends 1,000 strings to that instance, and then returns its string representation.</span></span>  
  
 [!code-vb[VbVbalrStrings#70](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-strings-using-a-stringbuilder_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="4df30-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df30-107">See Also</span></span>  
 [<span data-ttu-id="4df30-108">Utilisation de la classe StringBuilder</span><span class="sxs-lookup"><span data-stu-id="4df30-108">Using the StringBuilder Class</span></span>](../../../../standard/base-types/stringbuilder.md)  
 [<span data-ttu-id="4df30-109">&= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="4df30-109">&= Operator</span></span>](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)  
 [<span data-ttu-id="4df30-110">Chaînes</span><span class="sxs-lookup"><span data-stu-id="4df30-110">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)  
 [<span data-ttu-id="4df30-111">Création de chaînes</span><span class="sxs-lookup"><span data-stu-id="4df30-111">Creating New Strings</span></span>](../../../../standard/base-types/creating-new.md)  
 [<span data-ttu-id="4df30-112">Manipulation de chaînes</span><span class="sxs-lookup"><span data-stu-id="4df30-112">Manipulating Strings</span></span>](../../../../standard/base-types/manipulating-strings.md)  
 <span data-ttu-id="4df30-113">[Exemples de chaînes](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4df30-113">[Strings Sample](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span></span>
