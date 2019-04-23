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
ms.openlocfilehash: c196bcc159b18b9dc04329d817ebe16e07bb8bb7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59218249"
---
# <a name="emitinternalexportedtypes-method"></a><span data-ttu-id="a1c8b-102">EmitInternalExportedTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="a1c8b-102">EmitInternalExportedTypes Method</span></span>
<span data-ttu-id="a1c8b-103">Émet des types ajoutés à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-103">Emits types added to the assembly.</span></span> <span data-ttu-id="a1c8b-104">Appelez cette méthode une fois connu types internes ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-104">Call this method after known internal types have been added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1c8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1c8b-105">Syntax</span></span>  
  
```  
HRESULT EmitInternalExportedTypes(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1c8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1c8b-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a1c8b-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-107">ID of assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a1c8b-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a1c8b-108">Return Value</span></span>  
 <span data-ttu-id="a1c8b-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1c8b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1c8b-110">Requirements</span></span>  
 <span data-ttu-id="a1c8b-111">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="a1c8b-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1c8b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1c8b-112">See also</span></span>

- [<span data-ttu-id="a1c8b-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="a1c8b-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a1c8b-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="a1c8b-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a1c8b-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="a1c8b-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
