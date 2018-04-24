---
title: "Comment : créer un domaine d'application"
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-bcl
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- application domains, creating
ms.assetid: ba1fa43e-49f5-47d9-bd7f-3024af16f4ba
caps.latest.revision: 9
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 366dbea0f9559cdeccd2e126e4a3e913fb5ba23d
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="how-to-create-an-application-domain"></a>Comment : créer un domaine d'application
Un hôte Common Language Runtime crée automatiquement des domaines d’application quand ils sont nécessaires. Toutefois, vous pouvez créer vos propres domaines d’application et y charger les assemblys que vous souhaitez gérer personnellement. Vous pouvez également créer des domaines d’application à partir desquels vous exécutez du code.  
  
 Vous pouvez créer un domaine d’application à l’aide de l’une des méthodes **CreateDomain** surchargées dans la classe <xref:System.AppDomain?displayProperty=nameWithType>. Vous pouvez nommer le domaine d’application et le référencer par ce nom.  
  
 L’exemple suivant crée un domaine d’application et lui attribue le nom `MyDomain`, puis imprime le nom du domaine hôte et du domaine d’application enfant créé dans la console.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[ADCreateDomain#2](../../../samples/snippets/cpp/VS_Snippets_CLR/ADCreateDomain/CPP/source2.cpp#2)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 [Programmation avec des domaines d’application](application-domains.md#programming-with-application-domains)  
 [Utilisation des domaines d’application](../../../docs/framework/app-domains/use.md)
