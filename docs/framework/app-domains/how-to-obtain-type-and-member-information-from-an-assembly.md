---
title: Guide pratique pour obtenir des informations relatives au type et aux membres à partir d'un assembly
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
- obtaining assembly information
- assemblies [.NET Framework], obtaining information from
ms.assetid: 348ae651-ccda-4f13-8eda-19e8337e9438
caps.latest.revision: 11
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 390afb392c06d5ce003d69f028cd667deb4d86c8
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="how-to-obtain-type-and-member-information-from-an-assembly"></a>Guide pratique pour obtenir des informations relatives au type et aux membres à partir d'un assembly
L’espace de noms <xref:System.Reflection> contient de nombreuses méthodes pour obtenir des informations à partir d’un assembly. Cette section illustre l’une de ces méthodes. Pour plus d’informations, consultez [Vue d’ensemble de la réflexion](../../../docs/framework/reflection-and-codedom/reflection.md).  
  
 L’exemple suivant obtient des informations relatives au type et aux membres d’un assembly.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.types.viewinfo/cpp/source6.cpp#8)]
 [!code-csharp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.types.viewinfo/cs/source6.cs#8)]
 [!code-vb[Conceptual.Types.ViewInfo#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.types.viewinfo/vb/source6.vb#8)]  
  
## <a name="see-also"></a>Voir aussi  
 [Programmation avec des domaines d’application](./application-domains.md#programming-with-application-domains) [Réflexion](../../../docs/framework/reflection-and-codedom/reflection.md)  
 [Utilisation des domaines d’application](../../../docs/framework/app-domains/use.md)
