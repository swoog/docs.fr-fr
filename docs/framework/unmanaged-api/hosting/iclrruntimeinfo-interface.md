---
title: ICLRRuntimeInfo, interface
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo
helpviewer_keywords:
- ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 287e5ede-b3a7-4ef8-a756-4fca3f285a82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cc8225b6612c7bf07d220b20d515f64a346b9691
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436466"
---
# <a name="iclrruntimeinfo-interface"></a>ICLRRuntimeInfo, interface
Fournit des méthodes qui retournent des informations concernant un common language runtime (CLR), spécifique, y compris la version, le répertoire et l’état de charge. Cette interface fournit également des fonctionnalités spécifiques au runtime sans l’initialisation du runtime. Il inclut le relatifs au runtime [LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md) (méthode), l’exécution du module spécifique [GetProcAddress](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md) (méthode) et les interfaces fournies par le biais du [GetInterface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)(méthode).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[BindAsLegacyV2Runtime, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md)|Lie ce runtime pour toutes les décisions de stratégie CLR version 2 d’activation héritée.|  
|[GetDefaultStartupFlags, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getdefaultstartupflags-method.md)|Obtient les indicateurs de démarrage CLR et le fichier de configuration hôte.|  
|[GetInterface, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)|Charge le CLR dans le processus en cours et retourne des pointeurs d’interface runtime tels que [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md) et [IMetaDataDispenser](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md). Cette méthode remplace toutes les `CorBindTo*` fonctions.|  
|[GetProcAddress, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md)|Obtient l’adresse d’une fonction spécifiée qui a été exportée à partir du CLR associé à cette interface. Cette méthode remplace la [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) (méthode).|  
|[GetRuntimeDirectory, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md)|Obtient le répertoire d’installation du CLR associé à cette interface. Cette méthode remplace la [GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md) (méthode).|  
|[GetVersionString, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getversionstring-method.md)|Obtient les informations de version du common language runtime (CLR) associées à une donnée [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface. Cette méthode remplace la [GetRequestedRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md) et [GetRequestedRuntimeVersion](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md) méthodes.|  
|[IsLoadable, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloadable-method.md)|Indique si le runtime associé à cette interface peut être chargé dans le processus actuel, en tenant compte autres exécutions qui peuvent déjà être chargées dans le processus.|  
|[IsLoaded, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloaded-method.md)|Indique si le CLR associé à le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface est chargé dans un processus.|  
|[IsStarted, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isstarted-method.md)|Indique si le CLR qui est associé à la [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface a été démarré.|  
|[LoadErrorString, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loaderrorstring-method.md)|Traduit une valeur HRESULT dans un message d’erreur approprié pour la culture spécifiée. Cette méthode remplace la [LoadStringRC](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md) et [LoadStringRCEx](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md) méthodes.|  
|[LoadLibrary, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md)|Charge une bibliothèque à partir du répertoire de l’infrastructure du CLR représenté par une [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface. Cette méthode remplace la [LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md) (méthode).|  
|[SetDefaultStartupFlags, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-setdefaultstartupflags-method.md)|Définit les indicateurs de démarrage CLR et l’hôte de fichier de configuration.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
