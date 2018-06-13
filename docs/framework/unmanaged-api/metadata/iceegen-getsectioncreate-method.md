---
title: ICeeGen::GetSectionCreate, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 857462c380ce51994e13dab5cfe3c28bba0f38be
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443337"
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="a3a77-102">ICeeGen::GetSectionCreate, méthode</span><span class="sxs-lookup"><span data-stu-id="a3a77-102">ICeeGen::GetSectionCreate Method</span></span>
<span data-ttu-id="a3a77-103">Génère et obtient une section de code utilisant le nom spécifié et les valeurs d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="a3a77-103">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="a3a77-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a3a77-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3a77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3a77-105">Syntax</span></span>  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a3a77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3a77-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="a3a77-107">[in] Un pointeur vers une chaîne qui spécifie le nom de la section doit être créé.</span><span class="sxs-lookup"><span data-stu-id="a3a77-107">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="a3a77-108">[in] Indicateurs qui spécifient des options.</span><span class="sxs-lookup"><span data-stu-id="a3a77-108">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="a3a77-109">[out] Pointeur vers la section de code nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="a3a77-109">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a3a77-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a3a77-110">Remarks</span></span>  
 <span data-ttu-id="a3a77-111">Appelez `GetSectionCreate` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérés par d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3a77-111">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3a77-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3a77-112">Requirements</span></span>  
 <span data-ttu-id="a3a77-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a3a77-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3a77-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a3a77-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a3a77-115">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3a77-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a3a77-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3a77-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3a77-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3a77-117">See Also</span></span>  
 [<span data-ttu-id="a3a77-118">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="a3a77-118">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
