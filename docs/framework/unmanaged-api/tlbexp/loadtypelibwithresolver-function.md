---
title: LoadTypeLibWithResolver, fonction
ms.date: 03/30/2017
api_name:
- LoadTypeLibWithResolver
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- LoadTypeLibWithResolver
helpviewer_keywords:
- LoadTypeLibWithResolver function [.NET Framework]
ms.assetid: 7123a89b-eb9b-463a-a552-a081e33b0a3a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c14080e3ac128a6a7fbb48586f59d8a5ea4105f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049334"
---
# <a name="loadtypelibwithresolver-function"></a><span data-ttu-id="4e70e-102">LoadTypeLibWithResolver, fonction</span><span class="sxs-lookup"><span data-stu-id="4e70e-102">LoadTypeLibWithResolver Function</span></span>
<span data-ttu-id="4e70e-103">Charge une bibliothèque de types et utilise fourni [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) pour résoudre toutes bibliothèques de types référencées en interne.</span><span class="sxs-lookup"><span data-stu-id="4e70e-103">Loads a type library and uses the supplied [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) to resolve any internally referenced type libraries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e70e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e70e-104">Syntax</span></span>  
  
```  
HRESULT LoadTypeLibWithResolver(  
    [in]  LPCOLESTR           szFile,  
    [in]  REGKIND             regkind,  
    [in]  ITypeLibResolver   *pTlbResolver,  
    [out] ITypeLib          **pptlib);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4e70e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e70e-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="4e70e-106">[in] Le chemin d’accès de fichier de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4e70e-106">[in] The file path of the type library.</span></span>  
  
 `regkind`  
 <span data-ttu-id="4e70e-107">[in] Un [énumération de regkind a](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/ne-oleauto-tagregkind) indicateur qui contrôle comment la bibliothèque de types est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="4e70e-107">[in] A [REGKIND enumeration](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/ne-oleauto-tagregkind) flag that controls how the type library is registered.</span></span> <span data-ttu-id="4e70e-108">Ses valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="4e70e-108">Its possible values are:</span></span>  
  
- <span data-ttu-id="4e70e-109">`REGKIND_DEFAULT`: Utiliser le comportement de l’inscription par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e70e-109">`REGKIND_DEFAULT`: Use default registration behavior.</span></span>  
  
- <span data-ttu-id="4e70e-110">`REGKIND_REGISTER`: Inscrire cette bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4e70e-110">`REGKIND_REGISTER`: Register this type library.</span></span>  
  
- <span data-ttu-id="4e70e-111">`REGKIND_NONE`: N’enregistrez pas cette bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4e70e-111">`REGKIND_NONE`: Do not register this type library.</span></span>  
  
 `pTlbResolver`  
 <span data-ttu-id="4e70e-112">[in] Un pointeur vers l’implémentation de la [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4e70e-112">[in] A pointer to the implementation of the [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md).</span></span>  
  
 `pptlib`  
 <span data-ttu-id="4e70e-113">[out] Une référence à la bibliothèque de types en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="4e70e-113">[out] A reference to the type library that is being loaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4e70e-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4e70e-114">Return Value</span></span>  
 <span data-ttu-id="4e70e-115">Une des valeurs HRESULT répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4e70e-115">One of the HRESULT values listed in the following table.</span></span>  
  
|<span data-ttu-id="4e70e-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4e70e-116">Return value</span></span>|<span data-ttu-id="4e70e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="4e70e-117">Meaning</span></span>|  
|------------------|-------------|  
|`S_OK`|<span data-ttu-id="4e70e-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4e70e-118">Success.</span></span>|  
|`E_OUTOFMEMORY`|<span data-ttu-id="4e70e-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="4e70e-119">Out of memory.</span></span>|  
|`E_POINTER`|<span data-ttu-id="4e70e-120">Un ou plusieurs des pointeurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4e70e-120">One or more of the pointers are invalid.</span></span>|  
|`E_INVALIDARG`|<span data-ttu-id="4e70e-121">Un ou plusieurs des arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4e70e-121">One or more of the arguments are invalid.</span></span>|  
|`TYPE_E_IOERROR`|<span data-ttu-id="4e70e-122">La fonction n’a pas pu écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="4e70e-122">The function could not write to the file.</span></span>|  
|`TYPE_E_REGISTRYACCESS`|<span data-ttu-id="4e70e-123">La base de données système d’inscription n’a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="4e70e-123">The system registration database could not be opened.</span></span>|  
|`TYPE_E_INVALIDSTATE`|<span data-ttu-id="4e70e-124">La bibliothèque de types n’a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="4e70e-124">The type library could not be opened.</span></span>|  
|`TYPE_E_CANTLOADLIBRARY`|<span data-ttu-id="4e70e-125">La bibliothèque de types ou de la DLL n’a pas pu être chargé.</span><span class="sxs-lookup"><span data-stu-id="4e70e-125">The type library or DLL could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4e70e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="4e70e-126">Remarks</span></span>  
 <span data-ttu-id="4e70e-127">Le [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) appelle le `LoadTypeLibWithResolver` fonction pendant le processus de conversion de l’assembly de bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="4e70e-127">The [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md) calls the `LoadTypeLibWithResolver` function during the assembly-to-type-library conversion process.</span></span>  
  
 <span data-ttu-id="4e70e-128">Cette fonction charge la bibliothèque de types spécifiée avec un accès minimal au Registre.</span><span class="sxs-lookup"><span data-stu-id="4e70e-128">This function loads the specified type library with minimal access to the registry.</span></span> <span data-ttu-id="4e70e-129">La fonction examine ensuite la bibliothèque de types pour les bibliothèques de types référencées en interne, chacun d’eux doit être chargé et ajouté à la bibliothèque de type parent.</span><span class="sxs-lookup"><span data-stu-id="4e70e-129">The function then examines the type library for internally referenced type libraries, each of which must be loaded and added to the parent type library.</span></span>  
  
 <span data-ttu-id="4e70e-130">Avant de la bibliothèque de types référencée peut être chargée, son chemin d’accès du fichier de référence doit être résolu en un chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="4e70e-130">Before a referenced type library can be loaded, its reference file path must be resolved to a full file path.</span></span> <span data-ttu-id="4e70e-131">Ceci est accompli par le [ResolveTypeLib, méthode](../../../../docs/framework/unmanaged-api/tlbexp/resolvetypelib-method.md) qui est fourni par le [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md), qui est transmis dans le `pTlbResolver` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e70e-131">This is accomplished through the [ResolveTypeLib method](../../../../docs/framework/unmanaged-api/tlbexp/resolvetypelib-method.md) that is provided by the [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md), which is passed in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="4e70e-132">Lorsque le chemin d’accès de fichier complet de la bibliothèque de types référencée est connu, le `LoadTypeLibWithResolver` fonction charge et ajoute la bibliothèque de types référencée à la bibliothèque de type parent, création d’une bibliothèque de types principale combinée.</span><span class="sxs-lookup"><span data-stu-id="4e70e-132">When the full file path of the referenced type library is known, the `LoadTypeLibWithResolver` function loads and adds the referenced type library to the parent type library, creating a combined master type library.</span></span>  
  
 <span data-ttu-id="4e70e-133">Une fois que la fonction et chargement de toutes les bibliothèques de types référencées en interne, elle retourne une référence à la bibliothèque de types résolue principale dans le `pptlib` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e70e-133">After the function resolves and loads all internally referenced type libraries, it returns a reference to the master resolved type library in the `pptlib` parameter.</span></span>  
  
 <span data-ttu-id="4e70e-134">Le `LoadTypeLibWithResolver` fonction est généralement appelée par le [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md), qui fournit sa propre interne [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) mise en œuvre dans le `pTlbResolver` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e70e-134">The `LoadTypeLibWithResolver` function is generally called by the [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md), which supplies its own internal [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) implementation in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="4e70e-135">Si vous appelez `LoadTypeLibWithResolver` directement, vous devez fournir votre propre [ITypeLibResolver, interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) implémentation.</span><span class="sxs-lookup"><span data-stu-id="4e70e-135">If you call `LoadTypeLibWithResolver` directly, you must supply your own [ITypeLibResolver interface](../../../../docs/framework/unmanaged-api/tlbexp/itypelibresolver-interface.md) implementation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e70e-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e70e-136">Requirements</span></span>  
 <span data-ttu-id="4e70e-137">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e70e-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e70e-138">**En-tête :** TlbRef.h</span><span class="sxs-lookup"><span data-stu-id="4e70e-138">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="4e70e-139">**Bibliothèque :** TlbRef.lib</span><span class="sxs-lookup"><span data-stu-id="4e70e-139">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="4e70e-140">**Version du .NET framework :** 3.5, 3.0, 2.0</span><span class="sxs-lookup"><span data-stu-id="4e70e-140">**.NET Framework Version:** 3.5, 3.0, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e70e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e70e-141">See also</span></span>

- [<span data-ttu-id="4e70e-142">Fonctions d’assistance Tlbexp</span><span class="sxs-lookup"><span data-stu-id="4e70e-142">Tlbexp Helper Functions</span></span>](../../../../docs/framework/unmanaged-api/tlbexp/index.md)
- [<span data-ttu-id="4e70e-143">LoadTypeLibEx de le dont (fonction)</span><span class="sxs-lookup"><span data-stu-id="4e70e-143">LoadTypeLibEx Function</span></span>](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
