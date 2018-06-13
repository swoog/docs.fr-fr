---
title: EmbedResource, méthode
ms.date: 03/30/2017
api_name:
- IALink.EmbedResource
- EmbedResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmbedResource
helpviewer_keywords:
- EmbedResource method
ms.assetid: 667bd954-6dc6-4020-a3cb-0e8224179993
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eb1fc266c8451953c8b6a9c686f4a1c1951966e3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405396"
---
# <a name="embedresource-method"></a><span data-ttu-id="297ee-102">EmbedResource, méthode</span><span class="sxs-lookup"><span data-stu-id="297ee-102">EmbedResource Method</span></span>
<span data-ttu-id="297ee-103">Déclare une ressource incorporée.</span><span class="sxs-lookup"><span data-stu-id="297ee-103">Declares an embedded resource.</span></span> <span data-ttu-id="297ee-104">Cette méthode n’incorpore pas réellement la ressource.</span><span class="sxs-lookup"><span data-stu-id="297ee-104">This method does not actually embed the resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="297ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="297ee-105">Syntax</span></span>  
  
```  
HRESULT EmbedResource(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    LPCWSTR     pszResourceName,  
    DWORD       dwOffset,  
    DWORD       dwFlags  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="297ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="297ee-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="297ee-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="297ee-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="297ee-108">ID de jeton ou l’assembly du fichier qui contient la ressource de fichier.</span><span class="sxs-lookup"><span data-stu-id="297ee-108">File token or assembly ID of file that contains the resource.</span></span>  
  
 `pszResourceName`  
 <span data-ttu-id="297ee-109">Nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="297ee-109">Name of the resource.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="297ee-110">Décalage de la ressource adresse RVA.</span><span class="sxs-lookup"><span data-stu-id="297ee-110">Offset of resource from RVA.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="297ee-111">Accessibilité indicateurs tels que `mrPublic` et `mrPrivate`.</span><span class="sxs-lookup"><span data-stu-id="297ee-111">Accessibility flags such as `mrPublic` and `mrPrivate`.</span></span> <span data-ttu-id="297ee-112">Ces indicateurs peuvent être passés à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="297ee-112">These flags may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="297ee-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="297ee-113">Return Value</span></span>  
 <span data-ttu-id="297ee-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="297ee-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="297ee-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="297ee-115">Requirements</span></span>  
 <span data-ttu-id="297ee-116">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="297ee-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="297ee-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="297ee-117">See Also</span></span>  
 [<span data-ttu-id="297ee-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="297ee-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="297ee-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="297ee-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="297ee-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="297ee-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
