---
title: ISymUnmanagedReader2, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2
helpviewer_keywords:
- ISymUnmanagedReader2 interface [.NET Framework debugging]
ms.assetid: a01a881b-82a3-4b3e-a3a9-9dc305c2e5f7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 890053e1bf2e0648a41cca718e94edcf21c7e612
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59165982"
---
# <a name="isymunmanagedreader2-interface"></a>ISymUnmanagedReader2, interface
Représente un lecteur de symboles qui fournit l’accès aux documents, des méthodes et des variables dans un magasin de symboles. Cette interface étend la [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetMethodByVersionPreRemap, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodbyversionpreremap-method.md)|Obtenir une méthode de lecteur de symboles, étant donné un jeton de méthode et un numéro de version modifier et continuer.|  
|[GetMethodsInDocument, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodsindocument-method.md)|Obtient toutes les méthodes ayant des informations de ligne dans le document fourni.|  
|[GetSymAttributePreRemap, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getsymattributepreremap-method.md)|Obtient un attribut personnalisé en fonction de son nom.|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
