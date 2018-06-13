---
title: Guide pratique pour obtenir des informations relatives au type et aux membres à partir d'un assembly
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
ms.openlocfilehash: 5fb06555f18c13f87347a5a76e6f4a3060777f02
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32744065"
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
