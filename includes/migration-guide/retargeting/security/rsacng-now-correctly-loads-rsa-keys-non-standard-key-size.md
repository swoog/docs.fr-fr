---
ms.openlocfilehash: 4892f75e4ae673d9d9cc7e9eeb6fb9b1a73f572e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803917"
---
### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>RSACng charge désormais correctement les clés RSA de taille de clé non standard

|   |   |
|---|---|
|Détails|Dans les versions du .NET Framework antérieures à 4.6.2, les clients avec des tailles de clé non standard pour les certificats RSA ne peuvent pas accéder à ces clés par le biais des méthodes d’extension <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> et <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>.  Une exception <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> est levée avec un message indiquant que &quot;la taille de clé demandée n’est pas prise en charge&quot;. Dans .NET Framework 4.6.2, ce problème a été résolu. De même, <xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)> et <xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)> fonctionnent désormais avec des tailles de clé non standard sans lever d’exception <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>.|
|Suggestion|S’il existe une logique de gestion des exceptions qui s’appuie sur le comportement précédent où un <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> est levé quand des tailles de clé non standard sont utilisées, supprimez la logique.|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|
