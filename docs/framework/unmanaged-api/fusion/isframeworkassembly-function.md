---
title: IsFrameworkAssembly, fonction
ms.date: 03/30/2017
api_name:
- IsFrameworkAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IsFrameworkAssembly
helpviewer_keywords:
- IsFrameworkAssembly function [.NET Framework fusion]
ms.assetid: b0c6f19b-d4fd-4971-88f0-12ffb5793da3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3fd130759ab11b54b597d5c099c33dab93070ae
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429248"
---
# <a name="isframeworkassembly-function"></a><span data-ttu-id="a2ce4-102">IsFrameworkAssembly, fonction</span><span class="sxs-lookup"><span data-stu-id="a2ce4-102">IsFrameworkAssembly Function</span></span>
<span data-ttu-id="a2ce4-103">Obtient une valeur qui indique si l’assembly spécifié est géré.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-103">Gets a value that indicates whether the specified assembly is managed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2ce4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2ce4-104">Syntax</span></span>  
  
```  
HRESULT IsFrameworkAssembly (  
    [in]  LPCWSTR pwzAssemblyReference,  
    [out] LPBOOL  pbIsFrameworkAssembly,  
    [in]  LPWSTR  pwzFrameworkAssemblyIdentity,  
    [in]  LPDWORD pccSize  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a2ce4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2ce4-105">Parameters</span></span>  
 `pwzAssemblyReference`  
 <span data-ttu-id="a2ce4-106">[in] Le nom de l’assembly à vérifier.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-106">[in] The name of the assembly to check.</span></span>  
  
 `pbIsFrameworkAssembly`  
 <span data-ttu-id="a2ce4-107">[out] Valeur booléenne qui indique si l’assembly est géré.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-107">[out] A Boolean value that indicates whether the assembly is managed.</span></span>  
  
 `pwzFrameworkAssemblyIdentity`  
 <span data-ttu-id="a2ce4-108">[in] Chaîne non canonique qui contient l’identité unique de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-108">[in] An uncanonicalized string that contains the unique identity of the assembly.</span></span>  
  
 `pccSize`  
 <span data-ttu-id="a2ce4-109">[in] Taille de `pwzFrameworkAssemblyIdentity`.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-109">[in] The size of `pwzFrameworkAssemblyIdentity`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a2ce4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a2ce4-110">Remarks</span></span>  
 <span data-ttu-id="a2ce4-111">Le `pwzAssemblyReference` paramètre est un pointeur vers une chaîne de caractères qui contient le nom d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-111">The `pwzAssemblyReference` parameter is a pointer to a character string that contains the name of an assembly.</span></span>  
  
 <span data-ttu-id="a2ce4-112">Si cet assembly fait partie du .NET Framework, le `pbIsFrameworkAssembly` paramètre contient une valeur booléenne `true`.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-112">If this assembly is part of the .NET Framework, the `pbIsFrameworkAssembly` parameter will contain a Boolean value of `true`.</span></span>  
  
 <span data-ttu-id="a2ce4-113">Si l’assembly nommé n’est pas partie du .NET Framework, ou si le `pwzAssemblyReference` paramètre ne désigne pas un assembly, `pbIsFrameworkAssembly` contient une valeur booléenne `false`.</span><span class="sxs-lookup"><span data-stu-id="a2ce4-113">If the named assembly is not part of the .NET Framework, or if the `pwzAssemblyReference` parameter does not name an assembly, `pbIsFrameworkAssembly` will contain a Boolean value of `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2ce4-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a2ce4-114">Requirements</span></span>  
 <span data-ttu-id="a2ce4-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a2ce4-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2ce4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2ce4-116">See Also</span></span>  
 [<span data-ttu-id="a2ce4-117">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="a2ce4-117">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
