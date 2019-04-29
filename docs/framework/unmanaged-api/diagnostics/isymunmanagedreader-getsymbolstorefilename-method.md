---
title: ISymUnmanagedReader::GetSymbolStoreFileName, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetSymbolStoreFileName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetSymbolStoreFileName
helpviewer_keywords:
- GetSymbolStoreFileName method [.NET Framework debugging]
- ISymUnmanagedReader::GetSymbolStoreFileName method [.NET Framework debugging]
ms.assetid: c84f4846-9bc8-44a4-9a76-e39106d6d8b2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 147b33a3f49f9163daea776779ca26f62561a84e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670012"
---
# <a name="isymunmanagedreadergetsymbolstorefilename-method"></a><span data-ttu-id="53202-102">ISymUnmanagedReader::GetSymbolStoreFileName, méthode</span><span class="sxs-lookup"><span data-stu-id="53202-102">ISymUnmanagedReader::GetSymbolStoreFileName Method</span></span>
<span data-ttu-id="53202-103">Fournit le nom de fichier sur disque du magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="53202-103">Provides the on-disk file name of the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53202-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53202-104">Syntax</span></span>  
  
```  
HRESULT GetSymbolStoreFileName (  
    [in]  ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is (cchName),  
        length_is (*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="53202-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53202-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="53202-106">[in] La taille de la `szName` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="53202-106">[in] The size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="53202-107">[out] Un pointeur vers la variable qui reçoit la longueur du nom retourné dans `szName`, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="53202-107">[out] A pointer to the variable that receives the length of the name returned in `szName`, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="53202-108">[out] Pointeur vers la variable qui reçoit le nom de fichier du magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="53202-108">[out] A pointer to the variable that receives the file name of the symbol store.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="53202-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="53202-109">Return Value</span></span>  
 <span data-ttu-id="53202-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="53202-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53202-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53202-111">Requirements</span></span>  
 <span data-ttu-id="53202-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="53202-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53202-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53202-113">See also</span></span>

- [<span data-ttu-id="53202-114">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="53202-114">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
