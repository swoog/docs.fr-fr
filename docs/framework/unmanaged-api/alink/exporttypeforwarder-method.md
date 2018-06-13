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
ms.openlocfilehash: 5b28c18d55b91d6315003229295ab0e6781be183
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406303"
---
# <a name="exporttypeforwarder-method"></a><span data-ttu-id="8b190-102">ExportTypeForwarder, méthode</span><span class="sxs-lookup"><span data-stu-id="8b190-102">ExportTypeForwarder Method</span></span>
<span data-ttu-id="8b190-103">Ajoute un redirecteur de type à la table de type de l’assembly donné.</span><span class="sxs-lookup"><span data-stu-id="8b190-103">Adds a type forwarder to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b190-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b190-104">Syntax</span></span>  
  
```  
HRESULT ExportTypeForwarder(  
    mdAssemblyRef   tkAssemblyRef,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8b190-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b190-105">Parameters</span></span>  
 `tkAssemblyRef`  
 <span data-ttu-id="8b190-106">Référence à l’assembly auquel le redirecteur de type fait référence.</span><span class="sxs-lookup"><span data-stu-id="8b190-106">Reference to the assembly to which the type forwarder refers.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="8b190-107">Nom de type qualifié complet à exporter.</span><span class="sxs-lookup"><span data-stu-id="8b190-107">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="8b190-108">`ComType` indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="8b190-108">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="8b190-109">Cette valeur peut être passée à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b190-109">This value may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="8b190-110">Reçoit le jeton du type exporté.</span><span class="sxs-lookup"><span data-stu-id="8b190-110">Receives the token of the exported type.</span></span> <span data-ttu-id="8b190-111">Cela est nécessaire uniquement pour émettre des types imbriqués.</span><span class="sxs-lookup"><span data-stu-id="8b190-111">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8b190-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8b190-112">Return Value</span></span>  
 <span data-ttu-id="8b190-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="8b190-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b190-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8b190-114">Requirements</span></span>  
 <span data-ttu-id="8b190-115">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="8b190-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b190-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b190-116">See Also</span></span>  
 [<span data-ttu-id="8b190-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="8b190-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="8b190-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="8b190-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="8b190-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="8b190-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
