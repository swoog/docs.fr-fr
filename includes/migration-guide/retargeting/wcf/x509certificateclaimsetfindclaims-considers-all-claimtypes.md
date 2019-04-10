---
ms.openlocfilehash: 878aef544b2706bfd10a3dddce1b902655ef003a
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760988"
---
### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims prend en compte tous les claimTypes

|   |   |
|---|---|
|Détails|Dans les applications qui ciblent .NET Framework 4.6.1, si un ensemble de revendications X509 est initialisé à partir d’un certificat dont le champ SAN a plusieurs entrées DNS, la méthode <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> tente de faire correspondre l’argument claimType avec toutes les entrées DNS. Pour les applications qui ciblent des versions antérieures du .NET Framework, la méthode <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> tente de faire correspondre l’argument claimType uniquement avec la dernière entrée DNS.|
|Suggestion|Cette modification affecte uniquement les applications qui ciblent le .NET Framework 4.6.1. Elle peut être désactivée (ou activée si vous ciblez une version antérieure à 4.6.1) avec le commutateur de compatibilité [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Portée|Mineur|
|Version|4.6.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

