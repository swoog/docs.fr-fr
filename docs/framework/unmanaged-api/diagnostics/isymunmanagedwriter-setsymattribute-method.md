---
title: ISymUnmanagedWriter::SetSymAttribute, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetSymAttribute
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetSymAttribute
helpviewer_keywords:
- SetSymAttribute method [.NET Framework debugging]
- ISymUnmanagedWriter::SetSymAttribute method [.NET Framework debugging]
ms.assetid: 64d9b80e-b883-4539-89c7-03573185a1eb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8ffcc3a079e7e9a9d69622dc6666bb0e7641d4e3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59155465"
---
# <a name="isymunmanagedwritersetsymattribute-method"></a><span data-ttu-id="f2905-102">ISymUnmanagedWriter::SetSymAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="f2905-102">ISymUnmanagedWriter::SetSymAttribute Method</span></span>
<span data-ttu-id="f2905-103">Définit un attribut personnalisé en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="f2905-103">Defines a custom attribute based upon its name.</span></span> <span data-ttu-id="f2905-104">Ces attributs sont stockés dans le magasin de symboles, contrairement aux attributs personnalisés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f2905-104">These attributes are held in the symbol store, unlike metadata custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2905-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2905-105">Syntax</span></span>  
  
```  
HRESULT SetSymAttribute(  
    [in] mdToken parent,  
    [in] const WCHAR *name,  
    [in] ULONG32 cData,  
    [in, size_is(cData)] unsigned char data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2905-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2905-106">Parameters</span></span>  
 `parent`  
 <span data-ttu-id="f2905-107">[in] Le jeton de métadonnées pour lequel l’attribut est défini.</span><span class="sxs-lookup"><span data-stu-id="f2905-107">[in] The metadata token for which the attribute is being defined.</span></span>  
  
 `name`  
 <span data-ttu-id="f2905-108">[in] Un pointeur vers un `WCHAR` qui contient le nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="f2905-108">[in] A pointer to a `WCHAR` that contains the attribute name.</span></span>  
  
 `cData`  
 <span data-ttu-id="f2905-109">[in] Un `ULONG32` qui indique la taille de la `data` tableau.</span><span class="sxs-lookup"><span data-stu-id="f2905-109">[in] A `ULONG32` that indicates the size of the `data` array.</span></span>  
  
 `data`  
 <span data-ttu-id="f2905-110">[in] La valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="f2905-110">[in] The attribute value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2905-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f2905-111">Return Value</span></span>  
 <span data-ttu-id="f2905-112">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f2905-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2905-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2905-113">Requirements</span></span>  
 <span data-ttu-id="f2905-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f2905-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2905-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2905-115">See also</span></span>

- [<span data-ttu-id="f2905-116">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="f2905-116">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
