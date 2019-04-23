---
title: GetFileVersion, fonction
ms.date: 03/30/2017
api_name:
- GetFileVersion
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetFileVersion
helpviewer_keywords:
- GetFileVersion function [.NET Framework hosting]
ms.assetid: b3222c85-da88-4485-97d7-3a6ee3e8d358
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d25a3ccdd66ff7acb70f1f5e6c60157b53cc97c5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59123724"
---
# <a name="getfileversion-function"></a><span data-ttu-id="e63b1-102">GetFileVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="e63b1-102">GetFileVersion Function</span></span>
<span data-ttu-id="e63b1-103">Obtient les informations de version common language runtime (CLR) du fichier spécifié, à l’aide de la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e63b1-103">Gets the common language runtime (CLR) version information of the specified file, using the specified buffer.</span></span>  
  
 <span data-ttu-id="e63b1-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e63b1-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e63b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e63b1-105">Syntax</span></span>  
  
```  
HRESULT GetFileVersion (  
    [in]  LPCWSTR      szFilename,   
    [in, out] LPWSTR   szBuffer,   
    [in]  DWORD        cchBuffer,   
    [out] DWORD        *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e63b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e63b1-106">Parameters</span></span>  
 `szFilename`  
 <span data-ttu-id="e63b1-107">[in] Le chemin d’accès du fichier doit être examinée.</span><span class="sxs-lookup"><span data-stu-id="e63b1-107">[in] The path of the file to be examined.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="e63b1-108">[in, out] La mémoire tampon allouée pour les informations de version qui sont retournées.</span><span class="sxs-lookup"><span data-stu-id="e63b1-108">[in, out] The buffer allocated for the version information that is returned.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="e63b1-109">[in] La taille, en caractères larges, de `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="e63b1-109">[in] The size, in wide characters, of `szBuffer`.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="e63b1-110">[out] La taille, en octets, de retourné `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="e63b1-110">[out] The size, in bytes, of the returned `szBuffer`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e63b1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e63b1-111">Requirements</span></span>  
 <span data-ttu-id="e63b1-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e63b1-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e63b1-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e63b1-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e63b1-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e63b1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e63b1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e63b1-115">See also</span></span>

- [<span data-ttu-id="e63b1-116">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="e63b1-116">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
