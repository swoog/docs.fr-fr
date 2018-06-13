---
title: ResolveTypeLib, méthode
ms.date: 03/30/2017
api_name:
- ResolveTypeLib
api_location:
- tlbref.dll
f1_keywords:
- ResolveTypeLib
helpviewer_keywords:
- ITypeLibResolver::ResolveTypeLib method [.NET Framework]
- ResolveTypeLib method [.NET Framework]
ms.assetid: 95d2aa0d-8eeb-4a9f-a216-5249f7e2c167
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 96a9672ee05cb1fe2573620bd1dea23e57339c93
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33460839"
---
# <a name="resolvetypelib-method"></a><span data-ttu-id="4ccd1-102">ResolveTypeLib, méthode</span><span class="sxs-lookup"><span data-stu-id="4ccd1-102">ResolveTypeLib Method</span></span>
<span data-ttu-id="4ccd1-103">Résout le nom simple d’une bibliothèque de types en retournant son chemin d’accès qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-103">Resolves the simple name of a type library by returning its fully qualified path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ccd1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ccd1-104">Syntax</span></span>  
  
```  
HRESULT ResolveTypeLib(  
    [in]  BSTR      bstrSimpleName,  
    [in]  GUID      tlbid,  
    [in]  LCID      lcid,  
    [in]  USHORT    wMajorVersion,  
    [in]  USHORT    wMinorVersion,  
    [in]  SYSKIND   syskind,  
    [out] BSTR     *pbstrResolvedTlbName);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4ccd1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ccd1-105">Parameters</span></span>  
 `bstrSimpleName`  
 <span data-ttu-id="4ccd1-106">[in] A [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) qui contient le nom simple de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-106">[in] A [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) that contains the simple name of the type library.</span></span>  
  
 `tlbid`  
 <span data-ttu-id="4ccd1-107">[in] Le GUID affecté à la bibliothèque de types dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-107">[in] The GUID assigned to the type library in the registry.</span></span>  
  
 `lcid`  
 <span data-ttu-id="4ccd1-108">[in] ID de localisation de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-108">[in] The localization ID of the type library.</span></span>  
  
 `wMajorVersion`  
 <span data-ttu-id="4ccd1-109">[in] Numéro de version principale de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-109">[in] The major version number of the type library.</span></span> <span data-ttu-id="4ccd1-110">Par exemple, pour la version *x.y*, le numéro de version majeure est *x*.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-110">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `wMinorVersion`  
 <span data-ttu-id="4ccd1-111">[in] Numéro de version secondaire de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-111">[in] The minor version number of the type library.</span></span> <span data-ttu-id="4ccd1-112">Par exemple, pour la version *x.y*, le numéro de version mineure est *y*.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-112">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
 `syskind`  
 <span data-ttu-id="4ccd1-113">[in] A [SYSKIND](http://msdn.microsoft.com/library/662048b2-59a8-48ca-9e4f-2f9a5306faa1) indicateur qui identifie l’environnement d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-113">[in] A [SYSKIND](http://msdn.microsoft.com/library/662048b2-59a8-48ca-9e4f-2f9a5306faa1) flag that identifies the operating environment.</span></span> <span data-ttu-id="4ccd1-114">Les valeurs courantes sont SYS_WIN32 et SYS_WIN64.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-114">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pbstrResolvedTlbName`  
 <span data-ttu-id="4ccd1-115">[out] Un pointeur vers un [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) qui contient le chemin d’accès complet de la bibliothèque de types nommée dans le `bstrSimpleName` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-115">[out] A pointer to a [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) that contains the full path of the type library named in the `bstrSimpleName` parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4ccd1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4ccd1-116">Remarks</span></span>  
 <span data-ttu-id="4ccd1-117">Le `ResolveTypeLib` méthode est appelée par le [LoadTypeLibWithResolver, fonction](../../../../docs/framework/unmanaged-api/tlbexp/loadtypelibwithresolver-function.md) pendant [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) de traitement.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-117">The `ResolveTypeLib` method is called by the [LoadTypeLibWithResolver function](../../../../docs/framework/unmanaged-api/tlbexp/loadtypelibwithresolver-function.md) during [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) processing.</span></span>  
  
 <span data-ttu-id="4ccd1-118">Les implémentations personnalisées de cette interface doivent retourner un [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) qui contient le chemin d’accès complet de la bibliothèque de types nommée dans le `bstrSimpleName` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ccd1-118">Custom implementations of this interface must return a [BSTR](http://msdn.microsoft.com/library/1b2d7d2c-47af-4389-a6b6-b01b7e915228) that contains the full path of the type library named in the `bstrSimpleName` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ccd1-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ccd1-119">Requirements</span></span>  
 <span data-ttu-id="4ccd1-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ccd1-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ccd1-121">**En-tête :** TlbRef.idl, TlbRef.h</span><span class="sxs-lookup"><span data-stu-id="4ccd1-121">**Header:** TlbRef.idl, TlbRef.h</span></span>  
  
 <span data-ttu-id="4ccd1-122">**Bibliothèque :** TlbRef.lib</span><span class="sxs-lookup"><span data-stu-id="4ccd1-122">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="4ccd1-123">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ccd1-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ccd1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ccd1-124">See Also</span></span>  
 [<span data-ttu-id="4ccd1-125">Fonctions d’assistance Tlbexp</span><span class="sxs-lookup"><span data-stu-id="4ccd1-125">Tlbexp Helper Functions</span></span>](../../../../docs/framework/unmanaged-api/tlbexp/index.md)  
 [<span data-ttu-id="4ccd1-126">LoadTypeLibEx</span><span class="sxs-lookup"><span data-stu-id="4ccd1-126">LoadTypeLibEx</span></span>](http://msdn.microsoft.com/library/56a7f9e1-810b-4a42-aa4d-691f4304f5ef)
