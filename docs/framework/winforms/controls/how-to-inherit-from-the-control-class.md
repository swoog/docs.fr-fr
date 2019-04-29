---
title: 'Procédure : hériter de la classe Control'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- Control class [Windows Forms], inheriting from
- custom controls [Windows Forms], inheritance
- OnPaint method [Windows Forms]
- custom controls [Windows Forms], creating
ms.assetid: 46ba0df3-5cf7-443c-a3b4-a72660172476
ms.openlocfilehash: 14f225f5587379b3efa7b6dc2475f1b697ebb281
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941139"
---
# <a name="how-to-inherit-from-the-control-class"></a>Procédure : hériter de la classe Control
Si vous souhaitez créer un contrôle entièrement personnalisé à utiliser sur un formulaire Windows, vous devez hériter de la <xref:System.Windows.Forms.Control> classe. Tout en héritant de la <xref:System.Windows.Forms.Control> classe nécessite que vous effectuer davantage de planification et de l’implémentation, il vous fournit également la plus grande plage d’options. Lorsque vous héritez de <xref:System.Windows.Forms.Control>, vous héritez des fonctionnalités très basique qui facilite le travail de contrôles. Les fonctionnalités inhérentes à la <xref:System.Windows.Forms.Control> classe gère l’entrée utilisateur via le clavier et de la souris, définissent les limites et la taille du contrôle, fournit un handle windows et fournit la gestion des messages et la sécurité. Elles n’intègrent pas la peinture, qui désigne ici le rendu réel de l’interface graphique du contrôle, ni les fonctionnalités d’interaction utilisateur spécifiques. Vous devez fournir tous ces aspects par le biais de code personnalisé.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-a-custom-control"></a>Pour créer un contrôle personnalisé  
  
1. Créez un projet d’**application Windows** ou de **bibliothèque de contrôles Windows**.  
  
2. Dans le menu **Projet** , choisissez **Ajouter une classe**.  
  
3. Dans la boîte de dialogue **Ajouter un nouvel élément**, cliquez sur **Contrôle personnalisé**.  
  
     Un nouveau contrôle personnalisé est ajouté à votre projet.  
  
4. Appuyez sur F7 pour ouvrir l’**éditeur de code** de votre contrôle personnalisé.  
  
5. Recherchez le <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode), qui doit être vide à l’exception d’un appel à la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode de la classe de base.  
  
6. Modifiez le code afin d’incorporer la peinture personnalisée pour votre contrôle.  
  
     Pour plus d’informations sur l’écriture de code permettant d’afficher des graphiques concernant les contrôles, consultez [Peinture et rendu personnalisés des contrôles](custom-control-painting-and-rendering.md).  
  
7. Implémentez les méthodes, les propriétés ou les événements personnalisés que votre contrôle intégrera.  
  
8. Enregistrez et testez votre contrôle.  
  
## <a name="see-also"></a>Voir aussi

- [Variétés de contrôles personnalisés](varieties-of-custom-controls.md)
- [Guide pratique pour Hériter de la classe UserControl](how-to-inherit-from-the-usercontrol-class.md)
- [Guide pratique pour Windows existant hériter de contrôles de formulaires](how-to-inherit-from-existing-windows-forms-controls.md)
- [Guide pratique pour Créer des contrôles pour les Windows Forms](how-to-author-controls-for-windows-forms.md)
- [Dépannage des gestionnaires d’événements hérités en Visual Basic](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
- [Développement de contrôles Windows Forms au moment du design](developing-windows-forms-controls-at-design-time.md)
