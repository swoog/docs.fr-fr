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
ms.openlocfilehash: 622e57aedf6c49e95dc2d7e40ba598361b3e6a26
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59222859"
---
# <a name="importtypes-method"></a><span data-ttu-id="98cc3-102">ImportTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="98cc3-102">ImportTypes Method</span></span>
<span data-ttu-id="98cc3-103">Lance l’importation de types de chaque portée importée par [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="98cc3-103">Initiates the importing of types from each scope imported via [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98cc3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98cc3-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="98cc3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98cc3-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="98cc3-106">ID de l’assembly à importer dans.</span><span class="sxs-lookup"><span data-stu-id="98cc3-106">ID of the assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="98cc3-107">ID du fichier à importer à partir de.</span><span class="sxs-lookup"><span data-stu-id="98cc3-107">ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="98cc3-108">Portée de base zéro à importer.</span><span class="sxs-lookup"><span data-stu-id="98cc3-108">Zero-based scope to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="98cc3-109">Reçoit le handle d’énumérateur pour les types dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="98cc3-109">Receives enumerator handle for the types in this scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="98cc3-110">Si vous le souhaitez reçoit [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="98cc3-110">Optionally receives [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="98cc3-111">Si vous le souhaitez reçoit le nombre de types dans la portée indiquée.</span><span class="sxs-lookup"><span data-stu-id="98cc3-111">Optionally receives count of types in the indicated scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="98cc3-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="98cc3-112">Return Value</span></span>  
 <span data-ttu-id="98cc3-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="98cc3-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98cc3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98cc3-114">Requirements</span></span>  
 <span data-ttu-id="98cc3-115">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="98cc3-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98cc3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98cc3-116">See also</span></span>

- [<span data-ttu-id="98cc3-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="98cc3-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="98cc3-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="98cc3-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="98cc3-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="98cc3-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
