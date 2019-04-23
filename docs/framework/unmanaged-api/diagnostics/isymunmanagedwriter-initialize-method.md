---
title: ISymUnmanagedWriter::Initialize, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Initialize
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Initialize
helpviewer_keywords:
- ISymUnmanagedWriter::Initialize method [.NET Framework debugging]
- Initialize method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: e0ebd793-3764-4df0-8f12-0e95f60b9eae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 417cf623948d16147f9a1242d714f4df1311a314
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212048"
---
# <a name="isymunmanagedwriterinitialize-method"></a><span data-ttu-id="29163-102">ISymUnmanagedWriter::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="29163-102">ISymUnmanagedWriter::Initialize Method</span></span>
<span data-ttu-id="29163-103">Définit l’interface d’émetteur de métadonnées avec laquelle ce writer sera associé et définit le nom de fichier de sortie dans lequel les symboles de débogage doit être écrite.</span><span class="sxs-lookup"><span data-stu-id="29163-103">Sets the metadata emitter interface with which this writer will be associated, and sets the output file name to which the debugging symbols will be written.</span></span>  
  
 <span data-ttu-id="29163-104">Cette méthode peut être appelée qu’une seule fois, et elle doit être appelée avant toute autre méthode de writer.</span><span class="sxs-lookup"><span data-stu-id="29163-104">This method can be called only once, and it must be called before any other writer methods.</span></span> <span data-ttu-id="29163-105">Certains writers peuvent nécessiter un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="29163-105">Some writers may require a file name.</span></span> <span data-ttu-id="29163-106">Toutefois, vous pouvez toujours passer un nom de fichier à cette méthode sans effet négatif sur les writers qui n’utilisent pas le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="29163-106">However, you can always pass a file name to this method without any negative effect on writers that do not use the file name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29163-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29163-107">Syntax</span></span>  
  
```  
HRESULT Initialize(  
    [in] IUnknown     *emitter,  
    [in] const WCHAR  *filename,  
    [in] IStream      *pIStream,  
    [in] BOOL         fFullBuild);  
```  
  
## <a name="parameters"></a><span data-ttu-id="29163-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29163-108">Parameters</span></span>  
 `emitter`  
 <span data-ttu-id="29163-109">[in] Pointeur vers l’interface d’émetteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="29163-109">[in] A pointer to the metadata emitter interface.</span></span>  
  
 `filename`  
 <span data-ttu-id="29163-110">[in] Le nom de fichier dans lequel les symboles de débogage sont écrits.</span><span class="sxs-lookup"><span data-stu-id="29163-110">[in] The file name to which the debugging symbols are written.</span></span> <span data-ttu-id="29163-111">Si vous spécifiez un nom de fichier pour un writer qui n'utilise pas les noms de fichiers, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="29163-111">If a file name is specified for a writer that does not use file names, this parameter is ignored.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="29163-112">[in] Si spécifié, le writer de symbole émettra les symboles dans la donnée <xref:System.Runtime.InteropServices.ComTypes.IStream> plutôt que dans le fichier spécifié dans le `filename` paramètre.</span><span class="sxs-lookup"><span data-stu-id="29163-112">[in] If specified, the symbol writer will emit the symbols into the given <xref:System.Runtime.InteropServices.ComTypes.IStream> rather than to the file specified in the `filename` parameter.</span></span> <span data-ttu-id="29163-113">Le paramètre `pIStream` est optionnel.</span><span class="sxs-lookup"><span data-stu-id="29163-113">The `pIStream` parameter is optional.</span></span>  
  
 `fFullBuild`  
 <span data-ttu-id="29163-114">[in] `true` s’il s’agit d’une régénération complète ; `false` s’il s’agit d’une compilation incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="29163-114">[in] `true` if this is a full rebuild; `false` if this is an incremental compilation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="29163-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="29163-115">Return Value</span></span>  
 <span data-ttu-id="29163-116">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="29163-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29163-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29163-117">Requirements</span></span>  
 <span data-ttu-id="29163-118">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="29163-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29163-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29163-119">See also</span></span>

- [<span data-ttu-id="29163-120">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="29163-120">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="29163-121">Initialize2, méthode</span><span class="sxs-lookup"><span data-stu-id="29163-121">Initialize2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-initialize2-method.md)
