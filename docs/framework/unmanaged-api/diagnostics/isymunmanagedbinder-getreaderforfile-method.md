---
title: ISymUnmanagedBinder::GetReaderForFile, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder.GetReaderForFile
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder::GetReaderForFile
helpviewer_keywords:
- ISymUnmanagedBinder::GetReaderForFile method [.NET Framework debugging]
- GetReaderForFile method [.NET Framework debugging]
ms.assetid: 46c06258-831e-47c8-a50a-8650af6b637e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0414cadca910f3290f96a841e3f807f0de469606
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940086"
---
# <a name="isymunmanagedbindergetreaderforfile-method"></a><span data-ttu-id="e16c7-102">ISymUnmanagedBinder::GetReaderForFile, méthode</span><span class="sxs-lookup"><span data-stu-id="e16c7-102">ISymUnmanagedBinder::GetReaderForFile Method</span></span>
<span data-ttu-id="e16c7-103">Une interface de métadonnées et un nom de fichier, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface qui lit les symboles de débogage associés au module.</span><span class="sxs-lookup"><span data-stu-id="e16c7-103">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface that will read the debugging symbols associated with the module.</span></span>  
  
 <span data-ttu-id="e16c7-104">Cette méthode s’ouvre le fichier du programme (PDB) de la base de données uniquement s’il est en regard du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="e16c7-104">This method will open the program database (PDB) file only if it is next to the executable file.</span></span> <span data-ttu-id="e16c7-105">Cette modification a été apportée pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e16c7-105">This change has been made for security purposes.</span></span> <span data-ttu-id="e16c7-106">Si vous avez besoin d’une recherche plus étendue pour le fichier PDB, utilisez la [ISymUnmanagedBinder2::GetReaderForFile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e16c7-106">If you need a more extensive search for the PDB file, use the [ISymUnmanagedBinder2::GetReaderForFile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e16c7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e16c7-107">Syntax</span></span>  
  
```  
HRESULT GetReaderForFile(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [out, retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e16c7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e16c7-108">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="e16c7-109">[in] Pointeur vers l’interface d’importation de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e16c7-109">[in] A pointer to the metadata import interface.</span></span>  
  
 `fileName`  
 <span data-ttu-id="e16c7-110">[in] Pointeur vers le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e16c7-110">[in] A pointer to the file name.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="e16c7-111">[in] Pointeur vers le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="e16c7-111">[in] A pointer to the search path.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="e16c7-112">[out] Un pointeur qui est défini à retourné [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e16c7-112">[out] A pointer that is set to the returned [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e16c7-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e16c7-113">Return Value</span></span>  
 <span data-ttu-id="e16c7-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e16c7-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e16c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e16c7-115">Requirements</span></span>  
 <span data-ttu-id="e16c7-116">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e16c7-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e16c7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e16c7-117">See also</span></span>

- [<span data-ttu-id="e16c7-118">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="e16c7-118">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
- [<span data-ttu-id="e16c7-119">GetReaderForFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="e16c7-119">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)
