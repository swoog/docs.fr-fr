---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 923c85a9dff11753a338fcfd3673d3590fca607a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196747"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a>ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode
Définit le langage intermédiaire de décalage pour le gestionnaire catch généré par le compilateur qui encapsule une méthode async.  
  
 L’offset IL de la capture générée est utilisé par le débogueur pour gérer les captures comme s’il s’agissait d’un code non utilisateur même si elle peut se produire dans une méthode de code utilisateur. En particulier, il est utilisé en réponse à une **CatchHandlerFound** événement d’exception.  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
## <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne `HRESULT`.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedAsyncMethodPropertiesWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
