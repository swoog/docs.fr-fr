---
title: GetAssemblyRefHash, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetAssemblyRefHash
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetAssemblyRefHash
helpviewer_keywords:
- GetAssemblyRefHash method
ms.assetid: 091a18bd-e901-46f6-b999-74d71c8a7c41
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e5698e5555e82fd8f64fd029f78cda361a367ca7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585222"
---
# <a name="getassemblyrefhash-method"></a><span data-ttu-id="d1dc2-102">GetAssemblyRefHash, méthode</span><span class="sxs-lookup"><span data-stu-id="d1dc2-102">GetAssemblyRefHash Method</span></span>
<span data-ttu-id="d1dc2-103">Récupère un objet blob de hachage pour un assembly donné.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-103">Retrieves a hash blob for a given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1dc2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1dc2-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyRefHash(  
    mdToken FileToken,  
    const void** ppvHash,  
    DWORD* pcbHash  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d1dc2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1dc2-105">Parameters</span></span>  
 `FileToken`  
 <span data-ttu-id="d1dc2-106">ID de l’assembly auquel le hachage fera référence.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-106">ID of assembly to which the hash will refer.</span></span>  
  
 `ppvHash`  
 <span data-ttu-id="d1dc2-107">Reçoit l’objet blob de hachage résultante.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-107">Receives the resulting hash blob.</span></span>  
  
 `pcbHash`  
 <span data-ttu-id="d1dc2-108">Reçoit la taille, en octets, du blob de hachage.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-108">Receives size, in bytes, of hash blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1dc2-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d1dc2-109">Return Value</span></span>  
 <span data-ttu-id="d1dc2-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="d1dc2-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1dc2-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d1dc2-111">Requirements</span></span>  
 <span data-ttu-id="d1dc2-112">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="d1dc2-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1dc2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1dc2-113">See also</span></span>
- [<span data-ttu-id="d1dc2-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="d1dc2-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="d1dc2-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="d1dc2-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="d1dc2-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="d1dc2-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
