---
title: ICLRDebuggingLibraryProvider::ProvideLibrary, méthode
ms.date: 03/30/2017
api_name:
- ICLRDebuggingLibraryProvider.ProvideLibrary Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebuggingLibraryProvider::ProvideLibrary
helpviewer_keywords:
- ProvideLibrary method [.NET Framework debugging]
- ICLRDebuggingLibraryProvider::ProvideLibrary method [.NET Framework debugging]
ms.assetid: 86f06245-9517-49be-8d8c-ca5deaf34c02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5f66d91434fd92ff80bb17e04bf38bb0b631e819
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55825496"
---
# <a name="iclrdebugginglibraryproviderprovidelibrary-method"></a>ICLRDebuggingLibraryProvider::ProvideLibrary, méthode
Obtient un fournisseur de bibliothèque interface de rappel qui permet de common language runtime (CLR) des bibliothèques de débogage spécifiques à la version être à la demande et le chargement.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ProvideLibrary(  
     [in] const WCHAR* pwszFileName,  
     [in] DWORD dwTimestamp,  
     [in] DWORD dwSizeOfImage,  
     [out] HMODULE* hModule);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pwszFilename`  
 [in] Nom du module demandé.  
  
 `dwTimestamp`  
 [in] L’horodatage stockée dans l’en-tête du fichier COFF de fichiers PE.  
  
 `pLibraryProvider`  
 [in] Le `SizeOfImage` champ stocké dans l’en-tête de fichier facultatif COFF de fichiers PE.  
  
 `hModule`  
 [out] Le handle du module demandé.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
  
## <a name="exceptions"></a>Exceptions  
  
## <a name="remarks"></a>Notes  
 `ProvideLibrary` permet au débogueur de fournir des modules qui sont nécessaires pour le débogage de fichiers CLR spécifiques tels que mscordbi.dll et mscordacwks.dll. Les handles de module doivent rester valides tant qu’un appel à la [ICLRDebugging::CanUnloadNow](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-canunloadnow-method.md) méthode indique qu’ils peuvent être libérés, à quel point il est responsable de l’appelant pour libérer les handles.  
  
 Le débogueur peut utiliser tous les moyens pour rechercher ou obtenir le module de débogage.  
  
> [!IMPORTANT]
>  Cette fonctionnalité permet à l’appelant de l’API de fournir des modules qui contiennent du code exécutable et potentiellement malveillant. Par mesure de sécurité, l’appelant ne doit pas utiliser `ProvideLibrary` distribuer n’importe quel code qu’il n’est pas prêt à s’exécuter.  
>   
>  Si un problème de sécurité sérieux est découvert dans une bibliothèque déjà libérée, tels que mscordbi.dll ou mscordacwks.dll, le shim peut être corrigé pour reconnaître les mauvaises versions des fichiers. Le shim peut ensuite émettre des demandes pour les versions corrigées des fichiers et rejeter les mauvaises versions si elles sont fournies en réponse à toute demande. Cela peut se produire uniquement si l’utilisateur a corrigé vers une nouvelle version du shim. Versions non corrigées restent vulnérables.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
