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
ms.openlocfilehash: aab42e939651d75b1933962d72ba8bec1090f52d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59184507"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="0ee75-102">PreCloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="0ee75-102">PreCloseAssembly Method</span></span>
<span data-ttu-id="0ee75-103">Ferme le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="0ee75-103">Closes the assembly file.</span></span> <span data-ttu-id="0ee75-104">Appelez cette méthode après la fermeture de tous les autres fichiers, mais avant de fermer le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="0ee75-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="0ee75-105">N’appelez pas cette méthode pour les modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="0ee75-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ee75-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ee75-106">Syntax</span></span>  
  
```  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="0ee75-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ee75-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="0ee75-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0ee75-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0ee75-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0ee75-109">Return Value</span></span>  
 <span data-ttu-id="0ee75-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0ee75-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ee75-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ee75-111">Requirements</span></span>  
 <span data-ttu-id="0ee75-112">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="0ee75-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ee75-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee75-113">See also</span></span>

- [<span data-ttu-id="0ee75-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0ee75-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="0ee75-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0ee75-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="0ee75-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="0ee75-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
