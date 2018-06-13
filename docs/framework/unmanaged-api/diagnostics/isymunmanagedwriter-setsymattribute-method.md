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
ms.openlocfilehash: bd1a55d4100d74b769b2bc1b8fe33d2042f5e739
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428299"
---
# <a name="isymunmanagedwritersetsymattribute-method"></a><span data-ttu-id="ea935-102">ISymUnmanagedWriter::SetSymAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="ea935-102">ISymUnmanagedWriter::SetSymAttribute Method</span></span>
<span data-ttu-id="ea935-103">Définit un attribut personnalisé en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="ea935-103">Defines a custom attribute based upon its name.</span></span> <span data-ttu-id="ea935-104">Ces attributs sont conservés dans le magasin de symboles, contrairement aux attributs personnalisés des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ea935-104">These attributes are held in the symbol store, unlike metadata custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea935-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea935-105">Syntax</span></span>  
  
```  
HRESULT SetSymAttribute(  
    [in] mdToken parent,  
    [in] const WCHAR *name,  
    [in] ULONG32 cData,  
    [in, size_is(cData)] unsigned char data[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ea935-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea935-106">Parameters</span></span>  
 `parent`  
 <span data-ttu-id="ea935-107">[in] Le jeton de métadonnées pour lequel l’attribut est défini.</span><span class="sxs-lookup"><span data-stu-id="ea935-107">[in] The metadata token for which the attribute is being defined.</span></span>  
  
 `name`  
 <span data-ttu-id="ea935-108">[in] Un pointeur vers un `WCHAR` qui contient le nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ea935-108">[in] A pointer to a `WCHAR` that contains the attribute name.</span></span>  
  
 `cData`  
 <span data-ttu-id="ea935-109">[in] A `ULONG32` qui indique la taille de la `data` tableau.</span><span class="sxs-lookup"><span data-stu-id="ea935-109">[in] A `ULONG32` that indicates the size of the `data` array.</span></span>  
  
 `data`  
 <span data-ttu-id="ea935-110">[in] La valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ea935-110">[in] The attribute value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ea935-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ea935-111">Return Value</span></span>  
 <span data-ttu-id="ea935-112">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ea935-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea935-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea935-113">Requirements</span></span>  
 <span data-ttu-id="ea935-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ea935-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea935-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea935-115">See Also</span></span>  
 [<span data-ttu-id="ea935-116">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="ea935-116">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
