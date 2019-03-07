---
title: ImportTypes, méthode
ms.date: 03/30/2017
api_name:
- IALink.ImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes
helpviewer_keywords:
- ImportTypes method
ms.assetid: 351d4b4c-c939-486d-9471-51914a55f471
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 92dfc2bec33501a5cd9ca6b4ec4c3629b6d89946
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487952"
---
# <a name="importtypes-method"></a><span data-ttu-id="ac6a2-102">ImportTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="ac6a2-102">ImportTypes Method</span></span>
<span data-ttu-id="ac6a2-103">Lance l’importation de types de chaque portée importée par [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="ac6a2-103">Initiates the importing of types from each scope imported via [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac6a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac6a2-104">Syntax</span></span>  
  
```  
HRESULT ImportTypes(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac6a2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac6a2-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="ac6a2-106">ID de l’assembly à importer dans.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-106">ID of the assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="ac6a2-107">ID du fichier à importer à partir de.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-107">ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="ac6a2-108">Portée de base zéro à importer.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-108">Zero-based scope to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="ac6a2-109">Reçoit le handle d’énumérateur pour les types dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-109">Receives enumerator handle for the types in this scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="ac6a2-110">Si vous le souhaitez reçoit [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-110">Optionally receives [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="ac6a2-111">Si vous le souhaitez reçoit le nombre de types dans la portée indiquée.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-111">Optionally receives count of types in the indicated scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ac6a2-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ac6a2-112">Return Value</span></span>  
 <span data-ttu-id="ac6a2-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="ac6a2-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac6a2-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ac6a2-114">Requirements</span></span>  
 <span data-ttu-id="ac6a2-115">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="ac6a2-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac6a2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac6a2-116">See also</span></span>
- [<span data-ttu-id="ac6a2-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="ac6a2-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="ac6a2-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="ac6a2-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="ac6a2-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="ac6a2-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
