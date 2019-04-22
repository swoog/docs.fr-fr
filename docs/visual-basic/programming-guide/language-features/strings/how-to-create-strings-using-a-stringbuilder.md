---
title: 'Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 00fefcc138164288d872cd339f165dc6ffc0131a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58834190"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a><span data-ttu-id="7fc26-102">Procédure : Créer des chaînes à l’aide de StringBuilder en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7fc26-102">How to: Create Strings Using a StringBuilder in Visual Basic</span></span>
<span data-ttu-id="7fc26-103">Cet exemple construit une longue chaîne à partir de plusieurs chaînes plus petites à l’aide de la <xref:System.Text.StringBuilder> classe.</span><span class="sxs-lookup"><span data-stu-id="7fc26-103">This example constructs a long string from many smaller strings using the <xref:System.Text.StringBuilder> class.</span></span> <span data-ttu-id="7fc26-104">Le <xref:System.Text.StringBuilder> classe est plus efficace que le `&=` opérateur pour concaténer plusieurs chaînes.</span><span class="sxs-lookup"><span data-stu-id="7fc26-104">The <xref:System.Text.StringBuilder> class is more efficient than the `&=` operator for concatenating many strings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7fc26-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="7fc26-105">Example</span></span>  
 <span data-ttu-id="7fc26-106">L’exemple suivant crée une instance de la <xref:System.Text.StringBuilder> classe, ajoute 1 000 chaînes à cette instance, puis retourne sa représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7fc26-106">The following example creates an instance of the <xref:System.Text.StringBuilder> class, appends 1,000 strings to that instance, and then returns its string representation.</span></span>  
  
 [!code-vb[VbVbalrStrings#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#70)]  
  
## <a name="see-also"></a><span data-ttu-id="7fc26-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fc26-107">See also</span></span>

- [<span data-ttu-id="7fc26-108">Utilisation de la classe StringBuilder</span><span class="sxs-lookup"><span data-stu-id="7fc26-108">Using the StringBuilder Class</span></span>](../../../../standard/base-types/stringbuilder.md)
- [<span data-ttu-id="7fc26-109">&= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="7fc26-109">&= Operator</span></span>](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [<span data-ttu-id="7fc26-110">Chaînes</span><span class="sxs-lookup"><span data-stu-id="7fc26-110">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
- [<span data-ttu-id="7fc26-111">Création de chaînes</span><span class="sxs-lookup"><span data-stu-id="7fc26-111">Creating New Strings</span></span>](../../../../standard/base-types/creating-new.md)
- [<span data-ttu-id="7fc26-112">Manipulation de chaînes</span><span class="sxs-lookup"><span data-stu-id="7fc26-112">Manipulating Strings</span></span>](../../../../standard/base-types/manipulating-strings.md)
