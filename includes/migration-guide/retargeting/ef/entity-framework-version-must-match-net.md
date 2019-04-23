---
ms.openlocfilehash: 4c6a89f9753989a5ad061e847dff70d2af0b3cf4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774342"
---
### <a name="entity-framework-version-must-match-the-net-framework-version"></a>La version d’Entity Framework doit correspondre à la version du .NET Framework

|   |   |
|---|---|
|Détails|La version d’Entity Framework doit être mise en correspondance avec la version du .NET Framework. Entity Framework 5 est recommandé pour .NET Framework 4.5. Il existe certains problèmes connus avec EF 4.x dans un projet .NET Framework 4.5 concernant <xref:System.ComponentModel.DataAnnotations>. Dans .NET 4.5, les annotations ont été déplacées vers un autre assembly. De ce fait, la détermination des annotations à utiliser pose problème.|
|Suggestion|Mise à niveau vers Entity Framework 5 pour .NET Framework 4.5|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|
