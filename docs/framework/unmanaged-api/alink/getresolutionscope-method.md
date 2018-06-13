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
ms.openlocfilehash: e67a71c25c0ae8ee7c54fae2e38d1116a5d92eff
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402585"
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="47714-102">GetResolutionScope, méthode</span><span class="sxs-lookup"><span data-stu-id="47714-102">GetResolutionScope Method</span></span>
<span data-ttu-id="47714-103">Récupère l’étendue d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="47714-103">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47714-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47714-104">Syntax</span></span>  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="47714-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47714-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="47714-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="47714-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="47714-107">Fichier qui a besoin d’être une référence.</span><span class="sxs-lookup"><span data-stu-id="47714-107">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="47714-108">Jeton du fichier dans lequel le type est défini, généralement récupéré avec [méthode ImportFile](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="47714-108">Token of file that type is defined in, usually retrieved with [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="47714-109">Reçoit la référence d’assembly ou module.</span><span class="sxs-lookup"><span data-stu-id="47714-109">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="47714-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="47714-110">Return Value</span></span>  
 <span data-ttu-id="47714-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="47714-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47714-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47714-112">Requirements</span></span>  
 <span data-ttu-id="47714-113">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="47714-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47714-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47714-114">See Also</span></span>  
 [<span data-ttu-id="47714-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="47714-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="47714-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="47714-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="47714-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="47714-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
