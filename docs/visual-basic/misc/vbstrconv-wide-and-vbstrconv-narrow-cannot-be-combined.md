---
title: Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_IllegalWideNarrow
ms.assetid: a53b4e6a-36b1-4e36-b2c5-8196313ec599
ms.openlocfilehash: 917fcdfcb34778074db6a19c04e12c3cf8de90dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61818753"
---
# <a name="vbstrconvwide-and-vbstrconvnarrow-cannot-be-combined"></a>Impossible de combiner VbStrConv.Wide et VbStrConv.Narrow
Votre application essaie de combiner les membres de l’énumération `VbStrConv` `Wide` et `Narrow`, qui s’excluent mutuellement.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Supprimez `VbStrConv.Wide` ou `VbStrConv.Narrow`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Globalization>

- [Introduction aux applications internationales basées sur le .NET Framework](/visualstudio/ide/introduction-to-international-applications-based-on-the-dotnet-framework)
