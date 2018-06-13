---
title: EmitInternalExportedTypes, méthode
ms.date: 03/30/2017
api_name:
- EmitInternalExportedTypes
- IALink2.EmitInternalExportedTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitInternalExportedTypes
helpviewer_keywords:
- EmitInternalExportedTypes method
ms.assetid: 28c8b00d-2c14-40b4-aed5-a1db0e2428eb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 55b9d185804f25c7431f2696d67753cc3ba02d1f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402039"
---
# <a name="emitinternalexportedtypes-method"></a><span data-ttu-id="e5538-102">EmitInternalExportedTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="e5538-102">EmitInternalExportedTypes Method</span></span>
<span data-ttu-id="e5538-103">Émet des types ajoutés à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e5538-103">Emits types added to the assembly.</span></span> <span data-ttu-id="e5538-104">Appelez cette méthode une fois connu types internes ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="e5538-104">Call this method after known internal types have been added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5538-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5538-105">Syntax</span></span>  
  
```  
HRESULT EmitInternalExportedTypes(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e5538-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5538-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="e5538-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e5538-107">ID of assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e5538-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e5538-108">Return Value</span></span>  
 <span data-ttu-id="e5538-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="e5538-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5538-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5538-110">Requirements</span></span>  
 <span data-ttu-id="e5538-111">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="e5538-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5538-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5538-112">See Also</span></span>  
 [<span data-ttu-id="e5538-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="e5538-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="e5538-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="e5538-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="e5538-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="e5538-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
