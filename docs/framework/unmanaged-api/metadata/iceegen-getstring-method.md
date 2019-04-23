---
title: ICeeGen::GetString, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetString
helpviewer_keywords:
- ICeeGen::GetString method [.NET Framework metadata]
- GetString method, ICeeGen interface [.NET Framework metadata]
ms.assetid: 7cc22562-128c-440a-9147-55ff20f173d7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 70d78942d4db2fea2cc1ccbcc5ddb20d743e9fdf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093668"
---
# <a name="iceegengetstring-method"></a><span data-ttu-id="cebe5-102">ICeeGen::GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="cebe5-102">ICeeGen::GetString Method</span></span>
<span data-ttu-id="cebe5-103">Obtient la chaîne stockée à l’adresse virtuelle relative spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cebe5-103">Gets the string stored at the specified relative virtual address.</span></span>  
  
 <span data-ttu-id="cebe5-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="cebe5-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cebe5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cebe5-105">Syntax</span></span>  
  
```  
HRESULT GetString (  
    [in]  ULONG      RVA,   
    [out] LPWSTR     *lpString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cebe5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cebe5-106">Parameters</span></span>  
 `RVA`  
 <span data-ttu-id="cebe5-107">[in] L’adresse virtuelle relative de la chaîne à retourner.</span><span class="sxs-lookup"><span data-stu-id="cebe5-107">[in] The relative virtual address of the string to return.</span></span>  
  
 `lpString`  
 <span data-ttu-id="cebe5-108">[out] La chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="cebe5-108">[out] The returned string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cebe5-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cebe5-109">Requirements</span></span>  
 <span data-ttu-id="cebe5-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cebe5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cebe5-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cebe5-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cebe5-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cebe5-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cebe5-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cebe5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cebe5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cebe5-114">See also</span></span>

- [<span data-ttu-id="cebe5-115">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="cebe5-115">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
