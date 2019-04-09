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
ms.openlocfilehash: 79ef272e0c8afa0cd1942416c3a5eb9b825c2e6f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59145143"
---
# <a name="iceegencomputepointer-method"></a><span data-ttu-id="5f3ed-102">ICeeGen::ComputePointer, méthode</span><span class="sxs-lookup"><span data-stu-id="5f3ed-102">ICeeGen::ComputePointer Method</span></span>
<span data-ttu-id="5f3ed-103">Détermine la mémoire tampon pour la section de code spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-103">Determines the buffer for the specified code section.</span></span>  
  
 <span data-ttu-id="5f3ed-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f3ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f3ed-105">Syntax</span></span>  
  
```  
HRESULT ComputePointer (  
    [in]  HCEESECTION  section,  
    [in]  ULONG        RVA,   
    [out] UCHAR        **lpBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f3ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f3ed-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="5f3ed-107">[in] La section de code pour laquelle retourner une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-107">[in] The code section for which to return a buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="5f3ed-108">[in] L’adresse virtuelle relative de la méthode pour laquelle obtenir un pointeur.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-108">[in] The relative virtual address of the method for which to get a pointer.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="5f3ed-109">[out] Pointeur vers la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="5f3ed-109">[out] A pointer to the returned buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f3ed-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f3ed-110">Requirements</span></span>  
 <span data-ttu-id="5f3ed-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f3ed-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f3ed-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5f3ed-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5f3ed-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f3ed-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="5f3ed-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5f3ed-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5f3ed-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f3ed-115">See also</span></span>

- [<span data-ttu-id="5f3ed-116">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="5f3ed-116">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
