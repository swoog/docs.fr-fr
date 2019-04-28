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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61753459"
---
# <a name="precloseassembly-method"></a><span data-ttu-id="b1923-102">PreCloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="b1923-102">PreCloseAssembly Method</span></span>
<span data-ttu-id="b1923-103">Ferme le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="b1923-103">Closes the assembly file.</span></span> <span data-ttu-id="b1923-104">Appelez cette méthode après la fermeture de tous les autres fichiers, mais avant de fermer le fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="b1923-104">Call this method after closing all other files, but before closing the assembly file.</span></span> <span data-ttu-id="b1923-105">N’appelez pas cette méthode pour les modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="b1923-105">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1923-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1923-106">Syntax</span></span>  
  
```  
HRESULT PreCloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1923-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1923-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="b1923-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="b1923-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b1923-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b1923-109">Return Value</span></span>  
 <span data-ttu-id="b1923-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="b1923-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1923-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1923-111">Requirements</span></span>  
 <span data-ttu-id="b1923-112">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="b1923-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1923-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1923-113">See also</span></span>

- [<span data-ttu-id="b1923-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="b1923-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="b1923-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="b1923-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="b1923-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="b1923-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
