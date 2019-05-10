---
title: Concepts de base du développement de contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], derivation types
- programming concepts [Windows Forms], Windows Forms controls
- controls [Windows Forms], creating
ms.assetid: 6277bb81-90f7-4c5b-9f4b-b02bb42dd316
ms.openlocfilehash: 8d9dedc016a8fda654fecb2ee09c7206b3ddea82
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64584769"
---
# <a name="windows-forms-control-development-basics"></a>Concepts de base du développement de contrôles Windows Forms
Un contrôle Windows Forms est une classe qui dérive directement ou indirectement de <xref:System.Windows.Forms.Control?displayProperty=nameWithType>. La liste suivante décrit des scénarios courants pour le développement de contrôles Windows Forms :  
  
- Combinaison de contrôles existants pour créer un contrôle composite.  
  
     Les contrôles composites encapsulent une interface utilisateur qui peut être réutilisée en tant que contrôle. Un exemple d’un contrôle composite est un contrôle qui se compose d’une zone de texte et un bouton de réinitialisation. Concepteurs visuels offrent une prise en charge riche pour la création de contrôles composites. Pour créer un contrôle composite, dérivez de <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>. La classe de base <xref:System.Windows.Forms.UserControl> fournit le routage clavier pour les contrôles enfants et permet aux contrôles enfants fonctionner en tant que groupe. Pour plus d’informations, consultez l’article [Développement d’un contrôle Windows Forms composite](developing-a-composite-windows-forms-control.md).  
  
- Extension d’un contrôle existant pour le personnaliser ou à ajouter à ses fonctionnalités.  
  
     Un bouton dont la couleur ne peut pas être modifiée et un bouton qui a une propriété supplémentaire qui assure le suivi du nombre de fois où il a été cliqué sont des exemples de contrôles étendus. Vous pouvez personnaliser n’importe quel contrôle Windows Forms en dérivant à partir de celui-ci et en substituant ou en ajoutant des propriétés, méthodes et événements.  
  
- Création d’un contrôle qui n’a pas été combiner ou étendre des contrôles existants.  
  
     Dans ce scénario, dérivez votre contrôle de la classe de base <xref:System.Windows.Forms.Control>. Vous pouvez ajouter mais aussi remplacer les propriétés, méthodes et événements de la classe de base. Pour commencer, consultez [Comment : Développer un contrôle de formulaires Windows Simple](how-to-develop-a-simple-windows-forms-control.md).  
  
 La classe de base pour les contrôles Windows Forms, <xref:System.Windows.Forms.Control>, fournit les éléments nécessaires à l’affichage dans les applications Windows côté client. <xref:System.Windows.Forms.Control> fournit un handle de fenêtre, gère le routage des messages et fournit des événements de souris et clavier ainsi que de nombreux autres utilisateur des événements d’interface. Il fournit une représentation avancée et possède des propriétés spécifiques à l’affichage visuel, telles que <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>et bien d’autres. En outre, il assure la sécurité, la prise en charge et l’interopérabilité avec les contrôles ActiveX de threading. Étant donné que la majeure partie de l’infrastructure est fournie par la classe de base, il est relativement facile de développer vos propres contrôles Windows Forms.  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Développer un contrôle de formulaires Windows Simple](how-to-develop-a-simple-windows-forms-control.md)
- [Développement d’un contrôle Windows Forms composite](developing-a-composite-windows-forms-control.md)
- [Guide pratique pour Créer un contrôle Windows Forms affiche la progression](how-to-create-a-windows-forms-control-that-shows-progress.md)
- [Variétés de contrôles personnalisés](varieties-of-custom-controls.md)
