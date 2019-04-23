---
title: ISymUnmanagedReader::ReplaceSymbolStore, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.ReplaceSymbolStore
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::ReplaceSymbolStore
helpviewer_keywords:
- ReplaceSymbolStore method [.NET Framework debugging]
- ISymUnmanagedReader::ReplaceSymbolStore method [.NET Framework debugging]
ms.assetid: 43257761-8cb1-4eaf-8fb5-1f3980cb66cd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 34d93c6956ff391e4d8726d8e45265c96947ad4c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59154763"
---
# <a name="isymunmanagedreaderreplacesymbolstore-method"></a><span data-ttu-id="8a47e-102">ISymUnmanagedReader::ReplaceSymbolStore, méthode</span><span class="sxs-lookup"><span data-stu-id="8a47e-102">ISymUnmanagedReader::ReplaceSymbolStore Method</span></span>
<span data-ttu-id="8a47e-103">Remplace le magasin de symboles existant par un magasin de symboles delta.</span><span class="sxs-lookup"><span data-stu-id="8a47e-103">Replaces the existing symbol store with a delta symbol store.</span></span> <span data-ttu-id="8a47e-104">Cette méthode est similaire à la [UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) (méthode), à ceci près que le delta donné opère un remplacement complet plutôt qu’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8a47e-104">This method is similar to the [UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) method, except that the given delta acts as a complete replacement rather than an update.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8a47e-105">Vous devez spécifier un seul de le `filename` ou `pIStream` paramètres, pas les deux.</span><span class="sxs-lookup"><span data-stu-id="8a47e-105">You need specify only one of the `filename` or `pIStream` parameters, not both.</span></span> <span data-ttu-id="8a47e-106">Si `filename` est spécifié, le magasin de symboles sera actualisée avec les symboles dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="8a47e-106">If `filename` is specified, the symbol store will be updated with the symbols in that file.</span></span> <span data-ttu-id="8a47e-107">Si `pIStream` est spécifié, le magasin sera actualisé avec les données à partir de la <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span><span class="sxs-lookup"><span data-stu-id="8a47e-107">If `pIStream` is specified, the store will be updated with the data from the <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a47e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a47e-108">Syntax</span></span>  
  
```  
HRESULT ReplaceSymbolStore (  
    [in] const WCHAR *filename,  
    [in] IStream *pIStream);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a47e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a47e-109">Parameters</span></span>  
 `filename`  
 <span data-ttu-id="8a47e-110">[in] Le nom du fichier contenant le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="8a47e-110">[in] The name of the file containing the symbol store.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="8a47e-111">[in] Le flux de fichier, utilisé comme alternative à le `filename` paramètre.</span><span class="sxs-lookup"><span data-stu-id="8a47e-111">[in] The file stream, used as an alternative to the `filename` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8a47e-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8a47e-112">Return Value</span></span>  
 <span data-ttu-id="8a47e-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8a47e-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a47e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a47e-114">Requirements</span></span>  
 <span data-ttu-id="8a47e-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8a47e-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a47e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a47e-116">See also</span></span>

- [<span data-ttu-id="8a47e-117">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="8a47e-117">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
