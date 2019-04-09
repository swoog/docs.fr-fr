---
title: ICeeGen::EmitString, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.EmitString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::EmitString
helpviewer_keywords:
- EmitString method [.NET Framework metadata]
- ICeeGen::EmitString method [.NET Framework metadata]
ms.assetid: ad2710a7-edb8-4493-8619-3fce235e3334
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1eabf5631fcfe7a187d0e203d64c7a7f4f5a819a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59209955"
---
# <a name="iceegenemitstring-method"></a><span data-ttu-id="cd8cf-102">ICeeGen::EmitString, méthode</span><span class="sxs-lookup"><span data-stu-id="cd8cf-102">ICeeGen::EmitString Method</span></span>
<span data-ttu-id="cd8cf-103">Émet la chaîne spécifiée dans la base de code.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-103">Emits the specified string into the code base.</span></span>  
  
 <span data-ttu-id="cd8cf-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd8cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd8cf-105">Syntax</span></span>  
  
```  
HRESULT EmitString (  
    [in]  LPWSTR    lpString,  
    [out] ULONG     *RVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd8cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd8cf-106">Parameters</span></span>  
 `lpString`  
 <span data-ttu-id="cd8cf-107">[in] Chaîne à émettre.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-107">[in] The string to emit.</span></span>  
  
 `RVA`  
 <span data-ttu-id="cd8cf-108">[out] L’adresse virtuelle relative de la chaîne émise.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-108">[out] The relative virtual address of the emitted string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd8cf-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd8cf-109">Requirements</span></span>  
 <span data-ttu-id="cd8cf-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd8cf-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd8cf-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cd8cf-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cd8cf-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cd8cf-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="cd8cf-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="cd8cf-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="cd8cf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd8cf-114">See also</span></span>

- [<span data-ttu-id="cd8cf-115">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="cd8cf-115">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
