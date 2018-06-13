---
title: GetCORSystemDirectory, fonction
ms.date: 03/30/2017
api_name:
- GetCORSystemDirectory
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetCORSystemDirectory
helpviewer_keywords:
- GetCORSystemDirectory function [.NET Framework hosting]
ms.assetid: 3dcd16a7-dafc-4ca8-b5cd-20ffb37db91d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 008514e3637a980f3722d0c9896a17be33d54c31
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431686"
---
# <a name="getcorsystemdirectory-function"></a><span data-ttu-id="cfcb5-102">GetCORSystemDirectory, fonction</span><span class="sxs-lookup"><span data-stu-id="cfcb5-102">GetCORSystemDirectory Function</span></span>
<span data-ttu-id="cfcb5-103">Retourne le répertoire d’installation du common language runtime (CLR) qui est chargé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-103">Returns the installation directory of the common language runtime (CLR) that is loaded into the process.</span></span> <span data-ttu-id="cfcb5-104">Le répertoire d’installation est qualifié complet, par exemple, « c:\windows\microsoft.net\framework\v1.0.3705 ».</span><span class="sxs-lookup"><span data-stu-id="cfcb5-104">The installation directory is fully qualified, for example, "c:\windows\microsoft.net\framework\v1.0.3705".</span></span>  
  
 <span data-ttu-id="cfcb5-105">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-105">This function is deprecated.</span></span> <span data-ttu-id="cfcb5-106">Il est remplacé par le [ICLRRuntimeInfo::GetRuntimeDirectory](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md) méthode fourni dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="cfcb5-106">It is superseded by the [ICLRRuntimeInfo::GetRuntimeDirectory](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md) method provided in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfcb5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfcb5-107">Syntax</span></span>  
  
```  
HRESULT GetCORSystemDirectory (   
    [out] LPWSTR  pbuffer,     
    [in]  DWORD   cchBuffer,   
    [out] DWORD*  dwlength  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="cfcb5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfcb5-108">Parameters</span></span>  
 `pbuffer`  
 <span data-ttu-id="cfcb5-109">[out] Une mémoire tampon dans laquelle le runtime retourne une chaîne qui contient le nom qualifié complet du répertoire d’installation pour le runtime chargé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-109">[out] A buffer in which the runtime returns a string that contains the fully qualified name of the installation directory for the runtime that is loaded into the process.</span></span> <span data-ttu-id="cfcb5-110">Si le runtime n’a pas encore été chargé dans le processus, la fonction retourne les informations de répertoire approprié pour la version la plus récente du runtime installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-110">If the runtime has not yet been loaded into the process, the function returns the appropriate directory information for the latest version of the runtime installed on the computer.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="cfcb5-111">[in] La taille, en octets, de `pbuffer`.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-111">[in] The size, in bytes, of `pbuffer`.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="cfcb5-112">[out] Le nombre de caractères retournés dans `pbuffer`.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-112">[out] The number of characters returned in `pbuffer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cfcb5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cfcb5-113">Remarks</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="cfcb5-114">N’utilisez pas cette fonction dans les processus qui exécutent la version 4 du CLR.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-114">Do not use this function in processes that are running version 4 of the CLR.</span></span> <span data-ttu-id="cfcb5-115">Si une version antérieure du CLR est installée sur l’ordinateur, cette fonction retourne le répertoire d’installation pour cette version.</span><span class="sxs-lookup"><span data-stu-id="cfcb5-115">If an earlier version of the CLR is installed on the computer, this function returns the installation directory for that version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfcb5-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfcb5-116">Requirements</span></span>  
 <span data-ttu-id="cfcb5-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cfcb5-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cfcb5-118">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cfcb5-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cfcb5-119">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cfcb5-119">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cfcb5-120">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cfcb5-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfcb5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfcb5-121">See Also</span></span>  
 [<span data-ttu-id="cfcb5-122">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="cfcb5-122">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
