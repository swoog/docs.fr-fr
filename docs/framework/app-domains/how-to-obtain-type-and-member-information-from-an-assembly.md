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
ms.openlocfilehash: 9f9d01715a9635b276ca87d94082bb4d3820084e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138877"
---
# <a name="how-to-obtain-type-and-member-information-from-an-assembly"></a><span data-ttu-id="f4033-102">Procédure : obtenir des informations relatives au type et aux membres à partir d’un assembly</span><span class="sxs-lookup"><span data-stu-id="f4033-102">How to: Obtain Type and Member Information from an Assembly</span></span>
<span data-ttu-id="f4033-103">L’espace de noms <xref:System.Reflection> contient de nombreuses méthodes pour obtenir des informations à partir d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="f4033-103">The <xref:System.Reflection> namespace contains many methods for obtaining information from an assembly.</span></span> <span data-ttu-id="f4033-104">Cette section illustre l’une de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f4033-104">This section demonstrates one of these methods.</span></span> <span data-ttu-id="f4033-105">Pour plus d’informations, consultez [Vue d’ensemble de la réflexion](../../../docs/framework/reflection-and-codedom/reflection.md).</span><span class="sxs-lookup"><span data-stu-id="f4033-105">For additional information, see [Reflection Overview](../../../docs/framework/reflection-and-codedom/reflection.md).</span></span>  
  
 <span data-ttu-id="f4033-106">L’exemple suivant obtient des informations relatives au type et aux membres d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="f4033-106">The following example obtains type and member information from an assembly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f4033-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4033-107">Example</span></span>  
 [!code-cpp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.types.viewinfo/cpp/source6.cpp#8)]
 [!code-csharp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.types.viewinfo/cs/source6.cs#8)]
 [!code-vb[Conceptual.Types.ViewInfo#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.types.viewinfo/vb/source6.vb#8)]  
  
## <a name="see-also"></a><span data-ttu-id="f4033-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4033-108">See also</span></span>

- [<span data-ttu-id="f4033-109">Programmation avec des domaines d'application</span><span class="sxs-lookup"><span data-stu-id="f4033-109">Programming with Application Domains</span></span>](./application-domains.md#programming-with-application-domains)
- [<span data-ttu-id="f4033-110">Réflexion</span><span class="sxs-lookup"><span data-stu-id="f4033-110">Reflection</span></span>](../../../docs/framework/reflection-and-codedom/reflection.md)
- [<span data-ttu-id="f4033-111">Utilisation des domaines d'application</span><span class="sxs-lookup"><span data-stu-id="f4033-111">Using Application Domains</span></span>](../../../docs/framework/app-domains/use.md)
