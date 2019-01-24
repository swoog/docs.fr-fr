---
title: EmitAssembly, méthode
ms.date: 03/30/2017
api_name:
- IALink2.EmitAssembly
- EmitAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssembly
helpviewer_keywords:
- EmitAssembly method
ms.assetid: 605ff39e-e5cc-4bff-8196-e8d68a9715b9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d73c158fa9d7b5574e4f875b8d51e932e30041b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54572238"
---
# <a name="emitassembly-method"></a><span data-ttu-id="d12cd-102">EmitAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="d12cd-102">EmitAssembly Method</span></span>
<span data-ttu-id="d12cd-103">Crée l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d12cd-103">Creates the assembly.</span></span> <span data-ttu-id="d12cd-104">Appelez cette méthode après la fermeture de tous les autres fichiers à l’exception du fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="d12cd-104">Call this method after all other files are closed except for the assembly file.</span></span> <span data-ttu-id="d12cd-105">N’appelez pas cette méthode lors de la production de modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="d12cd-105">Do not call this method when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d12cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d12cd-106">Syntax</span></span>  
  
```  
HRESULT EmitAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d12cd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d12cd-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="d12cd-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d12cd-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d12cd-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d12cd-109">Return Value</span></span>  
 <span data-ttu-id="d12cd-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="d12cd-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d12cd-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d12cd-111">Requirements</span></span>  
 <span data-ttu-id="d12cd-112">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="d12cd-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d12cd-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d12cd-113">See also</span></span>
- [<span data-ttu-id="d12cd-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="d12cd-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="d12cd-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="d12cd-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="d12cd-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="d12cd-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
