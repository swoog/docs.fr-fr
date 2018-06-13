---
title: SetPEKind, méthode
ms.date: 03/30/2017
api_name:
- IALink2.SetPEKind
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetPEKind
helpviewer_keywords:
- SetPEKind method
ms.assetid: 050e77ee-3014-45c0-9e29-2ebe29347b0d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4b985aeb97621e552e9e97581e67cae029d019ef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405891"
---
# <a name="setpekind-method"></a><span data-ttu-id="15f46-102">SetPEKind, méthode</span><span class="sxs-lookup"><span data-stu-id="15f46-102">SetPEKind Method</span></span>
<span data-ttu-id="15f46-103">Détermine le type exécutable portable, un ordinateur ou spécifique à indépendant de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="15f46-103">Determines the portable executable type, either machine-specific or machine-agnostic.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15f46-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f46-104">Syntax</span></span>  
  
```  
HRESULT SetPEKind(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwPEKind,  
    DWORD dwMachine  
) PURE;   
```  
  
#### <a name="parameters"></a><span data-ttu-id="15f46-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15f46-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="15f46-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="15f46-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="15f46-107">Jeton du fichier pour lequel le type PE doit être défini.</span><span class="sxs-lookup"><span data-stu-id="15f46-107">Token of file for which the PE type is to be set.</span></span> <span data-ttu-id="15f46-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="15f46-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `dwPEKind`  
 <span data-ttu-id="15f46-109">Le type de PE, tel qu’indiqué par le [CorPEKind, énumération](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="15f46-109">The type of PE, as indicated by the [CorPEKind Enumeration](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md).</span></span>  
  
 `dwMachine`  
 <span data-ttu-id="15f46-110">L’architecture d’ordinateur cible, comme indiqué dans l’en-tête NT.</span><span class="sxs-lookup"><span data-stu-id="15f46-110">The target machine architecture, as indicated in the NT header.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="15f46-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="15f46-111">Return Value</span></span>  
 <span data-ttu-id="15f46-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="15f46-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15f46-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="15f46-113">Requirements</span></span>  
 <span data-ttu-id="15f46-114">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="15f46-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15f46-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f46-115">See Also</span></span>  
 [<span data-ttu-id="15f46-116">GetPEKind, méthode</span><span class="sxs-lookup"><span data-stu-id="15f46-116">GetPEKind Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md)  
 [<span data-ttu-id="15f46-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="15f46-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="15f46-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="15f46-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="15f46-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="15f46-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
