---
title: Attribut &#39; &lt;attributename&gt; &#39; ne peut pas être appliqué plusieurs fois
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: df97a4e391406661db98eb1c958c0e12e45b6c49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33584857"
---
# <a name="attribute-39ltattributenamegt39-cannot-be-applied-multiple-times"></a><span data-ttu-id="dc084-102">Attribut &#39; &lt;attributename&gt; &#39; ne peut pas être appliqué plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="dc084-102">Attribute &#39;&lt;attributename&gt;&#39; cannot be applied multiple times</span></span>
<span data-ttu-id="dc084-103">L’attribut peut uniquement être appliqué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="dc084-103">The attribute can only be applied once.</span></span> <span data-ttu-id="dc084-104">Le `AttributeUsage` attribut détermine si un attribut peut être appliqué plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="dc084-104">The `AttributeUsage` attribute determines whether an attribute can be applied more than once.</span></span>  
  
 <span data-ttu-id="dc084-105">**ID d’erreur :** BC30663</span><span class="sxs-lookup"><span data-stu-id="dc084-105">**Error ID:** BC30663</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dc084-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="dc084-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="dc084-107">Assurez-vous que l’attribut n’est appliqué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="dc084-107">Make sure the attribute is only applied once.</span></span>  
  
2.  <span data-ttu-id="dc084-108">Si vous utilisez des attributs personnalisés que vous avez développés, envisagez de modifier leur `AttributeUsage` attribut pour permettre l’utilisation d’attributs multiples, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="dc084-108">If you are using custom attributes you developed, consider changing their `AttributeUsage` attribute to allow multiple attribute usage, as with the following example.</span></span>  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dc084-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc084-109">See Also</span></span>  
 <xref:System.AttributeUsageAttribute>  
 [<span data-ttu-id="dc084-110">Création d’attributs personnalisés</span><span class="sxs-lookup"><span data-stu-id="dc084-110">Creating Custom Attributes</span></span>](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)  
 [<span data-ttu-id="dc084-111">AttributeUsage</span><span class="sxs-lookup"><span data-stu-id="dc084-111">AttributeUsage</span></span>](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
