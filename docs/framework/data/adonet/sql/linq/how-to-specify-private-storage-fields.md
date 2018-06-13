---
title: 'Comment : spécifier des champs de stockage privés'
ms.date: 03/30/2017
ms.assetid: 5a40e816-cc6e-43a0-b32a-9caaa0ab6912
ms.openlocfilehash: d8a9bacd88b08384e7619dc64ab86cb0651ac44d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361596"
---
# <a name="how-to-specify-private-storage-fields"></a><span data-ttu-id="0adb5-102">Comment : spécifier des champs de stockage privés</span><span class="sxs-lookup"><span data-stu-id="0adb5-102">How to: Specify Private Storage Fields</span></span>
<span data-ttu-id="0adb5-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> propriété sur le <xref:System.Data.Linq.Mapping.DataAttribute> attribut pour désigner le nom d’un champ de stockage sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0adb5-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property on the <xref:System.Data.Linq.Mapping.DataAttribute> attribute to designate the name of an underlying storage field.</span></span>  
  
 <span data-ttu-id="0adb5-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span><span class="sxs-lookup"><span data-stu-id="0adb5-104">For code examples, see <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span></span>  
  
### <a name="to-specify-the-name-of-an-underlying-storage-field"></a><span data-ttu-id="0adb5-105">Pour spécifier le nom d'un champ de stockage sous-jacent</span><span class="sxs-lookup"><span data-stu-id="0adb5-105">To specify the name of an underlying storage field</span></span>  
  
1.  <span data-ttu-id="0adb5-106">Ajoutez la propriété <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="0adb5-106">Add the <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="0adb5-107">Assignez le nom du champ comme valeur de la propriété <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span><span class="sxs-lookup"><span data-stu-id="0adb5-107">Assign the name of the field as the value of the <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0adb5-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0adb5-108">See Also</span></span>  
 [<span data-ttu-id="0adb5-109">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="0adb5-109">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="0adb5-110">Guide pratique pour personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="0adb5-110">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
