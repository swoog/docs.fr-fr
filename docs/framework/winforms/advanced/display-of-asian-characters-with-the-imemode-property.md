---
title: Affichage des caractères asiatiques avec la propriété ImeMode
ms.date: 03/30/2017
helpviewer_keywords:
- Asian languages [Windows Forms], displaying with ImeMode
- Chinese characters [Windows Forms], displaying with ImeMode
- IME mode
- Japanese characters [Windows Forms], displaying with ImeMode
- international applications [Windows Forms], character display
- international characters
- Korean characters
- Asian languages
- Input Method Editor (IME), mode
- localization [Windows Forms], character sets
- globalization [Windows Forms], character sets
ms.assetid: c60ae399-0dab-4f07-9dea-6dbfb15ec0ae
ms.openlocfilehash: d3733f642d4218c851040582ee5637b5486a7804
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36208583"
---
# <a name="display-of-asian-characters-with-the-imemode-property"></a>Affichage des caractères asiatiques avec la propriété ImeMode
Le <xref:System.Windows.Forms.Control.ImeMode%2A> propriété est utilisée par les formulaires et les contrôles pour forcer un mode spécifique pour un éditeur de méthode d’entrée (IME). L’IME est un composant essentiel pour écrire en chinois, japonais et coréen, étant donné que ces systèmes d’écriture ont plus de caractères que ce que vous pouvez coder pour un clavier standard. Par exemple, vous voulez autoriser uniquement des caractères ASCII dans une zone de texte particulière. Dans ce cas, vous pouvez définir le <xref:System.Windows.Forms.Control.ImeMode%2A> propriété <xref:System.Windows.Forms.ImeMode> et les utilisateurs seulement sera en mesure d’entrer des caractères ASCII pour cette zone de texte particulière. La valeur par défaut de la <xref:System.Windows.Forms.Control.ImeMode%2A> propriété <xref:System.Windows.Forms.ImeMode>, de sorte que si vous définissez la propriété d’un formulaire, tous les contrôles sur le formulaire héritent ce paramètre. Pour plus d’informations, consultez <xref:System.Windows.Forms.Control.ImeMode%2A> ) et <xref:System.Windows.Forms.ImeMode>.  
  
## <a name="see-also"></a>Voir aussi

[Globalisation des applications Windows Forms](globalizing-windows-forms.md)
