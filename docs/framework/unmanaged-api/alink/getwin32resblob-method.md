---
title: GetWin32ResBlob, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetWin32ResBlob
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetWin32ResBlob
helpviewer_keywords:
- GetWin32ResBlob method
ms.assetid: 36997e04-f9f6-4254-a041-6767ac6c51d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a4c77ade46d2401e2499a94504808efd94f79f93
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152150"
---
# <a name="getwin32resblob-method"></a><span data-ttu-id="4b628-102">GetWin32ResBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="4b628-102">GetWin32ResBlob Method</span></span>
<span data-ttu-id="4b628-103">Récupère le blob de ressources Win32.</span><span class="sxs-lookup"><span data-stu-id="4b628-103">Retrieves Win32 resource blob.</span></span> <span data-ttu-id="4b628-104">Appelez cette méthode après avoir défini les options d’assembly.</span><span class="sxs-lookup"><span data-stu-id="4b628-104">Call this method after setting assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b628-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b628-105">Syntax</span></span>  
  
```  
HRESULT GetWin32ResBlob(  
    mdAssembly    AssemblyID,  
    mdToken       FileToken,  
    BOOL          fDll,  
    LPCWSTR       pszIconFile,  
    const void**  ppResBlob,  
    DWORD*        pcbResBlob  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b628-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b628-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="4b628-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4b628-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="4b628-108">Jeton de fichier utilisé pour récupérer le nom de fichier à utiliser lors de la construction de la ressource de Version Win32</span><span class="sxs-lookup"><span data-stu-id="4b628-108">File token used to retrieve the filename to be used when constructing the Win32 Version resource</span></span>  
  
 `fDll`  
 <span data-ttu-id="4b628-109">TRUE si le fichier est une DLL, false pour un fichier EXE.</span><span class="sxs-lookup"><span data-stu-id="4b628-109">TRUE if file is a DLL, false for an EXE.</span></span>  
  
 `pszIconFile`  
 <span data-ttu-id="4b628-110">Icône facultative à insérer dans le blob de ressources.</span><span class="sxs-lookup"><span data-stu-id="4b628-110">Optional icon to insert into the resource blob.</span></span>  
  
 `ppResBlob`  
 <span data-ttu-id="4b628-111">Reçoit le blob de ressources.</span><span class="sxs-lookup"><span data-stu-id="4b628-111">Receives the resource blob.</span></span>  
  
 `pcbResBlob`  
 <span data-ttu-id="4b628-112">Reçoit la taille de l’objet blob.</span><span class="sxs-lookup"><span data-stu-id="4b628-112">Receives the size of the blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b628-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4b628-113">Return Value</span></span>  
 <span data-ttu-id="4b628-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="4b628-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b628-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b628-115">Requirements</span></span>  
 <span data-ttu-id="4b628-116">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="4b628-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b628-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b628-117">See also</span></span>

- [<span data-ttu-id="4b628-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="4b628-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="4b628-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="4b628-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="4b628-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="4b628-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
