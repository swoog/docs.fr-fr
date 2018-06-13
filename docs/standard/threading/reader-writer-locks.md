---
title: Verrous de lecteur-writer
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- ReaderWriterLock class, about ReaderWriterLock class
- threading [.NET Framework], ReaderWriterLock class
ms.assetid: 8c71acf2-2c18-4f4d-8cdb-0728639265fd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f829fc0b399f5cfd10d98f6b7439de757674f11
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586371"
---
# <a name="reader-writer-locks"></a>Verrous de lecteur-writer
La classe <xref:System.Threading.ReaderWriterLockSlim> permet à plusieurs threads de lire simultanément une ressource, mais nécessite qu’un thread attende un verrou exclusif pour écrire dans la ressource.  
  
 Vous pouvez utiliser un <xref:System.Threading.ReaderWriterLockSlim> dans votre application pour fournir une synchronisation coopérative parmi les threads qui accèdent à une ressource partagée. Les verrous sont pris sur le <xref:System.Threading.ReaderWriterLockSlim> lui-même.  
  
 Comme avec tout mécanisme de synchronisation de threads, vous devez vous assurer qu’aucun thread ne contourne le verrouillage fourni par <xref:System.Threading.ReaderWriterLockSlim>. Une manière de le faire consiste à concevoir une classe qui encapsule la ressource partagée. Cette classe fournirait des membres qui accèdent à la ressource partagée privée et qui utilisent un <xref:System.Threading.ReaderWriterLockSlim> privé pour la synchronisation. Pour obtenir un exemple, consultez l’exemple de code pour la classe <xref:System.Threading.ReaderWriterLockSlim>. <xref:System.Threading.ReaderWriterLockSlim> est suffisamment efficace pour être utilisé dans le but de synchroniser des objets individuels.  
  
 Structurez votre application pour réduire la durée des opérations de lecture et d’écriture. Les opérations d’écriture longues affectent directement le débit, car le verrou en écriture est exclusif. Les opérations de lecture longues bloquent les writers en attente, et si au moins un thread attend l’accès en écriture, les threads qui demandent l’accès en lecture seront également bloqués.  
  
> [!NOTE]
>  Le [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] a deux verrous de lecteur-writer, à savoir <xref:System.Threading.ReaderWriterLockSlim> et <xref:System.Threading.ReaderWriterLock>. <xref:System.Threading.ReaderWriterLockSlim> est recommandé pour tout nouveau développement. <xref:System.Threading.ReaderWriterLockSlim> est similaire à <xref:System.Threading.ReaderWriterLock>, mais a des règles simplifiées pour la récursivité ainsi que la mise à niveau et la rétrogradation de l’état de verrou. <xref:System.Threading.ReaderWriterLockSlim> évite de nombreux cas d’interblocage potentiel. En outre, les performances de <xref:System.Threading.ReaderWriterLockSlim> sont considérablement meilleures que celles de <xref:System.Threading.ReaderWriterLock>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.ReaderWriterLockSlim>  
 <xref:System.Threading.ReaderWriterLock>  
 [Thread](../../../docs/standard/threading/index.md)  
 [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)
