---
title: EmitManifest, méthode
ms.date: 03/30/2017
api_name:
- EmitManifest
- IALink.EmitManifest
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitManifest
helpviewer_keywords:
- EmitManifest method
ms.assetid: fdebc1f3-b62e-4d9e-b775-8ccaa8ecb250
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 051b5f47db05301f3a3326a2cc4cc5cf5c8b1ec2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137824"
---
# <a name="emitmanifest-method"></a><span data-ttu-id="6b5ec-102">EmitManifest, méthode</span><span class="sxs-lookup"><span data-stu-id="6b5ec-102">EmitManifest Method</span></span>
<span data-ttu-id="6b5ec-103">Émet le manifeste final.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-103">Emits the final manifest.</span></span> <span data-ttu-id="6b5ec-104">Appelez cette méthode après l’importation de tous les autres fichiers et la définition de toutes les options.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-104">Call this method after importing all other files and setting all options.</span></span> <span data-ttu-id="6b5ec-105">N’appelez pas cette méthode pour les modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b5ec-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b5ec-106">Syntax</span></span>  
  
```  
HRESULT EmitManifest(  
    mdAssembly   AssemblyID,  
    DWORD*       pdwReserveSize,  
    mdAssembly*  ptkManifest  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="6b5ec-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b5ec-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="6b5ec-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-108">ID of the assembly.</span></span>  
  
 `pdwReserveSize`  
 <span data-ttu-id="6b5ec-109">Reçoit la taille à réserver dans le fichier d’assembly, récupérée à partir de [StrongNameSignatureSize, fonction](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="6b5ec-109">Receives the size to reserve in the assembly file, retrieved from [StrongNameSignatureSize Function](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturesize-function.md).</span></span>  
  
 `ptkManifest`  
 <span data-ttu-id="6b5ec-110">Si vous le souhaitez reçoit le jeton de manifeste d’assembly.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-110">Optionally receives the assembly manifest token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6b5ec-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6b5ec-111">Return Value</span></span>  
 <span data-ttu-id="6b5ec-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b5ec-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b5ec-113">Requirements</span></span>  
 <span data-ttu-id="6b5ec-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="6b5ec-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b5ec-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b5ec-115">See also</span></span>

- [<span data-ttu-id="6b5ec-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="6b5ec-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="6b5ec-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="6b5ec-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="6b5ec-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="6b5ec-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
