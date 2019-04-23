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
ms.openlocfilehash: bf7b54ab7a2318e8194bf39dbe41b864633ddb43
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212906"
---
# <a name="emitassembly-method"></a><span data-ttu-id="7ec5b-102">EmitAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="7ec5b-102">EmitAssembly Method</span></span>
<span data-ttu-id="7ec5b-103">Crée l’assembly.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-103">Creates the assembly.</span></span> <span data-ttu-id="7ec5b-104">Appelez cette méthode après la fermeture de tous les autres fichiers à l’exception du fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-104">Call this method after all other files are closed except for the assembly file.</span></span> <span data-ttu-id="7ec5b-105">N’appelez pas cette méthode lors de la production de modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-105">Do not call this method when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ec5b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec5b-106">Syntax</span></span>  
  
```  
HRESULT EmitAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="7ec5b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ec5b-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="7ec5b-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7ec5b-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7ec5b-109">Return Value</span></span>  
 <span data-ttu-id="7ec5b-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ec5b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec5b-111">Requirements</span></span>  
 <span data-ttu-id="7ec5b-112">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="7ec5b-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ec5b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec5b-113">See also</span></span>

- [<span data-ttu-id="7ec5b-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="7ec5b-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="7ec5b-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="7ec5b-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="7ec5b-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="7ec5b-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
