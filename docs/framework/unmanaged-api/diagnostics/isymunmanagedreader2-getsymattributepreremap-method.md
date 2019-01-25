---
title: ISymUnmanagedReader2::GetSymAttributePreRemap, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetSymAttributePreRemap
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetSymAttributePreRemap
helpviewer_keywords:
- GetSymAttributePreRemap method [.NET Framework debugging]
- ISymUnmanagedReader2::GetSymAttributePreRemap method [.NET Framework debugging]
ms.assetid: 7580d546-a709-40c5-ad02-aa70d774fd0b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0d5702f5df1e2d31a4e01de6be7c70af03b54296
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519682"
---
# <a name="isymunmanagedreader2getsymattributepreremap-method"></a><span data-ttu-id="ce4b2-102">ISymUnmanagedReader2::GetSymAttributePreRemap, méthode</span><span class="sxs-lookup"><span data-stu-id="ce4b2-102">ISymUnmanagedReader2::GetSymAttributePreRemap Method</span></span>
<span data-ttu-id="ce4b2-103">Obtient un attribut personnalisé en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-103">Gets a custom attribute based upon its name.</span></span> <span data-ttu-id="ce4b2-104">Contrairement aux attributs personnalisés des métadonnées, ces attributs sont stockés dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-104">Unlike metadata custom attributes, these attributes are held in the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce4b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce4b2-105">Syntax</span></span>  
  
```  
HRESULT GetSymAttributePreRemap(  
    [in]  mdToken  parent,  
    [in]  WCHAR    *name,  
    [in]  ULONG32  cBuffer,  
    [out] ULONG32  *pcBuffer,  
    [out, size_is(cBuffer),  
        length_is(*pcBuffer)] BYTE buffer[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ce4b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce4b2-106">Parameters</span></span>  
 `parent`  
 <span data-ttu-id="ce4b2-107">[in] Le jeton de métadonnées du parent.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-107">[in] The metadata token of the parent.</span></span>  
  
 `name`  
 <span data-ttu-id="ce4b2-108">[in] Un pointeur vers un `WCHAR` qui contient le nom.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-108">[in] A pointer to a `WCHAR` that contains the name.</span></span>  
  
 `cBuffer`  
 <span data-ttu-id="ce4b2-109">[in] Un `ULONG32` qui indique la taille de la `buffer` tableau.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-109">[in] A `ULONG32` that indicates the size of the `buffer` array.</span></span>  
  
 `pcBuffer`  
 <span data-ttu-id="ce4b2-110">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les octets d’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-110">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the attribute bytes.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ce4b2-111">[out] Pointeur vers la mémoire tampon qui reçoit les octets de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-111">[out] A pointer to the buffer that receives the attribute bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ce4b2-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ce4b2-112">Return Value</span></span>  
 <span data-ttu-id="ce4b2-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce4b2-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce4b2-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce4b2-114">Requirements</span></span>  
 <span data-ttu-id="ce4b2-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ce4b2-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce4b2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce4b2-116">See also</span></span>
- [<span data-ttu-id="ce4b2-117">ISymUnmanagedReader2, interface</span><span class="sxs-lookup"><span data-stu-id="ce4b2-117">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)
