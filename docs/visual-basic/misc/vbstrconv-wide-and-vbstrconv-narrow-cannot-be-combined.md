---
title: Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_IllegalWideNarrow
ms.assetid: a53b4e6a-36b1-4e36-b2c5-8196313ec599
ms.openlocfilehash: 917fcdfcb34778074db6a19c04e12c3cf8de90dc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59307923"
---
# <a name="vbstrconvwide-and-vbstrconvnarrow-cannot-be-combined"></a>Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
Votre application essaie de combiner les membres de l’énumération `VbStrConv` `Wide` et `Narrow`, qui s’excluent mutuellement.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Supprimez `VbStrConv.Wide` ou `VbStrConv.Narrow`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Globalization>

- [Introduction aux applications internationales basées sur le .NET Framework](/visualstudio/ide/introduction-to-international-applications-based-on-the-dotnet-framework)
