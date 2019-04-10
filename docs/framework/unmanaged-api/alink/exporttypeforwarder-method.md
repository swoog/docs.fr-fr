---
title: ExportTypeForwarder, méthode
ms.date: 03/30/2017
api_name:
- IALink.ExportTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportTypeForwarder
helpviewer_keywords:
- ExportTypeForwarder method
ms.assetid: 55989fa9-ab43-4f08-8eb6-2eb56fa7ca76
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5bdf9fb50fe06141df6f3818c784588b9e2138af
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212022"
---
# <a name="exporttypeforwarder-method"></a><span data-ttu-id="43d6d-102">ExportTypeForwarder, méthode</span><span class="sxs-lookup"><span data-stu-id="43d6d-102">ExportTypeForwarder Method</span></span>
<span data-ttu-id="43d6d-103">Ajoute un redirecteur de type à la table de type de l’assembly donné.</span><span class="sxs-lookup"><span data-stu-id="43d6d-103">Adds a type forwarder to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43d6d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43d6d-104">Syntax</span></span>  
  
```  
HRESULT ExportTypeForwarder(  
    mdAssemblyRef   tkAssemblyRef,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="43d6d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43d6d-105">Parameters</span></span>  
 `tkAssemblyRef`  
 <span data-ttu-id="43d6d-106">Référence à l’assembly auquel le redirecteur de type fait référence.</span><span class="sxs-lookup"><span data-stu-id="43d6d-106">Reference to the assembly to which the type forwarder refers.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="43d6d-107">Nom de type qualifié complet à exporter.</span><span class="sxs-lookup"><span data-stu-id="43d6d-107">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 `ComType` <span data-ttu-id="43d6d-108">indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="43d6d-108">flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="43d6d-109">Cette valeur peut être passée à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="43d6d-109">This value may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="43d6d-110">Reçoit le jeton du type exporté.</span><span class="sxs-lookup"><span data-stu-id="43d6d-110">Receives the token of the exported type.</span></span> <span data-ttu-id="43d6d-111">Cela est nécessaire uniquement pour émettre des types imbriqués.</span><span class="sxs-lookup"><span data-stu-id="43d6d-111">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="43d6d-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="43d6d-112">Return Value</span></span>  
 <span data-ttu-id="43d6d-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="43d6d-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43d6d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43d6d-114">Requirements</span></span>  
 <span data-ttu-id="43d6d-115">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="43d6d-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43d6d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43d6d-116">See also</span></span>

- [<span data-ttu-id="43d6d-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="43d6d-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="43d6d-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="43d6d-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="43d6d-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="43d6d-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
