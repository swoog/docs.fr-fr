---
ms.openlocfilehash: 380f662349a8dcd04e5bf445e1479d0a32d5861f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235300"
---
### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer ne parvient pas à désérialiser un ConcurrentDictionary sérialisé avec une autre version de .NET

|   |   |
|---|---|
|Détails|Par conception, <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> peut être utilisé uniquement si les extrémités de sérialisation et de désérialisation partagent toutes deux les mêmes types CLR. Par conséquent, il n’est pas garanti qu’un objet sérialisé avec une certaine version de .NET Framework puisse être désérialisé par une autre version.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> est un type qui est connu pour ne pas désérialiser correctement si la sérialisation est effectuée avec .NET Framework 4.5 ou version antérieure et la désérialisation avec .NET Framework 4.5.1 ou version ultérieure.|
|Suggestion|Il existe un certain nombre de solutions de contournement possibles à ce problème :<ul><li>Mettez à niveau l’ordinateur de sérialisation pour utiliser également .NET Framework 4.5.1.</li><li>Utilisez <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> au lieu de <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>, car il n’attend pas les mêmes types CLR à la fois aux extrémités de sérialisation et de désérialisation.</li><li>Utilisez <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> au lieu de <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>, car il ne présente pas cette rupture particulière entre 4.5-&gt;4.5.1.</li></ul>|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|
