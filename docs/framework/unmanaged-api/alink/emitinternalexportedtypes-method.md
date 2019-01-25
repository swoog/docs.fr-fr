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
ms.openlocfilehash: 68373e9277a9d87bba6941259588f25a92af90a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710545"
---
# <a name="emitinternalexportedtypes-method"></a><span data-ttu-id="51d7a-102">EmitInternalExportedTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="51d7a-102">EmitInternalExportedTypes Method</span></span>
<span data-ttu-id="51d7a-103">Émet des types ajoutés à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="51d7a-103">Emits types added to the assembly.</span></span> <span data-ttu-id="51d7a-104">Appelez cette méthode une fois connu types internes ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="51d7a-104">Call this method after known internal types have been added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51d7a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51d7a-105">Syntax</span></span>  
  
```  
HRESULT EmitInternalExportedTypes(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="51d7a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51d7a-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="51d7a-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="51d7a-107">ID of assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="51d7a-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="51d7a-108">Return Value</span></span>  
 <span data-ttu-id="51d7a-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="51d7a-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51d7a-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="51d7a-110">Requirements</span></span>  
 <span data-ttu-id="51d7a-111">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="51d7a-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51d7a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51d7a-112">See also</span></span>
- [<span data-ttu-id="51d7a-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="51d7a-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="51d7a-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="51d7a-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="51d7a-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="51d7a-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
