---
title: GetFileDef, méthode
ms.date: 03/30/2017
api_name:
- IALink2.GetFileDef
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetFileDef
helpviewer_keywords:
- GetFileDef method
ms.assetid: 4e3fbe6c-b82a-4181-ab17-7faa1263f5b3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9153c9b3735e265d59ba072f747c92434c95d9ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789868"
---
# <a name="getfiledef-method"></a><span data-ttu-id="c6776-102">GetFileDef, méthode</span><span class="sxs-lookup"><span data-stu-id="c6776-102">GetFileDef Method</span></span>
<span data-ttu-id="c6776-103">Récupère le jeton FileDef réel utilisé dans les métadonnées (par opposition au jeton assigné par ALink).</span><span class="sxs-lookup"><span data-stu-id="c6776-103">Retrieves the actual FileDef token used in metadata (as opposed to the token assigned by ALink).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6776-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6776-104">Syntax</span></span>  
  
```  
HRESULT GetFileDef(  
    mdAssembly AssemblyID,  
    mdFile TargetFile,  
    mdFile* pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="c6776-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6776-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="c6776-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c6776-106">ID of the assembly.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="c6776-107">Jeton du fichier ajouté récupéré à partir de la méthode AddFile ou AddImport (méthode).</span><span class="sxs-lookup"><span data-stu-id="c6776-107">Token of the added file as retrieved from AddFile Method or AddImport Method.</span></span>  
  
 `pScope`  
 <span data-ttu-id="c6776-108">Reçoit le jeton FileDef.</span><span class="sxs-lookup"><span data-stu-id="c6776-108">Receives the FileDef token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c6776-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c6776-109">Return Value</span></span>  
 <span data-ttu-id="c6776-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="c6776-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6776-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6776-111">Requirements</span></span>  
 <span data-ttu-id="c6776-112">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="c6776-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6776-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6776-113">See also</span></span>

- [<span data-ttu-id="c6776-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="c6776-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="c6776-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="c6776-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="c6776-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="c6776-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
