---
title: Recherche de revendications dans une classe ClaimSet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- claims [WCF], finding in a claimset
- claims [WCF]
ms.assetid: a76ce107-aeb3-47d0-bfa9-134c53664e20
ms.openlocfilehash: 42e6ee682220913f872da337eb41f6c290082988
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137122"
---
# <a name="finding-claims-in-a-claimset"></a><span data-ttu-id="a8894-102">Recherche de revendications dans une classe ClaimSet</span><span class="sxs-lookup"><span data-stu-id="a8894-102">Finding Claims in a ClaimSet</span></span>
<span data-ttu-id="a8894-103">L’examen du contenu d’une classe <xref:System.IdentityModel.Claims.ClaimSet> dans le but de rechercher des types particuliers de revendications est une tâche courante dans le cadre de l’utilisation de l’autorisation basée sur revendication.</span><span class="sxs-lookup"><span data-stu-id="a8894-103">Examining the content of a <xref:System.IdentityModel.Claims.ClaimSet> for particular types of claims is a common task when using claim-based authorization.</span></span> <span data-ttu-id="a8894-104">Pour examiner une classe <xref:System.IdentityModel.Claims.ClaimSet> afin de rechercher des revendications particulières, utilisez la méthode <xref:System.IdentityModel.Claims.ClaimSet.FindClaims%2A>.</span><span class="sxs-lookup"><span data-stu-id="a8894-104">To examine a <xref:System.IdentityModel.Claims.ClaimSet> for the presence of particular claims, use the <xref:System.IdentityModel.Claims.ClaimSet.FindClaims%2A> method.</span></span> <span data-ttu-id="a8894-105">Cette méthode est plus performante que l'itération directe au sein de <xref:System.IdentityModel.Claims.ClaimSet>.</span><span class="sxs-lookup"><span data-stu-id="a8894-105">This method provides better performance than iterating directly over the <xref:System.IdentityModel.Claims.ClaimSet>.</span></span> <span data-ttu-id="a8894-106">L'exemple suivant illustre cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="a8894-106">The following example demonstrates this usage.</span></span> <span data-ttu-id="a8894-107">Notez que les paramètres `claimType` et `claimRight` peuvent avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="a8894-107">Note that the `claimType` and `claimRight` parameters can be `null`.</span></span> <span data-ttu-id="a8894-108">Dans ce cas, les paramètres rechercheront tous les types de revendications et tous les droits de revendication.</span><span class="sxs-lookup"><span data-stu-id="a8894-108">In that case, the parameters will match all claim types and claim rights.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8894-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8894-109">Example</span></span>  
 [!code-csharp[c_FindClaimsPerf#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_findclaimsperf/cs/c_findclaimsperf.cs#2)]
 [!code-vb[c_FindClaimsPerf#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_findclaimsperf/vb/c_findclaimsperf.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="a8894-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8894-110">See also</span></span>

- [<span data-ttu-id="a8894-111">Gestion des revendications et autorisation avec le modèle d’identité</span><span class="sxs-lookup"><span data-stu-id="a8894-111">Managing Claims and Authorization with the Identity Model</span></span>](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
