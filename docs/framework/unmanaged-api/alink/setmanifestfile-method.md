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
ms.openlocfilehash: a253503f3046c004cc7109a31b5aa8fd8e8dc195
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618049"
---
# <a name="setmanifestfile-method"></a><span data-ttu-id="797b0-102">SetManifestFile, méthode</span><span class="sxs-lookup"><span data-stu-id="797b0-102">SetManifestFile Method</span></span>
<span data-ttu-id="797b0-103">Vous permet de spécifier ou de réinitialiser le fichier manifest que l’éditeur de liens utilise lorsqu’il crée l’assembly.</span><span class="sxs-lookup"><span data-stu-id="797b0-103">Enables you to specify or reset the manifest file that the linker uses when it creates the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="797b0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="797b0-104">Syntax</span></span>  
  
```  
HRESULT SetManifestFile(  
    LPCWSTR pszFile  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="797b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="797b0-105">Parameters</span></span>  
 `pszFile`  
  
 <span data-ttu-id="797b0-106">Le nom du fichier manifeste dont le contenu est placé dans le blob de ressources Win32.</span><span class="sxs-lookup"><span data-stu-id="797b0-106">The name of the manifest file whose contents are put into the Win32 resources blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="797b0-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="797b0-107">Return Value</span></span>  
 <span data-ttu-id="797b0-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="797b0-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="797b0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="797b0-109">Remarks</span></span>  
 <span data-ttu-id="797b0-110">Appelé avant de demander pour le Win32ResBlob.</span><span class="sxs-lookup"><span data-stu-id="797b0-110">Call this before asking for the Win32ResBlob.</span></span> <span data-ttu-id="797b0-111">La valeur de la `pszFile` paramètre est le nom du fichier manifeste dont le contenu est lu et mis dans les ressources Win32 avec l’ID de RT_MANIFEST.</span><span class="sxs-lookup"><span data-stu-id="797b0-111">The value of the `pszFile` parameter is the name of the manifest file whose contents are read and put in the Win32 resources with ID of RT_MANIFEST.</span></span> <span data-ttu-id="797b0-112">Lorsqu’elle est appelée à l’aide d’un paramètre de valeur NULL, tout manifeste lu précédemment est effacé.</span><span class="sxs-lookup"><span data-stu-id="797b0-112">When called by using a parameter of NULL, any previously read manifest is cleared.</span></span> <span data-ttu-id="797b0-113">Cela permet de réinitialiser l’état de l’éditeur de liens à celle du moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="797b0-113">This enables one to reset the state of the linker to that of initialization time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="797b0-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="797b0-114">Requirements</span></span>  
 <span data-ttu-id="797b0-115">Nécessite aLink.h</span><span class="sxs-lookup"><span data-stu-id="797b0-115">Requires aLink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="797b0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="797b0-116">See also</span></span>
- [<span data-ttu-id="797b0-117">IALink3, interface</span><span class="sxs-lookup"><span data-stu-id="797b0-117">IALink3 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink3-interface.md)
- [<span data-ttu-id="797b0-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="797b0-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
- [<span data-ttu-id="797b0-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="797b0-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="797b0-120">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="797b0-120">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
