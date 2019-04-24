---
ms.openlocfilehash: a6f93bbdf39a1b525e2daeb12afc3a6392a66e30
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59235383"
---
### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>La désérialisation des objets MailMessage sérialisés sous .NET Framework 4.5 peut échouer

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, les objets <xref:System.Web.Mail.MailMessage> peuvent inclure des caractères non-ASCII. Dans le .NET Framework 4, seuls les caractères ASCII sont pris en charge. Les objets <xref:System.Web.Mail.MailMessage> qui contiennent des caractères non-ASCII et qui sont sérialisés sous .NET Framework 4.5 ou ultérieur ne peuvent pas être désérialisés dans .NET Framework 4.|
|Suggestion|Vérifiez que votre code assure la gestion des exceptions lors de la désérialisation d’un objet <xref:System.Web.Mail.MailMessage>.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|
