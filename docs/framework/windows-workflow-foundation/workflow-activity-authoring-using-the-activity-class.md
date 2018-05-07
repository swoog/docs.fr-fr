---
title: Création de l'activité de workflow à l'aide de la classe d'activité
ms.date: 03/30/2017
ms.assetid: 7b7b1c66-f093-43c3-b4d1-7173b46516da
ms.openlocfilehash: 040fe777e332efdfb296e6fb6565935f466ded71
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="workflow-activity-authoring-using-the-activity-class"></a>Création de l'activité de workflow à l'aide de la classe d'activité
La façon la plus simple de créer une activité à l’aide de Windows Workflow Foundation (WF) dans [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] consiste à créer une classe qui hérite de <xref:System.Activities.Activity> qui crée des fonctionnalités en assemblant personnalisé activités ou les activités à partir de la [intégrés Bibliothèque d’activités](../../../docs/framework/windows-workflow-foundation/net-framework-4-5-built-in-activity-library.md). Cette rubrique montre comment créer une activité qui écrit deux messages sur la console.  
  
### <a name="to-create-a-custom-activity-using-the-activity-designer"></a>Pour créer une activité personnalisée à l'aide du concepteur d'activités  
  
1.  Ouvrez [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)].  
  
2.  Sélectionnez Fichier, Nouveau, puis Projet. Sélectionnez **Workflow 4.0** sous **Visual C#** dans les **Types de projets** , puis sélectionnez le **v2010** nœud. Sélectionnez **bibliothèque d’activités** dans les **modèles** fenêtre. Nommez le nouveau projet HelloActivity.  
  
3.  Ouvrez la nouvelle activité.  Faites glisser une activité <xref:System.Activities.Statements.Sequence> de la boîte à outils jusqu'à l'aire du concepteur.  
  
4.  Faites glisser une activité <xref:System.Activities.Statements.WriteLine> dans l'activité <xref:System.Activities.Statements.Sequence>. Entrez `"Hello World"` (avec les guillemets) dans le **texte** champ.  
  
5.  Faites glisser une deuxième activité <xref:System.Activities.Statements.WriteLine> dans l'activité <xref:System.Activities.Statements.Sequence>, en dessous de la première. Entrez `"Goodbye"` (avec les guillemets) dans le **texte** champ.
