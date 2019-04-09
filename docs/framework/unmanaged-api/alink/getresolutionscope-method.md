---
title: GetResolutionScope, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6c6d298c84b801b87832c56026b05f647cb5a9dd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135170"
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="ece18-102">GetResolutionScope, méthode</span><span class="sxs-lookup"><span data-stu-id="ece18-102">GetResolutionScope Method</span></span>
<span data-ttu-id="ece18-103">Récupère l’étendue d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="ece18-103">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ece18-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ece18-104">Syntax</span></span>  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ece18-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ece18-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="ece18-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ece18-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="ece18-107">Fichier qui a besoin d’une référence.</span><span class="sxs-lookup"><span data-stu-id="ece18-107">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="ece18-108">Jeton du fichier dans lequel le type est défini, généralement récupéré avec [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="ece18-108">Token of file that type is defined in, usually retrieved with [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="ece18-109">Reçoit la référence d’assembly ou module.</span><span class="sxs-lookup"><span data-stu-id="ece18-109">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ece18-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ece18-110">Return Value</span></span>  
 <span data-ttu-id="ece18-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="ece18-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ece18-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ece18-112">Requirements</span></span>  
 <span data-ttu-id="ece18-113">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="ece18-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ece18-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ece18-114">See also</span></span>

- [<span data-ttu-id="ece18-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="ece18-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="ece18-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="ece18-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="ece18-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="ece18-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
