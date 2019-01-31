---
title: L'attribut '<attributename>' ne peut pas être appliqué plusieurs fois
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: 62e84d174e4e218472eda9b7c08ed677e0140438
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278705"
---
# <a name="attribute-attributename-cannot-be-applied-multiple-times"></a><span data-ttu-id="d535d-102">Attribut '\<attributename >' ne peut pas être appliqué plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="d535d-102">Attribute '\<attributename>' cannot be applied multiple times</span></span>
<span data-ttu-id="d535d-103">L’attribut peut uniquement être appliqué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d535d-103">The attribute can only be applied once.</span></span> <span data-ttu-id="d535d-104">Le `AttributeUsage` attribut détermine si un attribut peut être appliqué plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="d535d-104">The `AttributeUsage` attribute determines whether an attribute can be applied more than once.</span></span>  
  
 <span data-ttu-id="d535d-105">**ID d’erreur :** BC30663</span><span class="sxs-lookup"><span data-stu-id="d535d-105">**Error ID:** BC30663</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d535d-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="d535d-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="d535d-107">Assurez-vous que l’attribut est appliqué uniquement une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d535d-107">Make sure the attribute is only applied once.</span></span>  
  
2.  <span data-ttu-id="d535d-108">Si vous utilisez des attributs personnalisés que vous avez développé, envisagez de modifier leur `AttributeUsage` attribut pour permettre l’utilisation de plusieurs attributs, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d535d-108">If you are using custom attributes you developed, consider changing their `AttributeUsage` attribute to allow multiple attribute usage, as with the following example.</span></span>  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d535d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d535d-109">See also</span></span>
- <xref:System.AttributeUsageAttribute>
- [<span data-ttu-id="d535d-110">Création d’attributs personnalisés</span><span class="sxs-lookup"><span data-stu-id="d535d-110">Creating Custom Attributes</span></span>](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)
- [<span data-ttu-id="d535d-111">AttributeUsage</span><span class="sxs-lookup"><span data-stu-id="d535d-111">AttributeUsage</span></span>](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
