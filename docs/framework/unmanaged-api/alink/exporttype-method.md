---
title: ExportType, méthode
ms.date: 03/30/2017
api_name:
- IALink.ExportType
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportType
helpviewer_keywords:
- ExportType method
ms.assetid: 91a7ce63-f5b8-4f16-b2c4-e1d0baa88944
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 958b56266b0d2dcc317204c39a1df56baabd83e2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402481"
---
# <a name="exporttype-method"></a><span data-ttu-id="93594-102">ExportType, méthode</span><span class="sxs-lookup"><span data-stu-id="93594-102">ExportType Method</span></span>
<span data-ttu-id="93594-103">Spécifie qu’un type est exportable.</span><span class="sxs-lookup"><span data-stu-id="93594-103">Specifies that a type is exportable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93594-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93594-104">Syntax</span></span>  
  
```  
HRESULT ExportType(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="93594-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93594-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="93594-106">ID de l’assembly à exporter à partir de.</span><span class="sxs-lookup"><span data-stu-id="93594-106">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="93594-107">Fichier de jeton ou ID d’assembly de fichier qui définit le type exportable.</span><span class="sxs-lookup"><span data-stu-id="93594-107">File token or assembly ID of file that defines the exportable type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="93594-108">Jeton de type à rendre exportable.</span><span class="sxs-lookup"><span data-stu-id="93594-108">Token of type to be made exportable.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="93594-109">Nom de type qualifié complet à rendre exportable.</span><span class="sxs-lookup"><span data-stu-id="93594-109">Fully qualified type name to be made exportable.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="93594-110">`ComType` indicateurs tels que `tdPublic` ou `tdNested`.</span><span class="sxs-lookup"><span data-stu-id="93594-110">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="93594-111">Ce paramètre peut être passé à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="93594-111">This parameter may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="93594-112">Reçoit le jeton pour le type exporté.</span><span class="sxs-lookup"><span data-stu-id="93594-112">Receives token for exported type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="93594-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="93594-113">Return Value</span></span>  
 <span data-ttu-id="93594-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="93594-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93594-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93594-115">Requirements</span></span>  
 <span data-ttu-id="93594-116">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="93594-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93594-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93594-117">See Also</span></span>  
 [<span data-ttu-id="93594-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="93594-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="93594-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="93594-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="93594-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="93594-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
