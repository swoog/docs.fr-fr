---
title: 'Comment : spécifier des noms de bases de données'
ms.date: 03/30/2017
ms.assetid: b80f0fd2-7f75-45fe-9e12-496f80f183df
ms.openlocfilehash: a69fa1723c0660d3c6dfa8bfa7ec3b9e4dc75d7c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361583"
---
# <a name="how-to-specify-database-names"></a><span data-ttu-id="a979c-102">Comment : spécifier des noms de bases de données</span><span class="sxs-lookup"><span data-stu-id="a979c-102">How to: Specify Database Names</span></span>
<span data-ttu-id="a979c-103">Utilisez la propriété <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> sur un attribut <xref:System.Data.Linq.Mapping.DatabaseAttribute> pour spécifier le nom d'une base de données lorsque la connexion ne fournit pas de nom.</span><span class="sxs-lookup"><span data-stu-id="a979c-103">Use the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property on a <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to specify the name of a database when a name is not supplied by the connection.</span></span>  
  
 <span data-ttu-id="a979c-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span><span class="sxs-lookup"><span data-stu-id="a979c-104">For code samples, see <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span></span>  
  
### <a name="to-specify-the-name-of-the-database"></a><span data-ttu-id="a979c-105">Pour spécifier le nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="a979c-105">To specify the name of the database</span></span>  
  
1.  <span data-ttu-id="a979c-106">Ajoutez l'attribut <xref:System.Data.Linq.Mapping.DatabaseAttribute> à la déclaration de classe de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a979c-106">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to the class declaration for the database.</span></span>  
  
2.  <span data-ttu-id="a979c-107">Ajoutez la propriété <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> à l'attribut <xref:System.Data.Linq.Mapping.DatabaseAttribute>.</span><span class="sxs-lookup"><span data-stu-id="a979c-107">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property to the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute.</span></span>  
  
3.  <span data-ttu-id="a979c-108">Affectez le nom que vous souhaitez spécifier à la valeur de propriété <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span><span class="sxs-lookup"><span data-stu-id="a979c-108">Set the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property value to the name that you want to specify.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a979c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a979c-109">See Also</span></span>  
 [<span data-ttu-id="a979c-110">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="a979c-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="a979c-111">Guide pratique pour personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="a979c-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
