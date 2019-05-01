---
title: Multithreading dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- BackgroundWorker component
- threading [Windows Forms], controls
ms.assetid: c311d652-0f26-45fa-bdcc-b1615d73ce4e
ms.openlocfilehash: cc7f358a62c8057abb77e1f5a28544bb6c858d98
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012722"
---
# <a name="multithreading-in-windows-forms-controls"></a>Multithreading dans les contrôles Windows Forms
Dans de nombreuses applications, vous pouvez rendre votre interface utilisateur (IU) plus réactive en effectuant les opérations de longue durée sur un autre thread. Un certain nombre d’outils est disponible pour le multithreading vos contrôles Windows Forms, y compris le <xref:System.Threading> espace de noms, le <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> (méthode) et le `BackgroundWorker` composant.  
  
> [!NOTE]
>  Le `BackgroundWorker` composant remplace et ajoute des fonctionnalités à la <xref:System.Threading> espace de noms et le <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> méthode ; Toutefois, ceux-ci sont conservés pour la compatibilité descendante et une utilisation ultérieure, si vous choisissez. Pour plus d’informations, consultez [vue d’ensemble du composant BackgroundWorker](backgroundworker-component-overview.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Effectuer des appels Thread-Safe aux contrôles de Windows Forms](how-to-make-thread-safe-calls-to-windows-forms-controls.md)  
 Montre comment effectuer des appels thread-safe aux contrôles Windows Forms.  
  
 [Guide pratique pour Utiliser un Thread d’arrière-plan pour rechercher des fichiers](how-to-use-a-background-thread-to-search-for-files.md)  
 Montre comment utiliser le <xref:System.Threading> espace de noms et le <xref:System.Windows.Forms.Control.BeginInvoke%2A> méthode pour rechercher les fichiers de façon asynchrone.  
  
## <a name="reference"></a>Référence  
 <xref:System.ComponentModel.BackgroundWorker>  
 Documente un composant qui encapsule un thread de travail pour les opérations asynchrones.  
  
 <xref:System.Media.SoundPlayer.LoadAsync%2A>  
 Décrit comment charger un son de façon asynchrone.  
  
 <xref:System.Windows.Forms.PictureBox.LoadAsync%2A>  
 Décrit comment charger une image de façon asynchrone.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Guide pratique pour exécuter une opération en arrière-plan](how-to-run-an-operation-in-the-background.md)  
 Montre comment effectuer une opération longue avec le <xref:System.ComponentModel.BackgroundWorker> composant.  
  
 [Vue d'ensemble du composant BackgroundWorker](backgroundworker-component-overview.md)  
 Fournit des rubriques qui décrivent comment utiliser le <xref:System.ComponentModel.BackgroundWorker> composant pour les opérations asynchrones.
