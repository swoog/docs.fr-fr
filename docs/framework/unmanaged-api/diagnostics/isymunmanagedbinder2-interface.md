---
title: ISymUnmanagedBinder2, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder2 Interface
helpviewer_keywords:
- ISymUnmanagedBinder2 interface [.NET Framework debugging]
ms.assetid: 7a59f405-73e8-4434-8bcc-a9dc45ea08e6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 52b0f6b9d3e0ea3d6fe5f14badb8401b1a0c2c63
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187490"
---
# <a name="isymunmanagedbinder2-interface"></a>ISymUnmanagedBinder2, interface
Représente un classeur de symboles du code non managé et étend le [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.  
  
> [!IMPORTANT]
>  Il est un risque de sécurité pour ouvrir un fichier du programme (PDB) de la base de données à partir d’une source non fiable.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetReaderForFile2, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)|Une interface de métadonnées et un nom de fichier, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface qui lit les symboles de débogage associés au module. Fournit une recherche plus étendue que le [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) (méthode).|  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [ISymUnmanagedBinder, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 [ISymUnmanagedBinder3, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
