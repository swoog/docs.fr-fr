---
ms.openlocfilehash: a6f93bbdf39a1b525e2daeb12afc3a6392a66e30
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235383"
---
### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>La désérialisation des objets MailMessage sérialisés sous .NET Framework 4.5 peut échouer

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, les objets <xref:System.Web.Mail.MailMessage> peuvent inclure des caractères non-ASCII. Dans le .NET Framework 4, seuls les caractères ASCII sont pris en charge. <xref:System.Web.Mail.MailMessage> Les objets contenant des caractères hors ASCII et sérialisés dans .NET Framework 4.5 ou une version ultérieure ne sont pas désérialisables dans .NET Framework 4.|
|Suggestion|Vérifiez que votre code assure la gestion des exceptions lors de la désérialisation d’un objet <xref:System.Web.Mail.MailMessage>.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|
