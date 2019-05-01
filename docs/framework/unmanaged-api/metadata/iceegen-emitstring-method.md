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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045035"
---
# <a name="iceegenemitstring-method"></a><span data-ttu-id="75ca6-102">ICeeGen::EmitString, méthode</span><span class="sxs-lookup"><span data-stu-id="75ca6-102">ICeeGen::EmitString Method</span></span>
<span data-ttu-id="75ca6-103">Émet la chaîne spécifiée dans la base de code.</span><span class="sxs-lookup"><span data-stu-id="75ca6-103">Emits the specified string into the code base.</span></span>  
  
 <span data-ttu-id="75ca6-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="75ca6-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75ca6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75ca6-105">Syntax</span></span>  
  
```  
HRESULT EmitString (  
    [in]  LPWSTR    lpString,  
    [out] ULONG     *RVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="75ca6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75ca6-106">Parameters</span></span>  
 `lpString`  
 <span data-ttu-id="75ca6-107">[in] Chaîne à émettre.</span><span class="sxs-lookup"><span data-stu-id="75ca6-107">[in] The string to emit.</span></span>  
  
 `RVA`  
 <span data-ttu-id="75ca6-108">[out] L’adresse virtuelle relative de la chaîne émise.</span><span class="sxs-lookup"><span data-stu-id="75ca6-108">[out] The relative virtual address of the emitted string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75ca6-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75ca6-109">Requirements</span></span>  
 <span data-ttu-id="75ca6-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="75ca6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75ca6-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="75ca6-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="75ca6-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="75ca6-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="75ca6-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75ca6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75ca6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75ca6-114">See also</span></span>

- [<span data-ttu-id="75ca6-115">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="75ca6-115">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
