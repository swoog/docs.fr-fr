---
title: Vue d'ensemble de la propriété AutoSize
ms.date: 03/30/2017
helpviewer_keywords:
- sizing [Windows Forms], automatic
- layout [Windows Forms], AutoSize
- automatic sizing
- AutoSizeMode property
ms.assetid: 62fd82a2-9565-4f65-925b-9d1e66dc4e7d
ms.openlocfilehash: 6d5c4a22f186ddc5811c4a4d5e79776decea9e50
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173626"
---
# <a name="autosize-property-overview"></a>Vue d'ensemble de la propriété AutoSize
Le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété permet à un contrôle modifier sa taille, si nécessaire, pour atteindre la valeur spécifiée par le <xref:System.Windows.Forms.Control.PreferredSize%2A> propriété. Vous ajustez le comportement de dimensionnement de contrôles spécifiques en définissant le `AutoSizeMode` propriété.  
  
## <a name="autosize-behavior"></a>Comportement du redimensionnement automatique  
 Seuls certains contrôles prennent en charge le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété. En outre, certains contrôles qui prennent en charge la <xref:System.Windows.Forms.Control.AutoSize%2A> propriété prennent également en charge le `AutoSizeMode` propriété.  
  
 Le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété produit un comportement quelque peu différent, selon le type de contrôle spécifique et la valeur de la `AutoSizeMode` propriété, si la propriété existe. Le tableau suivant décrit les comportements qui sont toujours remplies et fournit une brève description de chacun d’eux :  
  
|Comportement toujours vrai|Description|  
|--------------------------|-----------------|  
|Dimensionnement automatique est une fonctionnalité de l’exécution.|Cela signifie qu’il jamais augmente ou réduit un contrôle puis n’a aucun effet.|  
|Si un contrôle change de taille, la valeur de son <xref:System.Windows.Forms.Control.Location%2A> propriété reste toujours constante.|Lorsque le contenu d’un contrôle de le rendre de croître, le contrôle s’agrandit vers la droite et vers le bas. Contrôles n’augmentent pas à gauche.|  
|Le <xref:System.Windows.Forms.Control.Dock%2A> et <xref:System.Windows.Forms.Control.Anchor%2A> propriétés sont respectées lorsque <xref:System.Windows.Forms.Control.AutoSize%2A> est `true`.|La valeur du contrôle <xref:System.Windows.Forms.Control.Location%2A> propriété est ajustée à la valeur correcte.<br /><br /> **Remarque** le <xref:System.Windows.Forms.Label> contrôle fait exception à cette règle. Lorsque vous définissez la valeur d’une fenêtre fixe <xref:System.Windows.Forms.Label> du contrôle <xref:System.Windows.Forms.Control.AutoSize%2A> propriété `true`, le <xref:System.Windows.Forms.Label> contrôle s’étirera pas.|  
|D’un contrôle <xref:System.Windows.Forms.Control.MaximumSize%2A> et <xref:System.Windows.Forms.Control.MinimumSize%2A> propriétés sont toujours respectées, quelle que soit la valeur de son <xref:System.Windows.Forms.Control.AutoSize%2A> propriété.|Le <xref:System.Windows.Forms.Control.MaximumSize%2A> et <xref:System.Windows.Forms.Control.MinimumSize%2A> propriétés ne sont pas affectées par la <xref:System.Windows.Forms.Control.AutoSize%2A> propriété.|  
|Il n’existe aucune taille minimale définie par défaut.|Cela signifie que si un contrôle est configuré pour être réduit sous <xref:System.Windows.Forms.Control.AutoSize%2A> et il n’a pas de contenu, la valeur de son <xref:System.Windows.Forms.Control.Size%2A> propriété est 0,0. Dans ce cas, votre contrôle sera réduit à un point, et il ne sera pas facilement visible.|  
|Si un contrôle n’implémente pas le <xref:System.Windows.Forms.Control.GetPreferredSize%2A> (méthode), le <xref:System.Windows.Forms.Control.GetPreferredSize%2A> méthode retourne la dernière valeur assignée à la <xref:System.Windows.Forms.Control.Size%2A> propriété.|Cela signifie que la configuration <xref:System.Windows.Forms.Control.AutoSize%2A> à `true` n’a aucun effet.|  
|Un contrôle dans un <xref:System.Windows.Forms.TableLayoutPanel> cellule toujours se réduit en fonction de la cellule jusqu'à ce que son <xref:System.Windows.Forms.Control.MinimumSize%2A> est atteinte.|Cette taille est appliquée comme une taille maximale. Cela n’est pas le cas lorsque la cellule fait partie d’un <xref:System.Windows.Forms.SizeType.AutoSize> ligne ou colonne.|  
  
## <a name="autosizemode-property"></a>AutoSizeMode (propriété)  
 Le `AutoSizeMode` propriété fournit un contrôle plus précis sur la valeur par défaut <xref:System.Windows.Forms.Control.AutoSize%2A> comportement. Le `AutoSizeMode` propriété spécifie comment un contrôle lui-même redimensionnée en fonction de son contenu. Le contenu, par exemple, pourrait être le texte pour un <xref:System.Windows.Forms.Button> contrôle ou les contrôles enfants pour un conteneur.  
  
 Le tableau suivant présente le <xref:System.Windows.Forms.AutoSizeMode> paramètres et une description du comportement de chaque paramètre est fournie.  
  
|Paramètre AutoSizeMode|Comportement|  
|--------------------------|--------------|  
|GrowAndShrink|Le contrôle augmente ou réduit pour englober son contenu.<br /><br /> Le <xref:System.Windows.Forms.Control.MinimumSize%2A> et <xref:System.Windows.Forms.Control.MaximumSize%2A> valeurs sont respectées, mais la valeur actuelle de la <xref:System.Windows.Forms.Control.Size%2A> propriété est ignorée.<br /><br /> Ceci est le même comportement que les contrôles avec le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété et aucune `AutoSizeMode` propriété.|  
|GrowOnly|Le contrôle s’agrandit autant que nécessaire pour englober son contenu, mais il sera diminuer en dessous de la valeur spécifiée par son <xref:System.Windows.Forms.Control.Size%2A> propriété.<br /><br /> Il s'agit de la valeur par défaut de l'objet `AutoSizeMode`.|  
  
## <a name="controls-that-support-the-autosize-property"></a>Contrôles qui prennent en charge la propriété AutoSize  
 Le tableau suivant répertorie les contrôles qui prennent en charge la <xref:System.Windows.Forms.Control.AutoSize%2A> et `AutoSizeMode` propriétés.  
  
|Prise en charge AutoSize|Type de contrôle|  
|----------------------|------------------|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> propriété prise en charge.<br />-Ne `AutoSizeMode` propriété.|<xref:System.Windows.Forms.CheckBox><br /><br /> <xref:System.Windows.Forms.DomainUpDown><br /><br /> <xref:System.Windows.Forms.Label><br /><br /> <xref:System.Windows.Forms.LinkLabel><br /><br /> <xref:System.Windows.Forms.MaskedTextBox> (<xref:System.Windows.Forms.TextBox> base)<br /><br /> <xref:System.Windows.Forms.NumericUpDown><br /><br /> <xref:System.Windows.Forms.RadioButton><br /><br /> <xref:System.Windows.Forms.TextBox><br /><br /> <xref:System.Windows.Forms.TrackBar>|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> propriété prise en charge.<br />-   `AutoSizeMode` propriété prise en charge.|<xref:System.Windows.Forms.Button><br /><br /> <xref:System.Windows.Forms.CheckedListBox><br /><br /> <xref:System.Windows.Forms.FlowLayoutPanel><br /><br /> <xref:System.Windows.Forms.Form><br /><br /> <xref:System.Windows.Forms.GroupBox><br /><br /> <xref:System.Windows.Forms.Panel><br /><br /> <xref:System.Windows.Forms.TableLayoutPanel>|  
|-Ne <xref:System.Windows.Forms.Control.AutoSize%2A> propriété.|<xref:System.Windows.Forms.CheckedListBox><br /><br /> <xref:System.Windows.Forms.ComboBox><br /><br /> <xref:System.Windows.Forms.DataGridView><br /><br /> <xref:System.Windows.Forms.DateTimePicker><br /><br /> <xref:System.Windows.Forms.ListBox><br /><br /> <xref:System.Windows.Forms.ListView><br /><br /> <xref:System.Windows.Forms.MaskedTextBox><br /><br /> <xref:System.Windows.Forms.MonthCalendar><br /><br /> <xref:System.Windows.Forms.ProgressBar><br /><br /> <xref:System.Windows.Forms.PropertyGrid><br /><br /> <xref:System.Windows.Forms.RichTextBox><br /><br /> <xref:System.Windows.Forms.SplitContainer><br /><br /> <xref:System.Windows.Forms.TabControl><br /><br /> <xref:System.Windows.Forms.TabPage><br /><br /> <xref:System.Windows.Forms.TreeView><br /><br /> <xref:System.Windows.Forms.WebBrowser><br /><br /> <xref:System.Windows.Forms.ScrollBar>|  
  
## <a name="autosize-in-the-design-environment"></a>Redimensionnement automatique dans l’environnement de conception  
 Le tableau suivant décrit le comportement de dimensionnement d’un contrôle au moment du design, selon la valeur de son <xref:System.Windows.Forms.Control.AutoSize%2A> et `AutoSizeMode` propriétés.  
  
 Remplacer le <xref:System.Windows.Forms.Design.ControlDesigner.SelectionRules%2A> propriété afin de déterminer si un contrôle donné est dans un état redimensionnable pour l’utilisateur. Dans le tableau suivant, « ne peut pas » signifie <xref:System.Windows.Forms.Design.SelectionRules.Moveable> uniquement, « peut » signifie <xref:System.Windows.Forms.Design.SelectionRules.AllSizeable> et <xref:System.Windows.Forms.Design.SelectionRules.Moveable>.  
  
|Paramètres AutoSize|Opération de dimensionnement d’au moment du design|  
|-----------------------|---------------------------------|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-Ne `AutoSizeMode` propriété.|L’utilisateur ne peut pas redimensionner le contrôle au moment du design, sauf pour les contrôles suivants :<br /><br /> -   <xref:System.Windows.Forms.TextBox><br />-   <xref:System.Windows.Forms.MaskedTextBox><br />-   <xref:System.Windows.Forms.RichTextBox><br />-   <xref:System.Windows.Forms.TrackBar>|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-   `AutoSizeMode` = <xref:System.Windows.Forms.AutoSizeMode.GrowAndShrink>|L’utilisateur ne peut pas redimensionner le contrôle au moment du design.|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-   `AutoSizeMode` = <xref:System.Windows.Forms.AutoSizeMode.GrowOnly>|L’utilisateur peut redimensionner le contrôle au moment du design. Lorsque le <xref:System.Windows.Forms.Control.Size%2A> est définie, l’utilisateur peut uniquement augmenter la taille du contrôle.|  
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `false`, ou <xref:System.Windows.Forms.Control.AutoSize%2A> propriété est masquée.|Utilisateur peut redimensionner le contrôle au moment du design.|  
  
> [!NOTE]
>  Pour optimiser la productivité, les ombres de Windows Forms Designer le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété pour la <xref:System.Windows.Forms.Form> classe. Au moment du design, le formulaire se comporte comme si le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété est définie sur `false`, quelle que soit sa valeur réelle. Lors de l’exécution, aucun aménagement spécial n’est effectuée et le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété est appliquée comme spécifié par le paramètre de propriété.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.AutoSize%2A>
- <xref:System.Windows.Forms.Control.PreferredSize%2A>
- <xref:System.Windows.Forms.Control.GetPreferredSize%2A>
