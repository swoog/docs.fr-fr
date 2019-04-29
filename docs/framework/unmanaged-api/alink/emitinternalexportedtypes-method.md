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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790011"
---
# <a name="emitinternalexportedtypes-method"></a><span data-ttu-id="37f31-102">EmitInternalExportedTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="37f31-102">EmitInternalExportedTypes Method</span></span>
<span data-ttu-id="37f31-103">Émet des types ajoutés à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="37f31-103">Emits types added to the assembly.</span></span> <span data-ttu-id="37f31-104">Appelez cette méthode une fois connu types internes ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="37f31-104">Call this method after known internal types have been added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37f31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37f31-105">Syntax</span></span>  
  
```  
HRESULT EmitInternalExportedTypes(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="37f31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37f31-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="37f31-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="37f31-107">ID of assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="37f31-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="37f31-108">Return Value</span></span>  
 <span data-ttu-id="37f31-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="37f31-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37f31-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37f31-110">Requirements</span></span>  
 <span data-ttu-id="37f31-111">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="37f31-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37f31-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37f31-112">See also</span></span>

- [<span data-ttu-id="37f31-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="37f31-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="37f31-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="37f31-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="37f31-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="37f31-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
