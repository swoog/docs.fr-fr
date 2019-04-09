---
title: System.Convert, méthodes
ms.date: 03/30/2017
ms.assetid: 3ca6c5b6-ea5d-4ab0-b675-f082135b342c
ms.openlocfilehash: 0d98d159c24e1a47723aeb07a9654fe22b1d9464
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198216"
---
# <a name="systemconvert-methods"></a>System.Convert, méthodes
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ne prend pas en charge les éléments suivants <xref:System.Convert> méthodes.  
  
-   Versions avec un paramètre <xref:System.IFormatProvider>.  
  
-   Méthodes impliquant des tableaux de caractères ou d'octets :  
  
    -   <xref:System.Convert.FromBase64CharArray%2A>  
  
    -   <xref:System.Convert.ToBase64CharArray%2A>  
  
    -   <xref:System.Convert.FromBase64String%2A>  
  
    -   <xref:System.Convert.ToBase64String%2A>  
  
-   Les méthodes suivantes :  
  
    -   `public static <Type2> To<Type2>(<Type1> value);` où  
  
         `Type1` et `Type2` sont chacun des `sbyte`, `uint`, `ulong`, ou `ushort`.  
  
    -   C# :  
  
         `int To<int type>(string value, int fromBase),`  
  
         `ToString(... value, int toBase)`  
  
    -   Visual Basic :  
  
         `Function To(Of [Numeric])(value as String, fromBase As Integer)`  
  
         `As [Numeric], ToString( value As …, toBase As Integer)`  
  
    -   <xref:System.Convert.IsDBNull%2A>  
  
    -   <xref:System.Convert.GetTypeCode%2A>  
  
    -   <xref:System.Convert.ChangeType%2A>  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
