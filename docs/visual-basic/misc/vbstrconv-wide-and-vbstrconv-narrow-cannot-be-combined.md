---
title: Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_IllegalWideNarrow
ms.assetid: a53b4e6a-36b1-4e36-b2c5-8196313ec599
ms.openlocfilehash: 0d41e283b103d0a1b585cbf686b66d64f47ed22d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723272"
---
# <a name="vbstrconvwide-and-vbstrconvnarrow-cannot-be-combined"></a>Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
Votre application essaie de combiner les membres de l’énumération `VbStrConv` `Wide` et `Narrow`, qui s’excluent mutuellement.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Supprimez `VbStrConv.Wide` ou `VbStrConv.Narrow`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Globalization>

- [Introduction aux applications internationales basées sur le .NET Framework](/visualstudio/ide/introduction-to-international-applications-based-on-the-dotnet-framework)
