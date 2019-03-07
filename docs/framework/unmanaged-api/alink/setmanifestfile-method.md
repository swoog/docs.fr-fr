---
title: SetManifestFile, méthode
ms.date: 03/30/2017
api_name:
- IALink3.SetManifestFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetManifestFile
helpviewer_keywords:
- SetManifestFile method
ms.assetid: 1b33de4c-19cb-4a36-a93f-8675b2a36d58
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f22927b388a62ee6025c987bb107b2dfd51da0e3
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57488992"
---
# <a name="setmanifestfile-method"></a><span data-ttu-id="41d67-102">SetManifestFile, méthode</span><span class="sxs-lookup"><span data-stu-id="41d67-102">SetManifestFile Method</span></span>
<span data-ttu-id="41d67-103">Vous permet de spécifier ou de réinitialiser le fichier manifest que l’éditeur de liens utilise lorsqu’il crée l’assembly.</span><span class="sxs-lookup"><span data-stu-id="41d67-103">Enables you to specify or reset the manifest file that the linker uses when it creates the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41d67-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41d67-104">Syntax</span></span>  
  
```  
HRESULT SetManifestFile(  
    LPCWSTR pszFile  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="41d67-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41d67-105">Parameters</span></span>  
 `pszFile`  
  
 <span data-ttu-id="41d67-106">Le nom du fichier manifeste dont le contenu est placé dans le blob de ressources Win32.</span><span class="sxs-lookup"><span data-stu-id="41d67-106">The name of the manifest file whose contents are put into the Win32 resources blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="41d67-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="41d67-107">Return Value</span></span>  
 <span data-ttu-id="41d67-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="41d67-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="41d67-109">Notes</span><span class="sxs-lookup"><span data-stu-id="41d67-109">Remarks</span></span>  
 <span data-ttu-id="41d67-110">Appelé avant de demander pour le Win32ResBlob.</span><span class="sxs-lookup"><span data-stu-id="41d67-110">Call this before asking for the Win32ResBlob.</span></span> <span data-ttu-id="41d67-111">La valeur de la `pszFile` paramètre est le nom du fichier manifeste dont le contenu est lu et mis dans les ressources Win32 avec l’ID de RT_MANIFEST.</span><span class="sxs-lookup"><span data-stu-id="41d67-111">The value of the `pszFile` parameter is the name of the manifest file whose contents are read and put in the Win32 resources with ID of RT_MANIFEST.</span></span> <span data-ttu-id="41d67-112">Lorsqu’elle est appelée à l’aide d’un paramètre de valeur NULL, tout manifeste lu précédemment est effacé.</span><span class="sxs-lookup"><span data-stu-id="41d67-112">When called by using a parameter of NULL, any previously read manifest is cleared.</span></span> <span data-ttu-id="41d67-113">Cela permet de réinitialiser l’état de l’éditeur de liens à celle du moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="41d67-113">This enables one to reset the state of the linker to that of initialization time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41d67-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41d67-114">Requirements</span></span>  
 <span data-ttu-id="41d67-115">Nécessite aLink.h</span><span class="sxs-lookup"><span data-stu-id="41d67-115">Requires aLink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41d67-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41d67-116">See also</span></span>
- [<span data-ttu-id="41d67-117">IALink3, interface</span><span class="sxs-lookup"><span data-stu-id="41d67-117">IALink3 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink3-interface.md)
- [<span data-ttu-id="41d67-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="41d67-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
- [<span data-ttu-id="41d67-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="41d67-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="41d67-120">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="41d67-120">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
