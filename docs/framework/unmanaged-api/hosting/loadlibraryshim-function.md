---
title: LoadLibraryShim, fonction
ms.date: 03/30/2017
api_name:
- LoadLibraryShim
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- LoadLibraryShim
helpviewer_keywords:
- LoadLibraryShim function [.NET Framework hosting]
ms.assetid: 30931874-4d0e-4df1-b3d1-e425b50655d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5fe1ba15f8a9f8ee79582158209049c1e502a61d
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44211682"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="defdb-102">LoadLibraryShim, fonction</span><span class="sxs-lookup"><span data-stu-id="defdb-102">LoadLibraryShim Function</span></span>
<span data-ttu-id="defdb-103">Charge une version spécifiée d’une DLL qui est incluse dans le package redistribuable .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="defdb-103">Loads a specified version of a DLL that is included in the .NET Framework redistributable package.</span></span>  
  
 <span data-ttu-id="defdb-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="defdb-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="defdb-105">Utilisez le [ICLRRuntimeInfo::LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="defdb-105">Use the [ICLRRuntimeInfo::LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="defdb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="defdb-106">Syntax</span></span>  
  
```  
HRESULT LoadLibraryShim (  
    [in]  LPCWSTR  szDllName,  
    [in]  LPCWSTR  szVersion,  
          LPVOID   pvReserved,  
    [out] HMODULE *phModDll  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="defdb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="defdb-107">Parameters</span></span>  
 `szDllName`  
 <span data-ttu-id="defdb-108">[in] Chaîne se terminant par zéro qui représente le nom de la DLL à charger à partir de la bibliothèque .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="defdb-108">[in] A zero-terminated string that represents the name of the DLL to be loaded from the .NET Framework library.</span></span>  
  
 `szVersion`  
 <span data-ttu-id="defdb-109">[in] Chaîne se terminant par zéro qui représente la version de la DLL à charger.</span><span class="sxs-lookup"><span data-stu-id="defdb-109">[in] A zero-terminated string that represents the version of the DLL to be loaded.</span></span> <span data-ttu-id="defdb-110">Si `szVersion` est null, la version sélectionnée pour le chargement est la dernière version de la DLL spécifiée est inférieure à la version 4.</span><span class="sxs-lookup"><span data-stu-id="defdb-110">If `szVersion` is null, the version selected for loading is the latest version of the specified DLL that is less than version 4.</span></span> <span data-ttu-id="defdb-111">Autrement dit, toutes les versions égales ou supérieures à la version 4 sont ignorées si `szVersion` a la valeur null, et si aucune version inférieure à la version 4 n’est installé, la DLL ne parvient pas à charger.</span><span class="sxs-lookup"><span data-stu-id="defdb-111">That is, all versions equal to or greater than version 4 are ignored if `szVersion` is null, and if no version less than version 4 is installed, the DLL fails to load.</span></span> <span data-ttu-id="defdb-112">Cela consiste à garantir que l’installation de le [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)] n’affecte pas des applications existantes ou des composants.</span><span class="sxs-lookup"><span data-stu-id="defdb-112">This is to ensure that installation of the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)] does not affect pre-existing applications or components.</span></span> <span data-ttu-id="defdb-113">Consultez l’entrée [In-Proc SxS and Migration Quick Start](https://go.microsoft.com/fwlink/?LinkId=200329) dans le blog de l’équipe CLR.</span><span class="sxs-lookup"><span data-stu-id="defdb-113">See the entry [In-Proc SxS and Migration Quick Start](https://go.microsoft.com/fwlink/?LinkId=200329) in the CLR team blog.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="defdb-114">Réservé à un usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="defdb-114">Reserved for future use.</span></span>  
  
 `phModDll`  
 <span data-ttu-id="defdb-115">[out] Un pointeur vers le handle du module.</span><span class="sxs-lookup"><span data-stu-id="defdb-115">[out] A pointer to the handle of the module.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="defdb-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="defdb-116">Return Value</span></span>  
 <span data-ttu-id="defdb-117">Cette méthode retourne des codes d’erreur de composant COM (Object Model) standard, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="defdb-117">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="defdb-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="defdb-118">Return code</span></span>|<span data-ttu-id="defdb-119">Description</span><span class="sxs-lookup"><span data-stu-id="defdb-119">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="defdb-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="defdb-120">S_OK</span></span>|<span data-ttu-id="defdb-121">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="defdb-121">The method completed successfully.</span></span>|  
|<span data-ttu-id="defdb-122">CLR_E_SHIM_RUNTIMELOAD</span><span class="sxs-lookup"><span data-stu-id="defdb-122">CLR_E_SHIM_RUNTIMELOAD</span></span>|<span data-ttu-id="defdb-123">Le chargement `szDllName` requiert le chargement, le common language runtime (CLR) et la version nécessaire du CLR ne peut pas être chargé.</span><span class="sxs-lookup"><span data-stu-id="defdb-123">Loading `szDllName` requires loading the common language runtime (CLR), and the necessary version of the CLR cannot be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="defdb-124">Notes</span><span class="sxs-lookup"><span data-stu-id="defdb-124">Remarks</span></span>  
 <span data-ttu-id="defdb-125">Cette fonction est utilisée pour charger les DLL qui sont inclus dans le package redistribuable .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="defdb-125">This function is used to load DLLs that are included in the .NET Framework redistributable package.</span></span> <span data-ttu-id="defdb-126">Il ne charge pas les DLL générées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="defdb-126">It does not load user-generated DLLs.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="defdb-127">À compter de .NET Framework version 2.0, en chargeant Fusion.dll provoque le CLR à charger.</span><span class="sxs-lookup"><span data-stu-id="defdb-127">Beginning with the .NET Framework version 2.0, loading Fusion.dll causes the CLR to be loaded.</span></span> <span data-ttu-id="defdb-128">Il s’agit, car les fonctions dans le fichier Fusion.dll sont maintenant des wrappers dont les implémentations sont fournies par le runtime.</span><span class="sxs-lookup"><span data-stu-id="defdb-128">This is because the functions in Fusion.dll are now wrappers whose implementations are provided by the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="defdb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="defdb-129">Requirements</span></span>  
 <span data-ttu-id="defdb-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="defdb-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="defdb-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="defdb-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="defdb-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="defdb-132">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="defdb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="defdb-133">See Also</span></span>  
 [<span data-ttu-id="defdb-134">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="defdb-134">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
