---
title: ImportTypes2, méthode
ms.date: 03/30/2017
api_name:
- IALink2.ImportTypes2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes2
helpviewer_keywords:
- ImportTypes2 method
ms.assetid: 32f3ba58-9695-41e9-ba58-fd19e45ed396
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 51c696679626a598be422376e9dc89b5add1773d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33400489"
---
# <a name="importtypes2-method"></a><span data-ttu-id="40e4f-102">ImportTypes2, méthode</span><span class="sxs-lookup"><span data-stu-id="40e4f-102">ImportTypes2 Method</span></span>
<span data-ttu-id="40e4f-103">Lance l’importation de types.</span><span class="sxs-lookup"><span data-stu-id="40e4f-103">Initiates the import of types.</span></span> <span data-ttu-id="40e4f-104">Appelez cette méthode pour commencer à importer les types de chaque portée importée par [méthode ImportFile](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="40e4f-104">Call this method to begin importing types from each scope imported via [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40e4f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40e4f-105">Syntax</span></span>  
  
```  
HRESULT ImportTypes2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport2** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="40e4f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40e4f-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="40e4f-107">ID de l’assembly dans lequel vous voulez importer.</span><span class="sxs-lookup"><span data-stu-id="40e4f-107">ID of assembly into which to import.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="40e4f-108">ID du fichier à partir duquel importer.</span><span class="sxs-lookup"><span data-stu-id="40e4f-108">ID of file to from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="40e4f-109">Portée de base zéro à partir duquel importer.</span><span class="sxs-lookup"><span data-stu-id="40e4f-109">Zero-based scope from which to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="40e4f-110">Reçoit le handle d’énumérateur pour les types dans l’étendue donnée.</span><span class="sxs-lookup"><span data-stu-id="40e4f-110">Receives enumerator handle for the types in the given scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="40e4f-111">Si vous le souhaitez reçoit [IMetaDataImport2 (Interface)](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="40e4f-111">Optionally receives [IMetaDataImport2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="40e4f-112">Si vous le souhaitez reçoit le nombre de types dans l’étendue spécifiée.</span><span class="sxs-lookup"><span data-stu-id="40e4f-112">Optionally receives count of types in the specified scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="40e4f-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="40e4f-113">Return Value</span></span>  
 <span data-ttu-id="40e4f-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="40e4f-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40e4f-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="40e4f-115">Requirements</span></span>  
 <span data-ttu-id="40e4f-116">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="40e4f-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40e4f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40e4f-117">See Also</span></span>  
 [<span data-ttu-id="40e4f-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="40e4f-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="40e4f-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="40e4f-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="40e4f-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="40e4f-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
