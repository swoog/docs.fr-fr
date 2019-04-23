---
title: La référence d'assembly Friend <reference> n'est pas valide
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: 0c1526e32ddc64cb4124c6f8205d58deef911dd6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59298992"
---
# <a name="friend-assembly-reference-reference-is-invalid"></a><span data-ttu-id="296ac-102">Référence d’assembly friend \<référence > n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="296ac-102">Friend assembly reference \<reference> is invalid</span></span>
<span data-ttu-id="296ac-103">Référence d’assembly friend \<référence > n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="296ac-103">Friend assembly reference \<reference> is invalid.</span></span> <span data-ttu-id="296ac-104">Les assemblys signés avec un nom fort doivent spécifier une clé publique dans leurs déclarations InternalsVisibleTo.</span><span class="sxs-lookup"><span data-stu-id="296ac-104">Strong-name signed assemblies must specify a public key in their InternalsVisibleTo declarations.</span></span>  
  
 <span data-ttu-id="296ac-105">Le nom de l’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut identifie un assembly avec nom fort, mais elle n’inclut pas un `PublicKey` attribut.</span><span class="sxs-lookup"><span data-stu-id="296ac-105">The assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor identifies a strong-named assembly, but it does not include a `PublicKey` attribute.</span></span>  
  
 <span data-ttu-id="296ac-106">**ID d’erreur :** BC31535</span><span class="sxs-lookup"><span data-stu-id="296ac-106">**Error ID:** BC31535</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="296ac-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="296ac-107">To correct this error</span></span>  
  
1. <span data-ttu-id="296ac-108">Déterminer la clé publique pour l’assembly friend avec nom fort.</span><span class="sxs-lookup"><span data-stu-id="296ac-108">Determine the public key for the strong-named friend assembly.</span></span> <span data-ttu-id="296ac-109">Inclure la clé publique comme partie du nom d’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut à l’aide de la `PublicKey` attribut.</span><span class="sxs-lookup"><span data-stu-id="296ac-109">Include the public key as part of the assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor by using the `PublicKey` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="296ac-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="296ac-110">See also</span></span>

- <xref:System.Reflection.AssemblyName>
- [<span data-ttu-id="296ac-111">Assemblys friend</span><span class="sxs-lookup"><span data-stu-id="296ac-111">Friend Assemblies</span></span>](../../../standard/assembly/friend-assemblies.md)
