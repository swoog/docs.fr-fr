---
title: Fonctionnalités par défaut du contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], default functionality in DataGridView control
- DataGridView control [Windows Forms], default functionality
ms.assetid: 4405f697-cad1-4839-9bcd-8ddb09d9f00e
ms.openlocfilehash: 26633b0abaa8c1c2916153b2236ecf9e4982fd68
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011357"
---
# <a name="default-functionality-in-the-windows-forms-datagridview-control"></a>Fonctionnalités par défaut du contrôle DataGridView Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.DataGridView> contrôle fournit aux utilisateurs avec une quantité significative de fonctionnalité par défaut.  
  
## <a name="default-functionality"></a>Fonctionnalité par défaut  
 Par défaut, un <xref:System.Windows.Forms.DataGridView> contrôle :  
  
- Affiche automatiquement les en-têtes de colonne et les en-têtes de lignes restent visibles pendant que la table fait défiler verticalement.  
  
- A un en-tête de ligne qui contient un indicateur de sélection de la ligne actuelle.  
  
- A un rectangle de sélection dans la première cellule.  
  
- A des colonnes qui peuvent être redimensionnés automatiquement lorsque l’utilisateur double-clique sur les séparateurs de colonne.  
  
- Prend automatiquement en charge les styles visuels sur Windows XP et la famille Windows Server 2003 lorsque la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> méthode est appelée à partir de l’application `Main` (méthode).  
  
 En outre, le contenu d’un <xref:System.Windows.Forms.DataGridView> contrôle peut être modifié par défaut :  
  
- Si l’utilisateur double-clique ou appuie sur F2 dans une cellule, le contrôle place la cellule en mode édition et le contenu de la cellule en tant que l’utilisateur tape des mises à jour automatiquement.  
  
- Si l’utilisateur fait défiler jusqu'à la fin de la grille, l’utilisateur verra qu’une ligne pour l’ajout de nouveaux enregistrements est présente. Lorsque l’utilisateur clique sur cette ligne, une nouvelle ligne est ajoutée à la <xref:System.Windows.Forms.DataGridView> contrôle, avec les valeurs par défaut. Lorsque l’utilisateur appuie sur ÉCHAP, cette nouvelle ligne disparaît.  
  
- Si l’utilisateur clique sur un en-tête de ligne, la ligne entière est sélectionnée.  
  
 Lorsque vous liez un <xref:System.Windows.Forms.DataGridView> contrôle à une source de données en définissant son <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété, le contrôle :  
  
- Utilise automatiquement les noms des colonnes de la source de données en tant que le texte d’en-tête de colonne.  
  
- Est rempli avec le contenu de la source de données. <xref:System.Windows.Forms.DataGridView> les colonnes sont automatiquement créés pour chaque colonne dans la source de données.  
  
- Crée une ligne pour chaque ligne visible dans la table.  
  
- Trie automatiquement les lignes selon les données sous-jacentes lorsque l’utilisateur clique sur un en-tête de colonne.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- [DataGridView, contrôle](datagridview-control-windows-forms.md)
