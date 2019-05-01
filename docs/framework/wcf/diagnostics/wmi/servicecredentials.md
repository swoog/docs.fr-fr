---
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: d9563bd3bfe067ad83bfa03e7c6375a9db933f14
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61956977"
---
# <a name="servicecredentials"></a>ServiceCredentials
ServiceCredentials  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceCredentials ne définit aucune méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceCredentials a les propriétés suivantes :  
  
### <a name="clientcertificate"></a>ClientCertificate  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres d'authentification et d'approvisionnement des certificats clients pour ce service.  
  
### <a name="issuedtokenauthentication"></a>IssuedTokenAuthentication  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres actuels d'authentification de jeton émis pour ce service.  
  
### <a name="peer"></a>Peer  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Authentification des informations d'identification actuelles et fourniture des paramètres à utiliser par les points de terminaison de transport d'homologue.  
  
### <a name="secureconversationauthentication"></a>SecureConversationAuthentication  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie les paramètres actuels de conversation sécurisée.  
  
### <a name="servicecertificate"></a>ServiceCertificate  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Certificat associé à ce service.  
  
### <a name="usernameauthentication"></a>UserNameAuthentication  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres de nom d'utilisateur/mot de passe pour ce service.  
  
### <a name="windowsauthentication"></a>WindowsAuthentication  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Paramètres d'authentification Windows pour ce service.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Description.ServiceCredentials>
