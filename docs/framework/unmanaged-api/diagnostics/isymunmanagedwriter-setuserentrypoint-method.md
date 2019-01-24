---
title: ISymUnmanagedWriter::SetUserEntryPoint, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetUserEntryPoint
helpviewer_keywords:
- ISymUnmanagedWriter::SetUserEntryPoint method [.NET Framework debugging]
- SetUserEntryPoint method [.NET Framework debugging]
ms.assetid: d4dcc575-3ac8-4453-9be1-2b24f47363d7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7595b4a69dd327e448aade1e2dcba06100e55bf4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638679"
---
# <a name="isymunmanagedwritersetuserentrypoint-method"></a><span data-ttu-id="833fa-102">ISymUnmanagedWriter::SetUserEntryPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="833fa-102">ISymUnmanagedWriter::SetUserEntryPoint Method</span></span>
<span data-ttu-id="833fa-103">Spécifie la méthode définie par l’utilisateur qui est le point d’entrée pour ce module.</span><span class="sxs-lookup"><span data-stu-id="833fa-103">Specifies the user-defined method that is the entry point for this module.</span></span> <span data-ttu-id="833fa-104">Par exemple, ce point d’entrée peut être la méthode de l’utilisateur principal au lieu de stubs générés par le compilateur avant principal.</span><span class="sxs-lookup"><span data-stu-id="833fa-104">For example, this entry point could be the user's main method instead of compiler-generated stubs before main.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="833fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833fa-105">Syntax</span></span>  
  
```  
HRESULT SetUserEntryPoint(  
    [in] mdMethodDef entryMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="833fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833fa-106">Parameters</span></span>  
 `entryMethod`  
 <span data-ttu-id="833fa-107">[in] Jeton de métadonnées pour la méthode qui est l’entrée utilisateur point.</span><span class="sxs-lookup"><span data-stu-id="833fa-107">[in] The metadata token for the method that is the user entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="833fa-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="833fa-108">Return Value</span></span>  
 <span data-ttu-id="833fa-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="833fa-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="833fa-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="833fa-110">Requirements</span></span>  
 <span data-ttu-id="833fa-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="833fa-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="833fa-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833fa-112">See also</span></span>
- [<span data-ttu-id="833fa-113">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="833fa-113">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
