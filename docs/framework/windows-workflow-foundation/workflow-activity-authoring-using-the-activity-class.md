---
title: Création de l'activité de workflow à l'aide de la classe d'activité
ms.date: 03/30/2017
ms.assetid: 7b7b1c66-f093-43c3-b4d1-7173b46516da
ms.openlocfilehash: abdabc46aa54e19d5a04c5b34d6d2b9be07488d6
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711861"
---
# <a name="workflow-activity-authoring-using-the-activity-class"></a>Création de l'activité de workflow à l'aide de la classe d'activité
La façon la plus simple pour créer une activité à l’aide de Windows Workflow Foundation (WF) dans [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] consiste à créer une classe qui hérite de <xref:System.Activities.Activity> qui crée les fonctionnalités en assemblant personnalisé activités ou les activités à partir de la [intégrés Bibliothèque d’activités](net-framework-4-5-built-in-activity-library.md). Cette rubrique montre comment créer une activité qui écrit deux messages sur la console.

### <a name="to-create-a-custom-activity-using-the-activity-designer"></a>Pour créer une activité personnalisée à l'aide du concepteur d'activités

1.  Ouvrez Visual Studio 2012.

2.  Sélectionnez Fichier, Nouveau, puis Projet. Sélectionnez **Workflow 4.0** sous **Visual C#** dans le **Types de projets** , puis sélectionnez le **v2010** nœud. Sélectionnez **bibliothèque d’activités** dans le **modèles** fenêtre. Nommez le nouveau projet HelloActivity.

3.  Ouvrez la nouvelle activité.  Faites glisser une activité <xref:System.Activities.Statements.Sequence> de la boîte à outils jusqu'à l'aire du concepteur.

4.  Faites glisser une activité <xref:System.Activities.Statements.WriteLine> dans l'activité <xref:System.Activities.Statements.Sequence>. Entrez `"Hello World"` (avec les guillemets) dans le **texte** champ.

5.  Faites glisser une deuxième activité <xref:System.Activities.Statements.WriteLine> dans l'activité <xref:System.Activities.Statements.Sequence>, en dessous de la première. Entrez `"Goodbye"` (avec les guillemets) dans le **texte** champ.
