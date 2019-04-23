---
title: LoadStringRCEx, fonction
ms.date: 03/30/2017
api_name:
- LoadStringRCEx
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRCEx
helpviewer_keywords:
- LoadStringRCEx function [.NET Framework hosting]
ms.assetid: bc789636-ca14-4f07-8f77-9305874d7495
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 697557463aa949036acb21e63b9a82b1fb84b415
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59105493"
---
# <a name="loadstringrcex-function"></a><span data-ttu-id="d9474-102">LoadStringRCEx, fonction</span><span class="sxs-lookup"><span data-stu-id="d9474-102">LoadStringRCEx Function</span></span>
<span data-ttu-id="d9474-103">Traduit une valeur HRESULT à un message d’erreur approprié pour la culture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d9474-103">Translates an HRESULT value to an appropriate error message for the specified culture.</span></span>  
  
 <span data-ttu-id="d9474-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9474-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9474-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9474-105">Syntax</span></span>  
  
```  
HRESULT LoadStringRCEx (  
    [in]  LCID    lcid,   
    [in]  UINT    iResouceID,   
    [out] LPWSTR  szBuffer,   
    [in]  int     iMax,   
    [in]  int     bQuiet,   
    [out] int    *pcwchUsed  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9474-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9474-106">Parameters</span></span>  
 `lcid`  
 <span data-ttu-id="d9474-107">[in] Identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="d9474-107">[in] A culture identifier.</span></span> <span data-ttu-id="d9474-108">Passez -1 `lcid` pour utiliser la culture par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9474-108">Pass -1 for `lcid` to use the default culture.</span></span>  
  
 `iResourceID`  
 <span data-ttu-id="d9474-109">[in] Une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d9474-109">[in] An HRESULT.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="d9474-110">[out] Une mémoire tampon qui contient le message d’erreur en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="d9474-110">[out] A buffer that contains the error message upon successful completion.</span></span>  
  
 `iMax`  
 <span data-ttu-id="d9474-111">[in] La taille de la mémoire tampon de message.</span><span class="sxs-lookup"><span data-stu-id="d9474-111">[in] The size of the error message buffer.</span></span>  
  
 `bQuiet`  
 <span data-ttu-id="d9474-112">[in] Ignoré.</span><span class="sxs-lookup"><span data-stu-id="d9474-112">[in] Ignored.</span></span>  
  
 `pcwchUsed`  
 <span data-ttu-id="d9474-113">[out] Pointeur vers la longueur du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d9474-113">[out] A pointer to the length of the error message.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d9474-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d9474-114">Return Value</span></span>  
 <span data-ttu-id="d9474-115">Cette méthode retourne des codes d’erreur COM standards, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9474-115">This method returns standard COM error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="d9474-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d9474-116">Return code</span></span>|<span data-ttu-id="d9474-117">Description</span><span class="sxs-lookup"><span data-stu-id="d9474-117">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="d9474-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9474-118">S_OK</span></span>|<span data-ttu-id="d9474-119">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="d9474-119">The method completed successfully.</span></span>|  
|<span data-ttu-id="d9474-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d9474-120">E_INVALIDARG</span></span>|<span data-ttu-id="d9474-121">`szBuffer` a la valeur null, ou `iMax` est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d9474-121">`szBuffer` is null, or `iMax` is zero (0).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d9474-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d9474-122">Remarks</span></span>  
 <span data-ttu-id="d9474-123">Si la méthode ne se termine pas correctement, `szBuffer` contient une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="d9474-123">If the method does not complete successfully, `szBuffer` contains an empty string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9474-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9474-124">Requirements</span></span>  
 <span data-ttu-id="d9474-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d9474-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9474-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d9474-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d9474-127">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d9474-127">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d9474-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9474-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9474-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9474-129">See also</span></span>

- <xref:System.Globalization.CultureInfo.LCID%2A?displayProperty=nameWithType>
- [<span data-ttu-id="d9474-130">LoadStringRC, fonction</span><span class="sxs-lookup"><span data-stu-id="d9474-130">LoadStringRC Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md)
- [<span data-ttu-id="d9474-131">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="d9474-131">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
