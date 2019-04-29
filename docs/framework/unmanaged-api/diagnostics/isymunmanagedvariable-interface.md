---
title: ISymUnmanagedVariable, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable
helpviewer_keywords:
- ISymUnmanagedVariable interface [.NET Framework debugging]
ms.assetid: 704c69ba-77bc-40d7-8c0c-400061686321
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 712eca7f3f9fec9c81e638802f5a664ec6469d53
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797477"
---
# <a name="isymunmanagedvariable-interface"></a><span data-ttu-id="dd3b0-102">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="dd3b0-102">ISymUnmanagedVariable Interface</span></span>
<span data-ttu-id="dd3b0-103">Représente une variable, comme un paramètre, une variable locale ou un champ.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-103">Represents a variable, such as a parameter, a local variable, or a field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dd3b0-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dd3b0-104">Methods</span></span>  
  
|<span data-ttu-id="dd3b0-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-105">Method</span></span>|<span data-ttu-id="dd3b0-106">Description</span><span class="sxs-lookup"><span data-stu-id="dd3b0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dd3b0-107">GetAddressField1, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-107">GetAddressField1 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield1-method.md)|<span data-ttu-id="dd3b0-108">Obtient le premier champ d’adresse pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-108">Gets the first address field for this variable.</span></span> <span data-ttu-id="dd3b0-109">Sa signification dépend du type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-109">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="dd3b0-110">GetAddressField2, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-110">GetAddressField2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield2-method.md)|<span data-ttu-id="dd3b0-111">Obtient le deuxième champ d’adresse pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-111">Gets the second address field for this variable.</span></span> <span data-ttu-id="dd3b0-112">Sa signification dépend du type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-112">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="dd3b0-113">GetAddressField3, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-113">GetAddressField3 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield3-method.md)|<span data-ttu-id="dd3b0-114">Obtient le troisième champ d’adresse pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-114">Gets the third address field for this variable.</span></span> <span data-ttu-id="dd3b0-115">Sa signification dépend du type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-115">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="dd3b0-116">GetAddressKind, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-116">GetAddressKind Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)|<span data-ttu-id="dd3b0-117">Obtient le type d’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-117">Gets the kind of address of this variable.</span></span>|  
|[<span data-ttu-id="dd3b0-118">GetAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-118">GetAttributes Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getattributes-method.md)|<span data-ttu-id="dd3b0-119">Obtient les indicateurs d’attribut pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-119">Gets the attribute flags for this variable.</span></span>|  
|[<span data-ttu-id="dd3b0-120">GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-120">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getendoffset-method.md)|<span data-ttu-id="dd3b0-121">Obtient l’offset de fin de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-121">Gets the end offset of this variable within its parent.</span></span>|  
|[<span data-ttu-id="dd3b0-122">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-122">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getname-method.md)|<span data-ttu-id="dd3b0-123">Obtient le nom de cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-123">Gets the name of this variable.</span></span>|  
|[<span data-ttu-id="dd3b0-124">GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-124">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getsignature-method.md)|<span data-ttu-id="dd3b0-125">Obtient la signature de cette variable.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-125">Gets the signature of this variable.</span></span>|  
|[<span data-ttu-id="dd3b0-126">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="dd3b0-126">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getstartoffset-method.md)|<span data-ttu-id="dd3b0-127">Obtient l’offset de début de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-127">Gets the start offset of this variable within its parent.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="dd3b0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd3b0-128">Requirements</span></span>  
 <span data-ttu-id="dd3b0-129">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="dd3b0-129">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd3b0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd3b0-130">See also</span></span>

- [<span data-ttu-id="dd3b0-131">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="dd3b0-131">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
