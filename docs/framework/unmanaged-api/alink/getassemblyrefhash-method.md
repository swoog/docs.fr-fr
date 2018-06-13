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
ms.openlocfilehash: ccf60d067af356dda1870a2fb1dcca21966f16a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401484"
---
# <a name="getassemblyrefhash-method"></a><span data-ttu-id="db523-102">GetAssemblyRefHash, méthode</span><span class="sxs-lookup"><span data-stu-id="db523-102">GetAssemblyRefHash Method</span></span>
<span data-ttu-id="db523-103">Récupère un objet blob de hachage pour un assembly donné.</span><span class="sxs-lookup"><span data-stu-id="db523-103">Retrieves a hash blob for a given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db523-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db523-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyRefHash(  
    mdToken FileToken,  
    const void** ppvHash,  
    DWORD* pcbHash  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="db523-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db523-105">Parameters</span></span>  
 `FileToken`  
 <span data-ttu-id="db523-106">ID de l’assembly à laquelle fait référence le code de hachage.</span><span class="sxs-lookup"><span data-stu-id="db523-106">ID of assembly to which the hash will refer.</span></span>  
  
 `ppvHash`  
 <span data-ttu-id="db523-107">Reçoit le blob de hachage obtenue.</span><span class="sxs-lookup"><span data-stu-id="db523-107">Receives the resulting hash blob.</span></span>  
  
 `pcbHash`  
 <span data-ttu-id="db523-108">Reçoit la taille, en octets, de l’objet blob de hachage.</span><span class="sxs-lookup"><span data-stu-id="db523-108">Receives size, in bytes, of hash blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="db523-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="db523-109">Return Value</span></span>  
 <span data-ttu-id="db523-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="db523-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db523-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db523-111">Requirements</span></span>  
 <span data-ttu-id="db523-112">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="db523-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db523-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db523-113">See Also</span></span>  
 [<span data-ttu-id="db523-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="db523-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="db523-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="db523-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="db523-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="db523-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
