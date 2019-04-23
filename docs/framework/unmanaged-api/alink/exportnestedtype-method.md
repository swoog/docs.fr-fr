---
title: ExportNestedType, méthode
ms.date: 03/30/2017
api_name:
- IALink.ExportNestedType
- ExportNestedType
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportNestedType
helpviewer_keywords:
- ExportNestedType method
ms.assetid: dec7df60-4d30-47c8-99db-72e0419e5f76
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ff159cf794d566be6478ef890c769a0ac72c9b25
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176603"
---
# <a name="exportnestedtype-method"></a><span data-ttu-id="da07a-102">ExportNestedType, méthode</span><span class="sxs-lookup"><span data-stu-id="da07a-102">ExportNestedType Method</span></span>
<span data-ttu-id="da07a-103">Spécifie les types imbriqués comme étant exportables.</span><span class="sxs-lookup"><span data-stu-id="da07a-103">Specifies nested types as exportable.</span></span> <span data-ttu-id="da07a-104">Le [ExportType, méthode](../../../../docs/framework/unmanaged-api/alink/exporttype-method.md) peut également exporter les types imbriqués, mais cette méthode est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="da07a-104">The [ExportType Method](../../../../docs/framework/unmanaged-api/alink/exporttype-method.md) can also export nested types, but this method is faster.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da07a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da07a-105">Syntax</span></span>  
  
```  
HRESULT ExportNestedType(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    mdExportedType  ParentType,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;   
```  
  
## <a name="parameters"></a><span data-ttu-id="da07a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da07a-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="da07a-107">ID de l’assembly à exporter à partir de.</span><span class="sxs-lookup"><span data-stu-id="da07a-107">ID of assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="da07a-108">Jeton de fichier ou l’Assembly du fichier qui définit le type à rendre exportable.</span><span class="sxs-lookup"><span data-stu-id="da07a-108">File token or Assembly of file that defines the type to be made exportable.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="da07a-109">Type de jeton de type à rendre exportable.</span><span class="sxs-lookup"><span data-stu-id="da07a-109">Type token of type to be made exportable.</span></span>  
  
 `ParentType`  
 <span data-ttu-id="da07a-110">Jeton de type parent.</span><span class="sxs-lookup"><span data-stu-id="da07a-110">Token of parent type.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="da07a-111">Nom de type qualifié complet à exporter.</span><span class="sxs-lookup"><span data-stu-id="da07a-111">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="da07a-112">`ComType` indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="da07a-112">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="da07a-113">Cette valeur peut être passée à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="da07a-113">This value may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="da07a-114">Reçoit le jeton pour le type exporté.</span><span class="sxs-lookup"><span data-stu-id="da07a-114">Receives token for exported type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="da07a-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da07a-115">Return Value</span></span>  
 <span data-ttu-id="da07a-116">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="da07a-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da07a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da07a-117">Requirements</span></span>  
 <span data-ttu-id="da07a-118">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="da07a-118">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da07a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da07a-119">See also</span></span>

- [<span data-ttu-id="da07a-120">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="da07a-120">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="da07a-121">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="da07a-121">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="da07a-122">API ALink</span><span class="sxs-lookup"><span data-stu-id="da07a-122">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
