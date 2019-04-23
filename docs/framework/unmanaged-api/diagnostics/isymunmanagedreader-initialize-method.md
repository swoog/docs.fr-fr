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
ms.openlocfilehash: 661c27b9c21f77104b8a86163d3c92d44f8a85df
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181777"
---
# <a name="isymunmanagedreaderinitialize-method"></a><span data-ttu-id="817c8-102">ISymUnmanagedReader::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="817c8-102">ISymUnmanagedReader::Initialize Method</span></span>
<span data-ttu-id="817c8-103">Initialise le lecteur de symboles avec l’interface d’importateur de métadonnées qui ce lecteur sera associé, ainsi que le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="817c8-103">Initializes the symbol reader with the metadata importer interface that this reader will be associated with, along with the file name of the module.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="817c8-104">Cette méthode peut être appelée qu’une seule fois et doit être appelée avant toute autre méthode de lecteur.</span><span class="sxs-lookup"><span data-stu-id="817c8-104">This method can be called only once, and must be called before any other reader methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="817c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="817c8-105">Syntax</span></span>  
  
```  
HRESULT Initialize (  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *filename,  
    [in]  const WCHAR  *searchPath,  
    [in]  IStream      *pIStream);  
```  
  
## <a name="parameters"></a><span data-ttu-id="817c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="817c8-106">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="817c8-107">[in] L’interface importateur de métadonnées avec laquelle ce lecteur sera associé.</span><span class="sxs-lookup"><span data-stu-id="817c8-107">[in] The metadata importer interface with which this reader will be associated.</span></span>  
  
 `filename`  
 <span data-ttu-id="817c8-108">[in] Le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="817c8-108">[in] The file name of the module.</span></span> <span data-ttu-id="817c8-109">Vous pouvez utiliser le `pIStream` paramètre à la place.</span><span class="sxs-lookup"><span data-stu-id="817c8-109">You can use the `pIStream` parameter instead.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="817c8-110">[in] Le chemin d’accès à rechercher.</span><span class="sxs-lookup"><span data-stu-id="817c8-110">[in] The path to search.</span></span> <span data-ttu-id="817c8-111">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="817c8-111">This parameter is optional.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="817c8-112">[in] Le flux de fichier, utilisé comme alternative au paramètre de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="817c8-112">[in] The file stream, used as an alternative to the filename parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="817c8-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="817c8-113">Return Value</span></span>  
 <span data-ttu-id="817c8-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="817c8-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="817c8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="817c8-115">Remarks</span></span>  
 <span data-ttu-id="817c8-116">Vous devez spécifier un seul de le `filename` ou `pIStream` paramètres, pas les deux.</span><span class="sxs-lookup"><span data-stu-id="817c8-116">You need to specify only one of the `filename` or the `pIStream` parameters, not both.</span></span> <span data-ttu-id="817c8-117">Le paramètre `searchPath` est optionnel.</span><span class="sxs-lookup"><span data-stu-id="817c8-117">The `searchPath` parameter is optional.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="817c8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="817c8-118">Requirements</span></span>  
 <span data-ttu-id="817c8-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="817c8-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="817c8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="817c8-120">See also</span></span>

- [<span data-ttu-id="817c8-121">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="817c8-121">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
