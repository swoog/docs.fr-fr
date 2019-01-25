---
title: Meilleures pratiques pour le contrôle TableLayoutPanel
ms.date: 03/30/2017
helpviewer_keywords:
- layout [Windows Forms]
- TableLayoutPanel control [Windows Forms], best practices
- forms [Windows Forms], best practices
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- layout [Windows Forms], AutoSize
- layout [Windows Forms], best practices
- best practices [Windows Forms], tableLayoutPanel control
- sizing [Windows Forms], automatic
- automatic sizing
ms.assetid: b6706efb-d7a4-45ec-8cf4-08fa993e3afb
ms.openlocfilehash: 6be6d0904d5b52e5188f0a5a16aaefa08265379c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674191"
---
# <a name="best-practices-for-the-tablelayoutpanel-control"></a>Meilleures pratiques pour le contrôle TableLayoutPanel
Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle fournit des fonctionnalités de disposition puissants, vous devez bien réfléchir avant d’utiliser sur vos formulaires Windows.  
  
## <a name="recommendations"></a>Recommandations  
 Les recommandations suivantes vous aideront à utiliser le <xref:System.Windows.Forms.TableLayoutPanel> contrôle mieux.  
  
### <a name="targeted-use"></a>Utilisation cibles  
 Utilisez le <xref:System.Windows.Forms.TableLayoutPanel> contrôler avec parcimonie. Vous ne devez pas l’utiliser dans toutes les situations qui nécessitent une disposition redimensionnable. La liste suivante décrit les dispositions qui bénéficient le plus de l’utilisation de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle :  
  
-   Mises en page dans laquelle il existe plusieurs parties du formulaire de redimensionnement proportionnellement entre eux.  
  
-   Dispositions qui seront modifiées ou générées dynamiquement au moment de l’exécution, telles que les formulaires de saisie de données qui ont des champs personnalisables par l’utilisateur ajoutées ou soustraites en fonction des préférences.  
  
-   Dispositions qui doivent rester à une taille fixe totale. Par exemple, avoir une boîte de dialogue qui doit rester inférieure à 800 x 600, mais vous devez prendre en charge des chaînes localisées.  
  
 La liste suivante décrit les dispositions qui ne bénéficient pas beaucoup de l’utilisation de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle :  
  
-   Formulaires de saisie des données simple avec une seule colonne d’étiquettes et une seule colonne de zones de saisie de texte.  
  
-   Formulaires avec une seule grande zone d’affichage qui doit remplir tout l’espace disponible lorsqu’un redimensionnement se produit. Un exemple de ceci est un formulaire qui affiche un seul <xref:System.Windows.Forms.PropertyGrid> contrôle. Dans ce cas, utilisez l’ancrage, étant donné que rien d’autre ne doit se développer lorsque le formulaire est redimensionné.  
  
 Choisissez soigneusement les contrôles qui doivent se trouver dans un <xref:System.Windows.Forms.TableLayoutPanel> contrôle. Si vous disposez d’espace pour votre texte augmente de 30 % à l’aide d’ancrage, envisagez d’utiliser le <xref:System.Windows.Forms.Control.Anchor%2A> propriété uniquement. Si vous pouvez estimer l’espace requis par votre disposition, l’utilisation du <xref:System.Windows.Forms.Control.Dock%2A> et <xref:System.Windows.Forms.Control.Anchor%2A> est plus facile que d’estimer les détails de l’espace restant et <xref:System.Windows.Forms.Control.AutoSize%2A> comportement.  
  
 En général, lorsque vous concevez votre disposition avec la <xref:System.Windows.Forms.TableLayoutPanel> contrôler, simplifier la conception.  
  
### <a name="use-the-document-outline-window"></a>Utilisez la fenêtre Structure du Document  
 La fenêtre Structure du Document vous donne une vue d’arborescence de votre disposition, vous pouvez utiliser pour manipuler les relations parent-enfant et d’ordre de plan de vos contrôles. À partir de la **menu Affichage**, sélectionnez **Windows autres**, puis sélectionnez **structure du Document**.  
  
### <a name="avoid-nesting"></a>Évitez l’imbrication  
 Évitez d’imbriquer d’autres <xref:System.Windows.Forms.TableLayoutPanel> contrôle au sein d’un <xref:System.Windows.Forms.TableLayoutPanel> contrôle. Débogage des dispositions imbriquées peut être difficile.  
  
### <a name="avoid-visual-inheritance"></a>Éviter l’héritage visuel  
 Le <xref:System.Windows.Forms.TableLayoutPanel> contrôle ne prend pas en charge l’héritage visuel dans le Concepteur de formulaires Windows. Un <xref:System.Windows.Forms.TableLayoutPanel> contrôle dans une classe dérivée apparaît comme « verrouillé » au moment du design.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
