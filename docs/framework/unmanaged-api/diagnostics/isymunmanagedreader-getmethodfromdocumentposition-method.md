---
title: ISymUnmanagedReader::GetMethodFromDocumentPosition, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodFromDocumentPosition
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodFromDocumentPosition
helpviewer_keywords:
- GetMethodFromDocumentPosition method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodFromDocumentPosition method [.NET Framework debugging]
ms.assetid: 55773dbc-9053-46e3-8a3c-86caa9d91fb4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ed13397748b2668c275b221e38bd75c0dd37f03
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197696"
---
# <a name="isymunmanagedreadergetmethodfromdocumentposition-method"></a><span data-ttu-id="7f800-102">ISymUnmanagedReader::GetMethodFromDocumentPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="7f800-102">ISymUnmanagedReader::GetMethodFromDocumentPosition Method</span></span>
<span data-ttu-id="7f800-103">Retourne la méthode qui contient le point d’arrêt à la position donnée dans un document.</span><span class="sxs-lookup"><span data-stu-id="7f800-103">Returns the method that contains the breakpoint at the given position in a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f800-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f800-104">Syntax</span></span>  
  
```  
HRESULT GetMethodFromDocumentPosition (  
    [in]  ISymUnmanagedDocument*  document,  
    [in]  ULONG32  line,  
    [in]  ULONG32  column,  
    [out, retval] ISymUnmanagedMethod**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f800-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f800-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="7f800-106">[in] Le document spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f800-106">[in] The specified document.</span></span>  
  
 `line`  
 <span data-ttu-id="7f800-107">[in] La ligne du document spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f800-107">[in] The line of the specified document.</span></span>  
  
 `column`  
 <span data-ttu-id="7f800-108">[in] La colonne du document spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f800-108">[in] The column of the specified document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="7f800-109">[out] Un pointeur vers l’adresse d’un [ISymUnmanagedMethod, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) objet qui représente la méthode contenant le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7f800-109">[out] A pointer to the address of a [ISymUnmanagedMethod Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) object that represents the method containing the breakpoint.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f800-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7f800-110">Return Value</span></span>  
 <span data-ttu-id="7f800-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f800-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f800-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f800-112">Requirements</span></span>  
 <span data-ttu-id="7f800-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7f800-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f800-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f800-114">See also</span></span>

- [<span data-ttu-id="7f800-115">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="7f800-115">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
