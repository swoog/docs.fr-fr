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
ms.openlocfilehash: e1aeffbd5d5b22bea87dd7a49a3268822ce84d38
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481171"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="a03ee-102">PreCloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="a03ee-102">PreCloseAssembly Method</span></span>
<span data-ttu-id="a03ee-103">Ferme le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="a03ee-103">Closes the assembly file.</span></span> <span data-ttu-id="a03ee-104">Appelez cette méthode après la fermeture de tous les autres fichiers, mais avant de fermer le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="a03ee-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="a03ee-105">N’appelez pas cette méthode pour les modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="a03ee-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a03ee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a03ee-106">Syntax</span></span>  
  
```  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a03ee-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a03ee-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a03ee-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a03ee-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a03ee-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a03ee-109">Return Value</span></span>  
 <span data-ttu-id="a03ee-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="a03ee-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a03ee-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a03ee-111">Requirements</span></span>  
 <span data-ttu-id="a03ee-112">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="a03ee-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a03ee-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a03ee-113">See also</span></span>
- [<span data-ttu-id="a03ee-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="a03ee-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a03ee-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="a03ee-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a03ee-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="a03ee-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
