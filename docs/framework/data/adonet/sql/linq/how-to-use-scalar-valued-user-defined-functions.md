---
title: 'Procédure : Utiliser des fonctions définies par l’utilisateur scalaires'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 714e252f-c053-4bbb-b1f3-924111cd4d97
ms.openlocfilehash: 33c6ae89184b90ba69cc9c3c01f0b1ec9d7ff1cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661683"
---
# <a name="how-to-use-scalar-valued-user-defined-functions"></a>Procédure : Utiliser des fonctions définies par l’utilisateur scalaires
Vous pouvez mapper une méthode cliente définie sur une classe à une fonction définie par l'utilisateur à l'aide de l'attribut <xref:System.Data.Linq.Mapping.FunctionAttribute>. Notez que le corps de la méthode construit une expression qui capture l'intention de l'appel de méthode et passe cette expression au <xref:System.Data.Linq.DataContext> pour la traduire et l'exécuter.  
  
> [!NOTE]
>  L'exécution directe se produit uniquement si la fonction est appelée à l'extérieur d'une requête. Pour plus d'informations, voir [Procédure : Appeler des fonctions définies par l’utilisateur Inline](../../../../../../docs/framework/data/adonet/sql/linq/how-to-call-user-defined-functions-inline.md).  
  
## <a name="example"></a>Exemple  
 Le code SQL suivant présente une fonction scalaire `ReverseCustName()` définie par l'utilisateur.  
  
```  
CREATE FUNCTION ReverseCustName(@string varchar(100))  
RETURNS varchar(100)  
AS  
BEGIN  
    DECLARE @custName varchar(100)  
    -- Implementation left as exercise for users.  
    RETURN @custName  
END  
```  
  
 Vous pouvez mapper une méthode cliente telle que la méthode suivante pour ce code :  
  
 [!code-csharp[DLinqUDFS#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqUDFS/cs/northwind-tfunc.cs#3)]
 [!code-vb[DLinqUDFS#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqUDFS/vb/northwind-tfunc.vb#3)]  
  
## <a name="see-also"></a>Voir aussi
- [Fonctions définies par l’utilisateur](../../../../../../docs/framework/data/adonet/sql/linq/user-defined-functions.md)
