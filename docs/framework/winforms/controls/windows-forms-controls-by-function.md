---
title: Classement par fonction des contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], by function
- Windows Forms, controls by function
- Windows Forms controls, list of
ms.assetid: 5e65a6c3-5d6f-480d-beb8-b28f865f07e3
ms.openlocfilehash: 3a82642c985b7ec1cee885cdda7b054adbe3dfee
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59115477"
---
# <a name="windows-forms-controls-by-function"></a>Classement par fonction des contrôles Windows Forms
Windows Forms offre des contrôles et composants qui effectuent un nombre de fonctions. Le tableau suivant répertorie les contrôles Windows Forms et les composants en fonction de la fonction général. En outre, il existe plusieurs contrôles qui remplissent la même fonction, le contrôle recommandé est répertorié avec une remarque concernant le contrôle qu’il est remplacé. Dans une table distincte ultérieure, les contrôles remplacés sont répertoriés avec leurs remplacements recommandés.  
  
> [!NOTE]
>  Les tableaux suivants ne répertorient pas chaque contrôle ou composant que vous pouvez utiliser dans les Windows Forms ; pour une liste plus complète, consultez [contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)  
  
## <a name="recommended-controls-and-components-by-function"></a>Contrôles et composants par fonction recommandés  
  
|Fonction|Contrôle|Description|  
|--------------|-------------|-----------------|  
|Affichage des données|<xref:System.Windows.Forms.DataGridView> contrôle|Le <xref:System.Windows.Forms.DataGridView> contrôle fournit une table personnalisable pour l’affichage des données. Le <xref:System.Windows.Forms.DataGridView> classe permet la personnalisation des cellules, lignes, colonnes et les bordures. **Remarque :**  Le <xref:System.Windows.Forms.DataGridView> contrôle fournit de nombreuses fonctionnalités de base et avancées qui manquent dans le <xref:System.Windows.Forms.DataGrid> contrôle. Pour plus d’informations, consultez [différences entre les Windows Forms contrôles DataGridView et DataGrid](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md)|  
|Liaison de données et de navigation|<xref:System.Windows.Forms.BindingSource> component|Simplifie la liaison de contrôles sur un formulaire à des données en fournissant une gestion des devises, de notification de modification et d’autres services.|  
||<xref:System.Windows.Forms.BindingNavigator> contrôle|Fournit une interface de type de la barre d’outils pour parcourir et de manipuler des données sur un formulaire.|  
|Édition du texte|<xref:System.Windows.Forms.TextBox> contrôle|Affiche un texte entré au moment du design qui peut être modifié par l’utilisateur en cours d’exécution ou par programme.|  
||<xref:System.Windows.Forms.RichTextBox> contrôle|Active le texte à afficher avec la mise en forme dans le format texte brut ou texte enrichi (RTF).|  
||<xref:System.Windows.Forms.MaskedTextBox> contrôle|Contraint le format d’entrée d’utilisateur|  
|Affichage d’informations (en lecture seule)|<xref:System.Windows.Forms.Label> contrôle|Affiche du texte que les utilisateurs ne peuvent pas directement modifier.|  
||<xref:System.Windows.Forms.LinkLabel> contrôle|Affiche le texte sous la forme d’un lien de style Web et déclenche un événement lorsque l’utilisateur clique sur le texte spécial. Généralement, le texte est un lien vers une autre fenêtre ou un site Web.|  
||<xref:System.Windows.Forms.StatusStrip> contrôle|Affiche des informations sur l’état actuel de l’application à l’aide de la zone délimitée, généralement en bas d’un formulaire parent.|  
||<xref:System.Windows.Forms.ProgressBar> contrôle|Affiche la progression actuelle d’une opération à l’utilisateur.|  
|Affichage de page Web|<xref:System.Windows.Forms.WebBrowser> contrôle|Autorise l’utilisateur à parcourir des pages web dans votre formulaire.|  
|Sélection dans une liste|<xref:System.Windows.Forms.CheckedListBox> contrôle|Affiche une liste déroulante d’éléments, accompagnés chacun d’une case à cocher.|  
||<xref:System.Windows.Forms.ComboBox> contrôle|Affiche une liste déroulante d’éléments.|  
||<xref:System.Windows.Forms.DomainUpDown> contrôle|Affiche une liste d’éléments que les utilisateurs peuvent faire défiler avec des boutons haut et bas.|  
||<xref:System.Windows.Forms.ListBox> contrôle|Affiche une liste des éléments texte et graphiques (icônes).|  
||<xref:System.Windows.Forms.ListView> contrôle|Affiche les éléments dans un des quatre vues différentes. Vues incluent uniquement le texte, texte avec petites icônes, texte avec grandes icônes et une vue de détails.|  
||<xref:System.Windows.Forms.NumericUpDown> contrôle|Affiche une liste de nombres que les utilisateurs peuvent faire défiler avec des boutons haut et bas.|  
||<xref:System.Windows.Forms.TreeView> contrôle|Affiche une collection hiérarchique d’objets de nœud qui peut être constitué de texte avec des cases à cocher facultatifs ou d’icônes.|  
|Affichage de graphiques|<xref:System.Windows.Forms.PictureBox> contrôle|Affiche les fichiers graphiques, comme les bitmaps et icônes, dans un frame.|  
|Stockage des graphismes|<xref:System.Windows.Forms.ImageList> contrôle|Sert de référentiel pour les images. <xref:System.Windows.Forms.ImageList> contrôles et les images qu’ils contiennent peuvent être réutilisés à partir d’une application à l’autre.|  
|Paramètre de valeur|<xref:System.Windows.Forms.CheckBox> contrôle|Affiche une case à cocher et une étiquette de texte. Généralement utilisé pour définir les options.|  
||<xref:System.Windows.Forms.CheckedListBox> contrôle|Affiche une liste déroulante d’éléments, accompagnés chacun d’une case à cocher.|  
||<xref:System.Windows.Forms.RadioButton> contrôle|Affiche un bouton qui peut être activé ou désactivée.|  
||<xref:System.Windows.Forms.TrackBar> contrôle|Permet aux utilisateurs de définir des valeurs sur une échelle en déplaçant un « thumb » le long d’une mise à l’échelle.|  
|Paramètre de date|<xref:System.Windows.Forms.DateTimePicker> contrôle|Affiche un calendrier graphique permettant aux utilisateurs de sélectionner une date ou une heure.|  
||<xref:System.Windows.Forms.MonthCalendar> contrôle|Affiche un calendrier graphique permettant aux utilisateurs de sélectionner une plage de dates.|  
|Boîtes de dialogue|<xref:System.Windows.Forms.ColorDialog> contrôle|Affiche la boîte de dialogue de sélecteur de couleurs qui permet aux utilisateurs de définir la couleur d’un élément d’interface.|  
||<xref:System.Windows.Forms.FontDialog> contrôle|Affiche une boîte de dialogue qui permet aux utilisateurs de définir une police et ses attributs.|  
||<xref:System.Windows.Forms.OpenFileDialog> contrôle|Affiche une boîte de dialogue qui permet aux utilisateurs d’accéder à et sélectionnez un fichier.|  
||<xref:System.Windows.Forms.PrintDialog> contrôle|Affiche une boîte de dialogue qui permet aux utilisateurs de sélectionner une imprimante et définissez ses attributs.|  
||<xref:System.Windows.Forms.PrintPreviewDialog> contrôle|Affiche une boîte de dialogue qui affiche la manière dont un contrôle <xref:System.Drawing.Printing.PrintDocument> composant apparaîtra une fois imprimé.|  
||<xref:System.Windows.Forms.FolderBrowserDialog> contrôle|Affiche une boîte de dialogue qui permet aux utilisateurs de parcourir, créer et éventuellement sélectionner un dossier|  
||<xref:System.Windows.Forms.SaveFileDialog> contrôle|Affiche une boîte de dialogue qui permet aux utilisateurs d’enregistrer un fichier.|  
|Contrôles de menu|<xref:System.Windows.Forms.MenuStrip> contrôle|Crée des menus personnalisés. **Remarque :**  Le <xref:System.Windows.Forms.MenuStrip> est conçu pour remplacer le <xref:System.Windows.Forms.MainMenu> contrôle.|  
||<xref:System.Windows.Forms.ContextMenuStrip> contrôle|Crée des menus contextuels personnalisés. **Remarque :**  Le <xref:System.Windows.Forms.ContextMenuStrip> est conçu pour remplacer le <xref:System.Windows.Forms.ContextMenu> contrôle.|  
|Commandes|<xref:System.Windows.Forms.Button> contrôle|Démarre, arrête ou interrompt un processus.|  
||<xref:System.Windows.Forms.LinkLabel> contrôle|Affiche le texte sous la forme d’un lien de style Web et déclenche un événement lorsque l’utilisateur clique sur le texte spécial. Généralement, le texte est un lien vers une autre fenêtre ou un site Web.|  
||<xref:System.Windows.Forms.NotifyIcon> contrôle|Affiche une icône dans la zone de notification d’état de la barre des tâches qui représente une application en cours d’exécution en arrière-plan.|  
||<xref:System.Windows.Forms.ToolStrip> contrôle|Crée des barres d’outils qui peuvent avoir un Microsoft Windows XP, Microsoft Office, Microsoft Internet Explorer ou personnalisé aspect, avec ou sans thèmes et prenant en charge le dépassement de capacité et la réorganisation des éléments au moment de l’exécution. **Remarque :**  Le <xref:System.Windows.Forms.ToolStrip> contrôle est conçu pour remplacer le <xref:System.Windows.Forms.ToolBar> contrôle.|  
|Aide de l’utilisateur|<xref:System.Windows.Forms.HelpProvider> component|Fournit une aide contextuelle ou en ligne pour les contrôles.|  
||<xref:System.Windows.Forms.ToolTip> component|Fournit une fenêtre contextuelle qui affiche une brève description de l’objectif d’un contrôle lorsque l’utilisateur place le pointeur sur le contrôle.|  
|Regrouper les autres contrôles|<xref:System.Windows.Forms.Panel> contrôle|Regroupe un ensemble de contrôles sur un frame déroulant sans étiquette.|  
||<xref:System.Windows.Forms.GroupBox> contrôle|Regroupe un ensemble de contrôles (tels que des boutons radio) sur un frame non déroulant doté étiqueté.|  
||<xref:System.Windows.Forms.TabControl> contrôle|Fournit une page à onglets pour organiser et d’y accéder efficacement les objets groupés.|  
||<xref:System.Windows.Forms.SplitContainer> contrôle|Fournit deux panneaux séparés par une barre mobile. **Remarque :**  Le <xref:System.Windows.Forms.SplitContainer> contrôle est conçu pour remplacer le <xref:System.Windows.Forms.Splitter> contrôle.|  
||<xref:System.Windows.Forms.TableLayoutPanel> contrôle|Représente un panneau qui dispose dynamiquement son contenu dans une grille composée de lignes et de colonnes.|  
||<xref:System.Windows.Forms.FlowLayoutPanel> contrôle|Représente un panneau qui dispose dynamiquement son contenu horizontalement ou verticalement.|  
|Audio|<xref:System.Media.SoundPlayer> contrôle|Lecture des fichiers audio au format .wav. Sons peuvent être chargées ou lus de manière asynchrone.|  
  
## <a name="superseded-controls-and-components-by-function"></a>Contrôles et composants par fonction remplacés  
  
|Fonction|Contrôle remplacé|Remplacement recommandé|  
|--------------|------------------------|-----------------------------|  
|Affichage des données|<xref:System.Windows.Forms.DataGrid>|<xref:System.Windows.Forms.DataGridView>|  
|Affichage d’informations (contrôles en lecture seule)|<xref:System.Windows.Forms.StatusBar>|<xref:System.Windows.Forms.StatusStrip>|  
|Contrôles de menu|<xref:System.Windows.Forms.ContextMenu>|<xref:System.Windows.Forms.ContextMenuStrip>|  
||<xref:System.Windows.Forms.MainMenu>|<xref:System.Windows.Forms.MenuStrip>|  
|Commandes|<xref:System.Windows.Forms.ToolBar>|<xref:System.Windows.Forms.ToolStrip>|  
||<xref:System.Windows.Forms.StatusBar>|<xref:System.Windows.Forms.StatusStrip>|  
|Présentation des formulaires|<xref:System.Windows.Forms.Splitter>|<xref:System.Windows.Forms.SplitContainer>|  
  
## <a name="see-also"></a>Voir aussi

- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
- [Développement de contrôles Windows Forms personnalisés avec le .NET Framework](developing-custom-windows-forms-controls.md)
