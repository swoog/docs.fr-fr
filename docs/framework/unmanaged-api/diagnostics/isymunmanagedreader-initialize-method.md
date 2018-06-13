---
title: ISymUnmanagedReader::Initialize, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.Initialize
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::Initialize
helpviewer_keywords:
- ISymUnmanagedReader::Initialize method [.NET Framework debugging]
- Initialize method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 8f0dd2fe-7df7-464e-91f4-5518c586bb5f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d141d23f02b2abc92e3d4455aebe1a4057b6bb85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426471"
---
# <a name="isymunmanagedreaderinitialize-method"></a><span data-ttu-id="75d7d-102">ISymUnmanagedReader::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="75d7d-102">ISymUnmanagedReader::Initialize Method</span></span>
<span data-ttu-id="75d7d-103">Initialise le lecteur de symboles avec l’interface de métadonnées de l’importateur ce lecteur sera associé, ainsi que le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="75d7d-103">Initializes the symbol reader with the metadata importer interface that this reader will be associated with, along with the file name of the module.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="75d7d-104">Cette méthode peut être appelée qu’une seule fois et doit être appelée avant toute autre méthode de lecteur.</span><span class="sxs-lookup"><span data-stu-id="75d7d-104">This method can be called only once, and must be called before any other reader methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75d7d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d7d-105">Syntax</span></span>  
  
```  
HRESULT Initialize (  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *filename,  
    [in]  const WCHAR  *searchPath,  
    [in]  IStream      *pIStream);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="75d7d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75d7d-106">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="75d7d-107">[in] L’interface importateur de métadonnées à laquelle ce lecteur sera associé.</span><span class="sxs-lookup"><span data-stu-id="75d7d-107">[in] The metadata importer interface with which this reader will be associated.</span></span>  
  
 `filename`  
 <span data-ttu-id="75d7d-108">[in] Le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="75d7d-108">[in] The file name of the module.</span></span> <span data-ttu-id="75d7d-109">Vous pouvez utiliser la `pIStream` paramètre à la place.</span><span class="sxs-lookup"><span data-stu-id="75d7d-109">You can use the `pIStream` parameter instead.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="75d7d-110">[in] Le chemin d’accès à rechercher.</span><span class="sxs-lookup"><span data-stu-id="75d7d-110">[in] The path to search.</span></span> <span data-ttu-id="75d7d-111">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="75d7d-111">This parameter is optional.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="75d7d-112">[in] Flux de fichier, utilisé comme alternative au paramètre de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="75d7d-112">[in] The file stream, used as an alternative to the filename parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="75d7d-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="75d7d-113">Return Value</span></span>  
 <span data-ttu-id="75d7d-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="75d7d-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="75d7d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="75d7d-115">Remarks</span></span>  
 <span data-ttu-id="75d7d-116">Vous devez ne spécifier qu’un seul de le `filename` ou `pIStream` paramètres, pas les deux.</span><span class="sxs-lookup"><span data-stu-id="75d7d-116">You need to specify only one of the `filename` or the `pIStream` parameters, not both.</span></span> <span data-ttu-id="75d7d-117">Le paramètre `searchPath` est optionnel.</span><span class="sxs-lookup"><span data-stu-id="75d7d-117">The `searchPath` parameter is optional.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75d7d-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="75d7d-118">Requirements</span></span>  
 <span data-ttu-id="75d7d-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="75d7d-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75d7d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d7d-120">See Also</span></span>  
 [<span data-ttu-id="75d7d-121">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="75d7d-121">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
