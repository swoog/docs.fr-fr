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
ms.openlocfilehash: 6fa8d42f9e849db6a02f6c62b37e04cf5dee016e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789855"
---
# <a name="getassemblyrefhash-method"></a><span data-ttu-id="59605-102">GetAssemblyRefHash, méthode</span><span class="sxs-lookup"><span data-stu-id="59605-102">GetAssemblyRefHash Method</span></span>
<span data-ttu-id="59605-103">Récupère un objet blob de hachage pour un assembly donné.</span><span class="sxs-lookup"><span data-stu-id="59605-103">Retrieves a hash blob for a given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59605-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59605-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyRefHash(  
    mdToken FileToken,  
    const void** ppvHash,  
    DWORD* pcbHash  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="59605-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59605-105">Parameters</span></span>  
 `FileToken`  
 <span data-ttu-id="59605-106">ID de l’assembly auquel le hachage fera référence.</span><span class="sxs-lookup"><span data-stu-id="59605-106">ID of assembly to which the hash will refer.</span></span>  
  
 `ppvHash`  
 <span data-ttu-id="59605-107">Reçoit l’objet blob de hachage résultante.</span><span class="sxs-lookup"><span data-stu-id="59605-107">Receives the resulting hash blob.</span></span>  
  
 `pcbHash`  
 <span data-ttu-id="59605-108">Reçoit la taille, en octets, du blob de hachage.</span><span class="sxs-lookup"><span data-stu-id="59605-108">Receives size, in bytes, of hash blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59605-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="59605-109">Return Value</span></span>  
 <span data-ttu-id="59605-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="59605-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59605-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59605-111">Requirements</span></span>  
 <span data-ttu-id="59605-112">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="59605-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59605-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59605-113">See also</span></span>

- [<span data-ttu-id="59605-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="59605-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="59605-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="59605-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="59605-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="59605-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
