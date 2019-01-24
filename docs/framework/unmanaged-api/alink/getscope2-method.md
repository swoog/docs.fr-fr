---
title: GetScope2, méthode
ms.date: 03/30/2017
api_name:
- IALink2.GetScope2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope2
helpviewer_keywords:
- GetScope2 method
ms.assetid: 49435665-6f5a-4acd-9034-8c9244a04a63
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cc986dc27deb08f779a9654324e6832d8420554a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587132"
---
# <a name="getscope2-method"></a><span data-ttu-id="c6b6e-102">GetScope2, méthode</span><span class="sxs-lookup"><span data-stu-id="c6b6e-102">GetScope2 Method</span></span>
<span data-ttu-id="c6b6e-103">Obtient une portée d’importation.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-103">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6b6e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6b6e-104">Syntax</span></span>  
  
```  
HRESULT GetScope2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport2** ppImportScope  
) PURE;   
```  
  
#### <a name="parameters"></a><span data-ttu-id="c6b6e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6b6e-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="c6b6e-106">ID de l’assembly cible.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-106">ID of target assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="c6b6e-107">ID du fichier à partir duquel importer.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-107">ID of file from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="c6b6e-108">Portée de base zéro à importer.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-108">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="c6b6e-109">Reçoit le pointeur vers [IMetaDataImport2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface pour la portée indiquée.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-109">Receives pointer to [IMetaDataImport2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface for indicated scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c6b6e-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c6b6e-110">Return Value</span></span>  
 <span data-ttu-id="c6b6e-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6b6e-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c6b6e-112">Requirements</span></span>  
 <span data-ttu-id="c6b6e-113">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="c6b6e-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6b6e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6b6e-114">See also</span></span>
- [<span data-ttu-id="c6b6e-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="c6b6e-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="c6b6e-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="c6b6e-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="c6b6e-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="c6b6e-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
