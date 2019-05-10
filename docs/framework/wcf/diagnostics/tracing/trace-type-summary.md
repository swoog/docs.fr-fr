---
title: Liste des types de suivis
ms.date: 03/30/2017
ms.assetid: e639410b-d1d1-479c-b78e-a4701d4e4085
ms.openlocfilehash: 44446b58510e58758934a5eb964efc8643854879
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64647190"
---
# <a name="trace-type-summary"></a>Liste des types de suivis
[Niveaux de source](https://go.microsoft.com/fwlink/?LinkID=94943) définit différents niveaux de suivi : Critique, erreur, avertissement, Information et Verbose, et fournit une description de la `ActivityTracing` indicateur qui active ou désactive la sortie de traçage des événements de transfert de limite et d’activité.  
  
 Vous pouvez également consulter [TraceEventType](https://go.microsoft.com/fwlink/?LinkId=95169) pour les types de suivis qui peuvent être émis à partir de <xref:System.Diagnostics>.  
  
 Le tableau suivant répertorie les plus importants.  
  
|Type de suivi|Description|  
|----------------|-----------------|  
|Critique|Erreur irrécupérable ou panne d'application.|  
|Error|Erreur récupérable.|  
|Warning|Message d'informations.|  
|Information|Problème non critique.|  
|Verbose|Suivi de débogage.|  
|Start|Démarrage d'une unité logique de traitement.|  
|Interrompre|Interruption d'une unité logique de traitement.|  
|Reprendre|Reprise d'une unité logique de traitement.|  
|Arrêter|Arrêt d'une unité logique de traitement.|  
|Transférer|Changement d'identité de corrélation.|  
  
 Une activité est définie comme une combinaison des types de suivi ci-dessus.  
  
 Le code suivant est une expression régulière qui définit une activité idéale dans une étendue locale (source de suivi).  
  
 `R = Start (Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop`  
  
 Cela signifie qu'une activité doit remplir les conditions suivantes.  
  
- Elle doit respectivement démarrer et s'arrêter avec les suivis Démarrer et Arrêter.  
  
- Elle doit contenir un suivi Transfert immédiatement avant un suivi Interrompre ou Reprendre.  
  
- Elle ne doit pas contenir de suivi entre les suivis Interrompre et Reprendre, s'ils existent.  
  
- Elle peut contenir n'importe quel type de suivi Critique/Avertissement/Informations/Commentaires/Transfert, en nombre illimité, tant que les conditions précédentes sont observées.  
  
 Le code suivant est une expression régulière qui définit une activité idéale dans la portée globale,  
  
```  
R+   
```  
  
 R étant l'expression régulière d'une activité dans l'étendue locale. Cela se traduit par :  
  
```  
[R+ = Start ( Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop]+  
```
