---
title: Fonctions statiques globales de la fusion
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged global static functions [.NET Framework], fusion
- fusion global static functions [.NET Framework]
- global static functions [.NET Framework fusion]
ms.assetid: 229b2188-9168-4b44-a987-e1f515494688
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 86cb59c0935c193a9865d5ace5fe11c96226d9e8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697717"
---
# <a name="fusion-global-static-functions"></a>Fonctions statiques globales de la fusion
Cette section décrit les fonctions statiques globales non managées qui utilise l’API de fusion.  
  
## <a name="in-this-section"></a>Dans cette section  
 [ClearDownloadCache, fonction](../../../../docs/framework/unmanaged-api/fusion/cleardownloadcache-function.md)  
 Efface le global assembly cache d’assemblys téléchargés.  
  
 [CompareAssemblyIdentity, fonction](../../../../docs/framework/unmanaged-api/fusion/compareassemblyidentity-function.md)  
 Compare deux identités d’assembly pour déterminer s’ils sont équivalents.  
  
 [CreateApplicationContext, fonction](../../../../docs/framework/unmanaged-api/fusion/createapplicationcontext-function.md)  
 Interne uniquement. (Cette fonction prend en charge l’infrastructure .NET Framework et n’est pas destinée à être utilisée directement depuis votre code.)  
  
 [CreateAssemblyCache, fonction](../../../../docs/framework/unmanaged-api/fusion/createassemblycache-function.md)  
 Obtient un pointeur vers un nouveau [IAssemblyCache](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md) instance qui représente le global assembly cache.  
  
 [CreateAssemblyEnum, fonction](../../../../docs/framework/unmanaged-api/fusion/createassemblyenum-function.md)  
 Obtient un pointeur vers un [IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md) instance qui représente une liste d’objets qui existent dans l’assembly spécifié.  
  
 [CreateAssemblyNameObject, fonction](../../../../docs/framework/unmanaged-api/fusion/createassemblynameobject-function.md)  
 Obtient un pointeur vers un [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) instance qui représente l’identité unique de l’assembly avec le nom spécifié.  
  
 [CreateHistoryReader, fonction](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)  
 Crée un lecteur de l’historique pour le fichier spécifié.  
  
 [CreateInstallReferenceEnum, fonction](../../../../docs/framework/unmanaged-api/fusion/createinstallreferenceenum-function.md)  
 Obtient un pointeur vers un [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance qui représente une liste de références d’une application à l’assembly spécifié.  
  
 [GetAppIdAuthority, fonction](../../../../docs/framework/unmanaged-api/fusion/getappidauthority-function.md)  
 Obtient un pointeur vers un [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance qui gère des clés pour les identités d’application et les références.  
  
 [GetAssemblyIdentityFromFile, fonction](../../../../docs/framework/unmanaged-api/fusion/getassemblyidentityfromfile-function.md)  
 Obtient un pointeur vers un `IUnknown` objet avec la valeur `IID` dans l’assembly dans le chemin de fichier spécifié.  
  
 [GetCachePath, fonction](../../../../docs/framework/unmanaged-api/fusion/getcachepath-function.md)  
 Obtient le chemin d’accès à l’assembly mis en cache, à l’aide des indicateurs spécifiés.  
  
 [GetHistoryFileDirectory, fonction](../../../../docs/framework/unmanaged-api/fusion/gethistoryfiledirectory-function.md)  
 Récupère le chemin d’accès du répertoire de l’historique de l’application.  
  
 [GetIdentityAuthority, fonction](../../../../docs/framework/unmanaged-api/fusion/getidentityauthority-function.md)  
 Obtient un pointeur vers un [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance qui gère des clés pour les objets de code.  
  
 [IsFrameworkAssembly, fonction](../../../../docs/framework/unmanaged-api/fusion/isframeworkassembly-function.md)  
 Obtient une valeur qui indique si l’assembly spécifié est géré.  
  
 [NukeDownloadedCache, fonction](../../../../docs/framework/unmanaged-api/fusion/nukedownloadedcache-function.md)  
 Supprime le cache de téléchargement du common language runtime.  
  
 [PreBindAssemblyEx, fonction](../../../../docs/framework/unmanaged-api/fusion/prebindassemblyex-function.md)  
 Obtient le nom complet de la stratégie après d’un assembly.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
  
 [Énumérations de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)  
  
 [Structures de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)  
  
 [Global Assembly Cache](../../../../docs/framework/app-domains/gac.md)
