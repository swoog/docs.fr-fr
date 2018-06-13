---
title: Valeur de type &#39;type1&#39; ne peut pas être converti en &#39;type2&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc31194
- bc31194
helpviewer_keywords:
- BC31194
ms.assetid: 03d50c31-addd-4c90-9c53-725b84f9782e
ms.openlocfilehash: 9e59d3bc5e2bfca3628248d08ffc475334d4da79
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602754"
---
# <a name="value-of-type-39type139-cannot-be-converted-to-39type239"></a><span data-ttu-id="33ccb-102">Valeur de type &#39;type1&#39; ne peut pas être converti en &#39;type2&#39;</span><span class="sxs-lookup"><span data-stu-id="33ccb-102">Value of type &#39;type1&#39; cannot be converted to &#39;type2&#39;</span></span>
<span data-ttu-id="33ccb-103">Valeur de type 'type1' ne peut pas être convertie en 'type2'.</span><span class="sxs-lookup"><span data-stu-id="33ccb-103">Value of type 'type1' cannot be converted to 'type2'.</span></span> <span data-ttu-id="33ccb-104">Vous pouvez utiliser la propriété 'Value' pour obtenir la valeur de chaîne du premier élément de '\<parentElement >'.</span><span class="sxs-lookup"><span data-stu-id="33ccb-104">You can use the 'Value' property to get the string value of the first element of '\<parentElement>'.</span></span>  
  
 <span data-ttu-id="33ccb-105">Une tentative de conversion implicite d’un littéral XML vers un type spécifique a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="33ccb-105">An attempt has been made to implicitly cast an XML literal to a specific type.</span></span> <span data-ttu-id="33ccb-106">Le littéral XML ne peut pas être implicitement converti vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="33ccb-106">The XML literal cannot be implicitly cast to the specified type.</span></span>  
  
 <span data-ttu-id="33ccb-107">**ID d’erreur :** BC31194</span><span class="sxs-lookup"><span data-stu-id="33ccb-107">**Error ID:** BC31194</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="33ccb-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="33ccb-108">To correct this error</span></span>  
  
-   <span data-ttu-id="33ccb-109">Utilisez la propriété `Value` du littéral XML pour faire référence à sa valeur comme une `String`.</span><span class="sxs-lookup"><span data-stu-id="33ccb-109">Use the `Value` property of the XML literal to reference its value as a `String`.</span></span> <span data-ttu-id="33ccb-110">Utilisez la fonction `CType` , une autre fonction de conversion de type, ou la classe <xref:System.Convert> pour effectuer un cast de la valeur vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="33ccb-110">Use the `CType` function, another type conversion function, or the <xref:System.Convert> class to cast the value as the specified type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33ccb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33ccb-111">See Also</span></span>  
 <xref:System.Convert>  
 [<span data-ttu-id="33ccb-112">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="33ccb-112">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)  
 [<span data-ttu-id="33ccb-113">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="33ccb-113">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)  
 [<span data-ttu-id="33ccb-114">XML</span><span class="sxs-lookup"><span data-stu-id="33ccb-114">XML</span></span>](../../../visual-basic/programming-guide/language-features/xml/index.md)
