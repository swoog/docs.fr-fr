---
title: GetCORVersion, fonction
ms.date: 03/30/2017
api_name:
- GetCORVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetCORVersion
helpviewer_keywords:
- GetCORVersion function [.NET Framework hosting]
ms.assetid: 2f09cd37-bf3a-4cc5-87b0-adc42a7eed31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0741e5773b946186a452e191cc3ae987e6067c44
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54606885"
---
# <a name="getcorversion-function"></a>GetCORVersion, fonction
Retourne le numéro de version du common language runtime (CLR) qui s’exécute dans le processus en cours.  
  
 Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCORVersion (  
    [in] LPWSTR  pbuffer,  
    [in]  DWORD   cchBuffer,   
    [out] DWORD*  dwlength  
);   
```  
  
#### <a name="parameters"></a>Paramètres  
 `pbuffer`  
 Un pointeur vers une mémoire tampon dans laquelle le CLR retourne une chaîne qui spécifie la version du runtime qui est actuellement chargé dans le processus. La chaîne retournée prend la même forme que les chaînes passées à [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), par exemple, « v1.0.1216 ». Si le runtime n’a pas encore été chargé dans le processus, la fonction retourne les informations de répertoire approprié pour la dernière version du runtime installée sur l’ordinateur.  
  
 `cchBuffer`  
 Le nombre de caractères (`WCHAR`s) qui peuvent être conservées dans `pbuffer`.  
  
 `dwLength`  
 Un pointeur vers le nombre de caractères réellement retournés dans `pbuffer`. Si `pbuffer` est un pointeur null, le runtime retourne E_POINTER. Si le nombre de caractères est supérieur puis la longueur de `pbuffer` , le runtime retourne ERROR_INSUFFICIENT_BUFFER.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Fonctions d’hébergement CLR dépréciées](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
