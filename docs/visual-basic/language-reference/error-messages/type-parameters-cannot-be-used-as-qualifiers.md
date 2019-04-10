---
title: Les paramètres de type ne peuvent pas être utilisés comme qualificateurs
ms.date: 07/20/2015
f1_keywords:
- vbc32098
- bc32098
helpviewer_keywords:
- BC32098
ms.assetid: bab05325-dde8-4621-a5f6-368b5b7b2d76
ms.openlocfilehash: ba7348ae50965ffcf2719b20934451916c8fa95a
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59296353"
---
# <a name="type-parameters-cannot-be-used-as-qualifiers"></a><span data-ttu-id="f6130-102">Les paramètres de type ne peuvent pas être utilisés comme qualificateurs</span><span class="sxs-lookup"><span data-stu-id="f6130-102">Type parameters cannot be used as qualifiers</span></span>
<span data-ttu-id="f6130-103">Un élément de programmation est qualifié avec une chaîne de qualification qui inclut un paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="f6130-103">A programming element is qualified with a qualification string that includes a type parameter.</span></span>  
  
 <span data-ttu-id="f6130-104">Un paramètre de type représente une exigence pour un type qui doit être fourni lorsque le type générique est construit.</span><span class="sxs-lookup"><span data-stu-id="f6130-104">A type parameter represents a requirement for a type that is to be supplied when the generic type is constructed.</span></span> <span data-ttu-id="f6130-105">Il ne représente pas un type défini spécifique.</span><span class="sxs-lookup"><span data-stu-id="f6130-105">It does not represent a specific defined type.</span></span> <span data-ttu-id="f6130-106">Une chaîne de qualification doit inclure uniquement les éléments qui sont définis au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="f6130-106">A qualification string must include only elements that are defined at compile time.</span></span>  
  
 <span data-ttu-id="f6130-107">Les instructions suivantes peuvent générer cette erreur.</span><span class="sxs-lookup"><span data-stu-id="f6130-107">The following statements can generate this error.</span></span>  
  
```  
Public Function checkText(Of c As System.Windows.Forms.Control)(  
    ByVal badText As String) As Boolean  
  
    Dim saveText As c.Text  
    ' Insert code to look for badText within saveText.  
End Function  
```  
  
 <span data-ttu-id="f6130-108">**ID d’erreur :** BC32098</span><span class="sxs-lookup"><span data-stu-id="f6130-108">**Error ID:** BC32098</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f6130-109">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f6130-109">To correct this error</span></span>  
  
1. <span data-ttu-id="f6130-110">Supprimez le paramètre de type de la chaîne de qualification ou remplacez-le par un type défini.</span><span class="sxs-lookup"><span data-stu-id="f6130-110">Remove the type parameter from the qualification string, or replace it with a defined type.</span></span>  
  
2. <span data-ttu-id="f6130-111">Si vous devez utiliser un type construit pour rechercher l’élément de programmation ne soient pas qualifiée, vous devez utiliser la logique de programme supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f6130-111">If you need to use a constructed type to locate the programming element being qualified, you must use additional program logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6130-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6130-112">See also</span></span>

- [<span data-ttu-id="f6130-113">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="f6130-113">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [<span data-ttu-id="f6130-114">Types génériques Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f6130-114">Generic Types in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="f6130-115">Type List</span><span class="sxs-lookup"><span data-stu-id="f6130-115">Type List</span></span>](../../../visual-basic/language-reference/statements/type-list.md)
