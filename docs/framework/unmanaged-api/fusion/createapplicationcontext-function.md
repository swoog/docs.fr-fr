---
title: CreateApplicationContext, fonction
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d98829b29100824e5d606e23aaf287c9f6e81d69
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59170961"
---
# <a name="createapplicationcontext-function"></a>CreateApplicationContext, fonction
Cette fonction prend en charge l’infrastructure .NET Framework et n’est pas destinée à être utilisée directement depuis votre code.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
## <a name="parameters"></a>Paramètres  
 `pName`  
 [in] Pointeur vers un nom convivial.  
  
 `ppCtx`  
 [out] Pointeur vers un contexte d’application.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans le fichier Fusion.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IAssemblyCache, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
- [Fonctions statiques globales de la fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
- [Global Assembly Cache](../../../../docs/framework/app-domains/gac.md)
