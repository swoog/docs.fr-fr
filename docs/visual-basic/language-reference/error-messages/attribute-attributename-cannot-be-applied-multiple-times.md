---
title: Attribut &#39; &lt;attributename&gt; &#39; ne peut pas être appliqué plusieurs fois
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: 6609ce299799bc3c4b78d48478e99e4d4101dd72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565161"
---
# <a name="attribute-39ltattributenamegt39-cannot-be-applied-multiple-times"></a>Attribut &#39; &lt;attributename&gt; &#39; ne peut pas être appliqué plusieurs fois
L’attribut peut uniquement être appliqué qu’une seule fois. Le `AttributeUsage` attribut détermine si un attribut peut être appliqué plusieurs fois.  
  
 **ID d’erreur :** BC30663  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que l’attribut est appliqué uniquement une seule fois.  
  
2.  Si vous utilisez des attributs personnalisés que vous avez développé, envisagez de modifier leur `AttributeUsage` attribut pour permettre l’utilisation de plusieurs attributs, comme dans l’exemple suivant.  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.AttributeUsageAttribute>
- [Création d’attributs personnalisés](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)
- [AttributeUsage](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
