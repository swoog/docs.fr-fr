---
title: Le nom de source spécifié dans le journal est inscrit auprès d’un journal autre que celui spécifié dans EventLogName
ms.date: 07/20/2015
ms.assetid: 7317e100-098b-408d-86e5-7c74cf8558c7
ms.openlocfilehash: 03fcc41b0fbb84233aa037d7af17d168050a98b6
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45512892"
---
# <a name="source-name-specified-in-eventlogsource-is-registered-to-a-log-other-than-that-specified-in-eventlogname"></a>Le nom de source spécifié dans le journal est inscrit auprès d’un journal autre que celui spécifié dans EventLogName
Le `EventLog` essaie de faire référence à une source qui est inscrite auprès d’un autre journal. Si vous écrivez des entrées dans le journal des événements, vous devez spécifier la propriété <xref:System.Diagnostics.EventLog.Source%2A> . La propriété <xref:System.Diagnostics.EventLog.Source%2A> inscrit votre composant auprès du journal des événements comme source d’entrées valide. Une même source ne peut être associée (et donc écrire des entrées) qu’à un seul journal des événements à la fois.  
  
 Par défaut, si vous tentez d’écrire une entrée sans avoir d’abord inscrit votre composant en tant que source valide, le système inscrit automatiquement la source auprès du journal des événements, en utilisant la valeur de la propriété <xref:System.Diagnostics.EventLog.Source%2A> comme chaîne source.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Vérifiez que la source est inscrite auprès du journal approprié. Pour ce faire, utilisez la méthode <xref:System.Diagnostics.EventLog.CreateEventSource%2A> ou l’une de ses surcharges pour spécifier une chaîne qui identifie votre composant auprès du journal des événements.  
  
## <a name="see-also"></a>Voir aussi  
 [Administration des journaux des événements](https://msdn.microsoft.com/library/35f53238-bdd2-417b-acd8-2fd9f7397f18)  
 [Références du journal des événements](https://msdn.microsoft.com/library/4af0661c-6c96-49f4-961d-b26ed9bc3e87)  
 [Comment : ajouter votre Application en tant que Source d’entrées de journal des événements](https://msdn.microsoft.com/library/948ff920-a739-4e66-a191-ee951512d42c)  
 [Comment : supprimer une Source d’événement](https://msdn.microsoft.com/library/bc66c900-4b8a-426a-b8e2-17031a20167e)
