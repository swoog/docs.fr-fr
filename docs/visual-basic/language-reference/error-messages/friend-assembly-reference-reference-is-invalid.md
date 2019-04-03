---
title: La référence d'assembly Friend <reference> n'est pas valide
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: 0966cea26c5dde8f116081c7a6411b4275e50f40
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817043"
---
# <a name="friend-assembly-reference-reference-is-invalid"></a><span data-ttu-id="a0838-102">Référence d’assembly friend \<référence > n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="a0838-102">Friend assembly reference \<reference> is invalid</span></span>
<span data-ttu-id="a0838-103">Référence d’assembly friend \<référence > n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a0838-103">Friend assembly reference \<reference> is invalid.</span></span> <span data-ttu-id="a0838-104">Les assemblys signés avec un nom fort doivent spécifier une clé publique dans leurs déclarations InternalsVisibleTo.</span><span class="sxs-lookup"><span data-stu-id="a0838-104">Strong-name signed assemblies must specify a public key in their InternalsVisibleTo declarations.</span></span>  
  
 <span data-ttu-id="a0838-105">Le nom de l’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut identifie un assembly avec nom fort, mais elle n’inclut pas un `PublicKey` attribut.</span><span class="sxs-lookup"><span data-stu-id="a0838-105">The assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor identifies a strong-named assembly, but it does not include a `PublicKey` attribute.</span></span>  
  
 <span data-ttu-id="a0838-106">**ID d’erreur :** BC31535</span><span class="sxs-lookup"><span data-stu-id="a0838-106">**Error ID:** BC31535</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a0838-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="a0838-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="a0838-108">Déterminer la clé publique pour l’assembly friend avec nom fort.</span><span class="sxs-lookup"><span data-stu-id="a0838-108">Determine the public key for the strong-named friend assembly.</span></span> <span data-ttu-id="a0838-109">Inclure la clé publique comme partie du nom d’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut à l’aide de la `PublicKey` attribut.</span><span class="sxs-lookup"><span data-stu-id="a0838-109">Include the public key as part of the assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor by using the `PublicKey` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0838-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0838-110">See also</span></span>

- <xref:System.Reflection.AssemblyName>
- [<span data-ttu-id="a0838-111">Assemblys friend</span><span class="sxs-lookup"><span data-stu-id="a0838-111">Friend Assemblies</span></span>](../../../standard/assembly/friend-assemblies.md)
