---
title: ICeeGen::ComputePointer, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.ComputePointer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::ComputePointer
helpviewer_keywords:
- ICeeGen::ComputePointer method [.NET Framework metadata]
- ComputePointer method [.NET Framework metadata]
ms.assetid: b6b95c04-0f2c-4fcc-a8bc-3b1dcbdba731
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5fb63d4fe1e736ca1ff0c729d8d83cfe092eaaf5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57465528"
---
# <a name="iceegencomputepointer-method"></a><span data-ttu-id="b3b5f-102">ICeeGen::ComputePointer, méthode</span><span class="sxs-lookup"><span data-stu-id="b3b5f-102">ICeeGen::ComputePointer Method</span></span>
<span data-ttu-id="b3b5f-103">Détermine la mémoire tampon pour la section de code spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3b5f-103">Determines the buffer for the specified code section.</span></span>  
  
 <span data-ttu-id="b3b5f-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b3b5f-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3b5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3b5f-105">Syntax</span></span>  
  
```  
HRESULT ComputePointer (  
    [in]  HCEESECTION  section,  
    [in]  ULONG        RVA,   
    [out] UCHAR        **lpBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b3b5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3b5f-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="b3b5f-107">[in] La section de code pour laquelle retourner une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b3b5f-107">[in] The code section for which to return a buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="b3b5f-108">[in] L’adresse virtuelle relative de la méthode pour laquelle obtenir un pointeur.</span><span class="sxs-lookup"><span data-stu-id="b3b5f-108">[in] The relative virtual address of the method for which to get a pointer.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="b3b5f-109">[out] Pointeur vers la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="b3b5f-109">[out] A pointer to the returned buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3b5f-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b3b5f-110">Requirements</span></span>  
 <span data-ttu-id="b3b5f-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3b5f-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3b5f-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b3b5f-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b3b5f-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b3b5f-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b3b5f-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3b5f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3b5f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3b5f-115">See also</span></span>
- [<span data-ttu-id="b3b5f-116">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="b3b5f-116">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
