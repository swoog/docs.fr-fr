---
title: Liaison de données et Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- master-details lists
- data [Windows Forms], data binding
- reports [Windows Forms], Windows Forms
- lookup tables [Windows Forms], data binding
- data [Windows Forms], complex data binding
- data binding [Windows Forms], Windows Forms
- data [Windows Forms], simple data binding
- Windows Forms controls, data binding
- data-bound controls [Windows Forms], Windows Forms
ms.assetid: 419aac5e-819b-4aad-88b0-73a2f8c0bd27
ms.openlocfilehash: 3c96275f3e5db24446b030ec007f23e9035242c8
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703684"
---
# <a name="data-binding-and-windows-forms"></a>Liaison de données et Windows Forms
Dans Windows Forms, vous pouvez créer des liaisons avec des sources de données traditionnelles, mais aussi avec quasiment toute structure contenant des données. Vous pouvez créer une liaison avec un tableau de valeurs que vous calculez au moment de l'exécution, que vous lisez depuis un fichier ou que vous dérivez de valeurs d'autres contrôles.  
  
 De plus, vous pouvez lier n'importe quelle propriété de n'importe quel contrôle à la source de données. Dans une liaison de données traditionnelle, vous liez généralement la propriété d'affichage (par exemple, la propriété <xref:System.Windows.Forms.Control.Text%2A> d'un contrôle <xref:System.Windows.Forms.TextBox>) à la source de données. Avec le [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)], vous avez également la possibilité de définir d'autres propriétés via la liaison de données. Vous pouvez utiliser des liaisons pour effectuer les tâches suivantes :  
  
-   Définir le graphisme d'un contrôle d'image  
  
-   Définir la couleur d'arrière-plan d'un ou plusieurs contrôles  
  
-   Définition de la taille des contrôles  
  
 La liaison de données permet de définir automatiquement toute propriété d'un contrôle de formulaire accessible au moment de l'exécution.  
  
## <a name="types-of-data-binding"></a>Types de liaisons de données  
 Windows Forms peut utiliser deux types de liaisons de données : les liaisons simples et les liaisons complexes. Chaque type a ses propres avantages.  
  
|Type de liaison de données|Description|  
|--------------------------|-----------------|  
|Liaison de données simple|Capacité d'un contrôle à créer une liaison avec un élément de données, tel qu'une valeur dans une colonne d'une table de dataset. Il s'agit du type de liaison typique des contrôles tels que <xref:System.Windows.Forms.TextBox> ou <xref:System.Windows.Forms.Label>, qui n'affichent généralement qu'une seule valeur. En réalité, n'importe quelle propriété d'un contrôle peut être liée à un champ d'une base de données. Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.<br /><br /> Pour plus d'informations, voir :<br /><br /> -   [Interfaces participant à la liaison de données](interfaces-related-to-data-binding.md)<br />-   [Guide pratique pour Naviguer parmi les données dans les Windows Forms](how-to-navigate-data-in-windows-forms.md)<br />-   [Guide pratique pour Créer un contrôle de liaison Simple dans un formulaire Windows](how-to-create-a-simple-bound-control-on-a-windows-form.md)|  
|Liaison de données complexe|Capacité d'un contrôle à lier plusieurs éléments de données, généralement plusieurs enregistrements d'une base de données. La liaison complexe est également appelée liaison basée sur des listes. Des contrôles qui prennent en charge la liaison complexe sont, par exemple, <xref:System.Windows.Forms.DataGridView>, <xref:System.Windows.Forms.ListBox> et <xref:System.Windows.Forms.ComboBox>. Pour obtenir un exemple de liaison de données complexe, consultez [Comment : Lier un contrôle ComboBox de Windows Forms ou d’un contrôle ListBox à des données](./controls/how-to-bind-a-windows-forms-combobox-or-listbox-control-to-data.md).|  
  
## <a name="bindingsource-component"></a>Composant BindingSource  
 Pour simplifier la liaison de données, Windows Forms permet de lier une source de données au composant <xref:System.Windows.Forms.BindingSource>, puis de lier les contrôles à <xref:System.Windows.Forms.BindingSource>. Vous pouvez utiliser <xref:System.Windows.Forms.BindingSource> dans des scénarios de liaison simple ou complexe. Dans les deux cas, <xref:System.Windows.Forms.BindingSource> joue le rôle d'intermédiaire entre la source de données et les contrôles liés qui fournissent des services de notification de modifications et de gestion des devises, entre autres services.  
  
## <a name="common-scenarios-that-employ-data-binding"></a>Scénarios courants impliquant des liaisons de données  
 Quasiment toutes les applications commerciales utilisent des informations lues à partir de sources de données d'un type quelconque, généralement au moyen de liaisons de données. La liste suivante présente quelques exemples de scénarios courants qui utilisent la liaison de données comme méthode de présentation et de manipulation des données.  
  
|Scénario|Description|  
|--------------|-----------------|  
|Création de rapports|Les rapports permettant d'afficher et de synthétiser vos données dans un document imprimé. Il est très courant de créer un rapport à partir du contenu sélectionné d'une source de données en vue de l'afficher à l'écran ou de l'imprimer. Les rapports les plus couramment créés sont les listes, les factures et les résumés. Les éléments sont généralement organisés sous forme de colonnes de listes, avec des sous-éléments sous chacun d'eux. Toutefois, vous devez choisir la disposition qui convient le mieux à vos données.|  
|Entrée de données|Les formulaires de saisie de données sont couramment utilisés pour entrer de grandes quantités de données associées ou pour demander aux utilisateurs de saisir des informations. Les utilisateurs peuvent entrer des informations ou choisir parmi des options au moyen de cases à cocher, de cases d'option, de listes déroulantes et de zones de texte. Les informations sont ensuite envoyées, puis stockées dans une base de données, dont la structure est basée sur les informations entrées.|  
|Relation Maître/Détail|Une application Maître/Détail est un format qui permet de consulter des données associées. Il s'agit de deux tables de données liées par une relation. Un exemple classique est celui de la table "Clients" et de la table "Commandes" qui sont liées par une relation permettant d'associer les clients aux commandes qu'ils ont passées. Pour plus d’informations sur la création d’une application maître/détail avec deux Windows Forms <xref:System.Windows.Forms.DataGridView> contrôles, consultez [Comment : Créer un formulaire maître/détail utilisant deux contrôles de DataGridView Windows Forms](./controls/create-a-master-detail-form-using-two-datagridviews.md)|  
|Table de choix|Un autre scénario courant de manipulation et de présentation des données est celui de la table de choix. Souvent, dans le cadre d'un affichage de données plus important, un contrôle <xref:System.Windows.Forms.ComboBox> est utilisé pour afficher et manipuler des données. Ce qu'il faut retenir, c'est que les données affichées dans le contrôle <xref:System.Windows.Forms.ComboBox> sont différentes de celles écrites dans la base de données. Par exemple, si vous avez un contrôle <xref:System.Windows.Forms.ComboBox> qui affiche les articles disponibles dans une épicerie, vous préférerez sans doute voir le nom des produits (pain, lait, œufs). Toutefois, afin de faciliter l'extraction d'informations et dans un objectif de normalisation des bases de données, vous stockeriez probablement les informations relatives aux éléments d'une commande donnée sous forme de numéros d'article (#501, #603, etc.). Par conséquent, il existe un lien implicite entre le "nom convivial" de l'article dans le contrôle <xref:System.Windows.Forms.ComboBox> de votre formulaire, et le numéro d'article associé qui est présent dans la commande. C'est tout l'intérêt d'une recherche dans une table. Pour plus d'informations, voir [Procédure : Créer une Table de correspondance avec le composant de BindingSource Windows Forms](./controls/how-to-create-a-lookup-table-with-the-windows-forms-bindingsource-component.md).|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Binding>
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
- [Guide pratique pour Lier le contrôle DataGrid Windows Forms à une Source de données](./controls/how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)
- [BindingSource, composant](./controls/bindingsource-component.md)
