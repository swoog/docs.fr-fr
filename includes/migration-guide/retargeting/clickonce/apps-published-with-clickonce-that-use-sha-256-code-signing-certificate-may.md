---
ms.openlocfilehash: bc56a3437e16e5d2c9679847bf3a3035b9e34286
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774350"
---
### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Les applications publiées avec ClickOnce qui utilisent un certificat de signature de code SHA-256 peuvent échouer sur Windows 2003

|   |   |
|---|---|
|Détails|L'exécutable est signé avec SHA256. Auparavant, il était signé avec SHA1, que le certificat de signature du code ait été SHA-1 ou SHA-256. Cela s'applique à :<ul><li>Toutes les applications générées avec Visual Studio 2012 ou ultérieur.</li><li>Toutes les applications générées avec Visual Studio 2010 ou antérieur en présence de .NET Framework 4.5.</li></ul>En outre, si .NET Framework 4.5 (ou une version ultérieure) est présent, le manifeste ClickOnce est également signé avec SHA-256 pour les certificats SHA-256, quelle que soit la version du .NET Framework sur laquelle il a été compilé.|
|Suggestion|Le changement de signature de l’exécutable ClickOnce affecte uniquement les systèmes Windows Server 2003. Vous devez installer le correctif logiciel KB 938397. Le changement de signature du manifeste avec l’algorithme SHA-256 même quand une application cible .NET Framework 4.0 ou des versions antérieures présente une dépendance de runtime sur .NET Framework 4.5 ou une version ultérieure.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
