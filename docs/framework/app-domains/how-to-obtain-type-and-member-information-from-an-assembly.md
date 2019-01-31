---
title: 'Procédure : obtenir des informations relatives au type et aux membres à partir d’un assembly'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- obtaining assembly information
- assemblies [.NET Framework], obtaining information from
ms.assetid: 348ae651-ccda-4f13-8eda-19e8337e9438
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef3fbb7af3097a67cb39f0c3b2ee294b86f0600e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701597"
---
# <a name="how-to-obtain-type-and-member-information-from-an-assembly"></a>Procédure : obtenir des informations relatives au type et aux membres à partir d’un assembly
L’espace de noms <xref:System.Reflection> contient de nombreuses méthodes pour obtenir des informations à partir d’un assembly. Cette section illustre l’une de ces méthodes. Pour plus d’informations, consultez [Vue d’ensemble de la réflexion](../../../docs/framework/reflection-and-codedom/reflection.md).  
  
 L’exemple suivant obtient des informations relatives au type et aux membres d’un assembly.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.types.viewinfo/cpp/source6.cpp#8)]
 [!code-csharp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.types.viewinfo/cs/source6.cs#8)]
 [!code-vb[Conceptual.Types.ViewInfo#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.types.viewinfo/vb/source6.vb#8)]  
  
## <a name="see-also"></a>Voir aussi
- [Programmation avec des domaines d’application](./application-domains.md#programming-with-application-domains)
- [Réflexion](../../../docs/framework/reflection-and-codedom/reflection.md)
- [Utilisation des domaines d’application](../../../docs/framework/app-domains/use.md)
