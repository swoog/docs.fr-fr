---
title: 'Comment : définir la stratégie de cache à durée définie par défaut pour une application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time-based cache policies
- cache [.NET Framework], time-based policies
- default time-based cache policy
ms.assetid: 6bfce066-a2e7-4add-a05e-85c12ec9f07f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 1e08026f8d1ec8b39f7ef3c2c34efad9e51b8fe9
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47235700"
---
# <a name="how-to-set-the-default-time-based-cache-policy-for-an-application"></a>Comment : définir la stratégie de cache à durée définie par défaut pour une application
Avec la stratégie de cache basée sur la durée par défaut, le comportement de cache d’une application est déterminé par les en-têtes envoyés avec la ressource en cache et par le comportement du cache défini dans les sections 13 et 14 du document RFC 2616, disponible à l’adresse [http://www.ietf.org](http://www.ietf.org/). Ce comportement de cache convient à la plupart des applications.  
  
### <a name="to-set-the-default-automatic-policy-for-an-application"></a>Pour utiliser automatiquement la stratégie par défaut pour une application  
  
1.  Créez une stratégie basée sur la durée par défaut.  
  
2.  Définissez cette stratégie comme stratégie par défaut pour le domaine d’application.  
  
## <a name="example"></a>Exemple  
 Les deux exemples de cette section créent des stratégies identiques.  
  
 L’exemple suivant crée une stratégie basée sur la durée par défaut et la définit comme stratégie par défaut pour le domaine d’application.  
  
```csharp  
public static void SetDefaultTimeBasedPolicy ()  
{  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy ();  
    HttpWebRequest.DefaultCachePolicy = policy ;  
}  
```  
  
```vb  
Public Shared Sub SetDefaultTimeBasedPolicy ()  
    Dim policy = New HttpRequestCachePolicy ()  
    HttpWebRequest.DefaultCachePolicy = policy  
End Sub  
```  
  
 Vous pouvez également créer une stratégie de cache basée sur la durée par défaut à l’aide la classe <xref:System.Net.Cache.RequestCachePolicy>, comme indiqué dans l’exemple suivant :  
  
```csharp  
public static void SetDefaultTimeBasedPolicy2()  
{  
    RequestCachePolicy policy = new RequestCachePolicy ();  
    HttpWebRequest.DefaultCachePolicy = policy ;  
}  
```  
  
```vb  
Public Shared Sub SetDefaultTimeBasedPolicy2()  
    Dim policy As New RequestCachePolicy()  
    HttpWebRequest.DefaultCachePolicy = policy  
End Sub  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Gestion du cache pour les applications réseau](../../../docs/framework/network-programming/cache-management-for-network-applications.md)  
 [Stratégie de cache](../../../docs/framework/network-programming/cache-policy.md)  
 [Stratégies de cache basées sur l’emplacement](../../../docs/framework/network-programming/location-based-cache-policies.md)  
 [Stratégies de cache basées sur la durée](../../../docs/framework/network-programming/time-based-cache-policies.md)  
 [\<requestCaching>, élément (paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)
