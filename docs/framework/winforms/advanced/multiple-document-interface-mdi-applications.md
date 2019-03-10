---
title: Applications d'interface multidocument (MDI, Multiple Document Interface)
ms.date: 03/30/2017
helpviewer_keywords:
- forms [Windows Forms], MDI
- windows [Windows Forms], mDI
- Windows Forms, MDI applications
- MDI
ms.assetid: 599faf75-13cf-49cc-ad3c-255545e5cb97
ms.openlocfilehash: 0ce7c66946d03d566b21473711cb6b3315885236
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717442"
---
# <a name="multiple-document-interface-mdi-applications"></a>Applications d'interface multidocument (MDI, Multiple Document Interface)
Applications d’interface multidocument (MDI) permettent d’afficher plusieurs documents en même temps, chaque document affiché dans sa propre fenêtre. Les applications MDI ont souvent un élément de menu Fenêtre avec les sous-menus pour basculer entre les fenêtres ou aux documents.  
  
> [!NOTE]
>  Il existe des différences de comportement entre des formulaires MDI et fenêtres d’interface monodocument (SDI) dans les Windows Forms. Le `Opacity` propriété n’affecte pas l’apparence des formulaires enfants MDI. En outre, le <xref:System.Windows.Forms.Form.CenterToParent%2A> méthode n’affecte pas le comportement des formulaires enfants MDI.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Créer des formulaires MDI parents](how-to-create-mdi-parent-forms.md)  
 Explique comment créer le conteneur de plusieurs documents dans une application MDI.  
  
 [Guide pratique pour Créer des formulaires MDI enfants](how-to-create-mdi-child-forms.md)  
 Fournit des instructions pour la création d’une ou plusieurs fenêtres qui opèrent au sein d’un formulaire MDI parent.  
  
 [Guide pratique pour Déterminer l’enfant MDI actif](how-to-determine-the-active-mdi-child.md)  
 Explique comment déterminer la fenêtre enfant qui a le focus (et envoyer son contenu dans le Presse-papiers).  
  
 [Guide pratique pour Envoyer des données à l’enfant MDI actif](how-to-send-data-to-the-active-mdi-child.md)  
 Explique comment transmettre des informations dans la fenêtre enfant active.  
  
 [Guide pratique pour Réorganiser des formulaires MDI enfants](how-to-arrange-mdi-child-forms.md)  
 Explique comment la mosaïque, en cascade ou réorganiser les fenêtres enfants d’une application MDI.
