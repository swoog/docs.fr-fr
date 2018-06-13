---
title: PreCloseAssembly, méthode
ms.date: 03/30/2017
api_name:
- IALink.PreCloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- PreCloseAssembly
helpviewer_keywords:
- PreCloseAssembly method
ms.assetid: 6d23ac54-15ea-4027-a172-9ebef43e8f56
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82421fa83a6f0d24492d70f961e731b679c25728
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33400716"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="1f601-102">PreCloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="1f601-102">PreCloseAssembly Method</span></span>
<span data-ttu-id="1f601-103">Ferme le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="1f601-103">Closes the assembly file.</span></span> <span data-ttu-id="1f601-104">Appelez cette méthode après la fermeture de tous les autres fichiers, mais avant de fermer le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="1f601-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="1f601-105">N’appelez pas cette méthode pour les modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="1f601-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f601-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f601-106">Syntax</span></span>  
  
```  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1f601-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f601-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="1f601-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="1f601-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1f601-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1f601-109">Return Value</span></span>  
 <span data-ttu-id="1f601-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="1f601-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1f601-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1f601-111">Requirements</span></span>  
 <span data-ttu-id="1f601-112">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="1f601-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f601-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f601-113">See Also</span></span>  
 [<span data-ttu-id="1f601-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="1f601-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="1f601-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="1f601-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="1f601-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="1f601-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
