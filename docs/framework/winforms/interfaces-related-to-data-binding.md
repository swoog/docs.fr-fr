---
title: Interfaces participant à la liaison de données
ms.date: 03/30/2017
helpviewer_keywords:
- data [Windows Forms], data-binding interfaces
- INotifyPropertyChanged interface
- IBindingListView interface
- IList interface [Windows Forms], Windows Forms data binding
- IBindingList interface [Windows Forms], Windows Forms data binding
- interfaces [Windows Forms], Windows Forms data binding
- IEditableObject interface [Windows Forms], Windows Forms data binding
- data binding [Windows Forms], interfaces
- IDataErrorInfo interface [Windows Forms], Windows Forms data binding
ms.assetid: 14e49a2e-3e46-47ca-b491-70d546333277
ms.openlocfilehash: ffda85b2704212ea5323117447e0cfe17ffb33db
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59226957"
---
# <a name="interfaces-related-to-data-binding"></a>Interfaces participant à la liaison de données
Avec [!INCLUDE[vstecado](../../../includes/vstecado-md.md)], vous pouvez créer de nombreuses structures de données différentes pour répondre aux besoins de liaison de votre application et des données que vous utilisez. Vous souhaiterez peut-être créer vos propres classes qui fourniront ou utiliseront des données dans les Windows Forms. Ces objets peuvent offrir différents niveaux de fonctionnalités et de complexité, de la liaison de données basique à la fourniture d’une prise en charge au moment du design, en passant par la vérification des erreurs, la notification des modifications ou même la prise en charge de la restauration structurée des modifications apportées aux données elles-mêmes.  
  
## <a name="consumers-of-data-binding-interfaces"></a>Utilisateurs d’interfaces de liaison de données  
 Les sections suivantes décrivent deux groupes d’objets d’interface. Le premier groupe répertorie les interfaces implémentées sur les sources de données par les auteurs de sources de données. Ces interfaces sont conçues pour être utilisées par les consommateurs de sources de données, qui sont dans la plupart des cas des contrôles ou des composants Windows Forms. Le second groupe répertorie les interfaces conçues pour être utilisées par les auteurs de composants. Les auteurs de composants utilisent ces interfaces lorsqu’ils créent un composant prenant en charge la liaison de données pour une utilisation par le moteur de liaison de données Windows Forms. Vous pouvez implémenter ces interfaces dans les classes associées à votre formulaire pour activer la liaison de données. Chaque cas présente une classe qui implémente une interface permettant l’interaction avec les données. Visual Studio rapide d’applications (RAD) de développement outils design de données expérience tirent déjà parti de cette fonctionnalité.  
  
### <a name="interfaces-for-implementation-by-data-source-authors"></a>Interfaces pour implémentation par des auteurs de sources de données  
 Les interfaces suivantes sont conçues pour être utilisées par les contrôles Windows Forms :  
  
-   <xref:System.Collections.IList> interface  
  
     Une classe qui implémente le <xref:System.Collections.IList> interface peut être un <xref:System.Array>, <xref:System.Collections.ArrayList>, ou <xref:System.Collections.CollectionBase>. Il s’agit de listes indexées d’éléments de type <xref:System.Object>. Ces listes doivent contenir des types homogènes, car le premier élément de l’index détermine le type. <xref:System.Collections.IList> seraient disponibles pour la liaison uniquement au moment de l’exécution.  
  
    > [!NOTE]
    >  Si vous souhaitez créer une liste d’objets métier à lier avec Windows Forms, vous devez envisager d’utiliser le <xref:System.ComponentModel.BindingList%601>. Le <xref:System.ComponentModel.BindingList%601> est une classe extensible qui implémente les interfaces principales requises pour la liaison de données Windows Forms bidirectionnelle.  
  
-   <xref:System.ComponentModel.IBindingList> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IBindingList> interface fournit un niveau plus élevé de fonctionnalités de liaison de données. Cette implémentation fournit des fonctionnalités de tri de base et une notification des modifications, à la fois lorsque la liste des éléments change (par exemple, le champ Adresse du troisième élément d’une liste de clients change) et lorsque la liste elle-même change (par exemple, augmentation ou diminution du nombre d’éléments de la liste). La notification des modifications est importante si vous prévoyez de lier plusieurs contrôles aux mêmes données et si vous souhaitez que les modifications apportées aux données d’un contrôle se propagent à d’autres contrôles liés.  
  
    > [!NOTE]
    >  Notification de modification est activée pour le <xref:System.ComponentModel.IBindingList> interface via la <xref:System.ComponentModel.IBindingList.SupportsChangeNotification%2A> propriété qui, lorsque `true`, déclenche un <xref:System.ComponentModel.IBindingList.ListChanged> événement, indiquant que la liste ou un élément dans la liste a changé.  
  
     Le type de modification est décrit par le <xref:System.ComponentModel.ListChangedType> propriété de le <xref:System.ComponentModel.ListChangedEventArgs> paramètre. Par conséquent, à chaque mise à jour du modèle de données, toutes les vues dépendantes, comme les autres contrôles liés à la même source de données, seront également mises à jour. Toutefois, les objets contenus dans la liste doivent avertir la liste quand ils changent afin que la liste puisse déclencher la <xref:System.ComponentModel.IBindingList.ListChanged> événement.  
  
    > [!NOTE]
    >  Le <xref:System.ComponentModel.BindingList%601> fournit une implémentation générique de la <xref:System.ComponentModel.IBindingList> interface.  
  
-   <xref:System.ComponentModel.IBindingListView> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IBindingListView> interface fournit toutes les fonctionnalités d’une implémentation de <xref:System.ComponentModel.IBindingList>, ainsi que filtrage et des avancées les fonctionnalités de tri. Cette implémentation offre un filtrage basé sur les chaînes ainsi que le tri multicolonne avec des paires direction-descripteur de propriété.  
  
-   <xref:System.ComponentModel.IEditableObject> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IEditableObject> interface permet à un objet contrôler quand les modifications apportées à cet objet deviennent permanentes. Cette implémentation vous permet le <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>, <xref:System.ComponentModel.IEditableObject.EndEdit%2A>, et <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> méthodes, qui vous permettent de restaurer les modifications apportées à l’objet. Voici une brève explication du fonctionnement de la <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>, <xref:System.ComponentModel.IEditableObject.EndEdit%2A>, et <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> méthodes et comment ils fonctionnent conjointement avec les autres pour permettre la restauration des modifications apportées aux données :  
  
    -   Le <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> méthode signale le début d’une modification sur un objet. Un objet qui implémente cette interface doit pouvoir stocker les mises à jour après le <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> appel de méthode de telle sorte que les mises à jour peuvent être ignorées si le <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> méthode est appelée. Dans la liaison de données Windows Forms, vous pouvez appeler <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> plusieurs fois dans l’étendue d’une seule transaction de modification (par exemple, <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>, <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>, <xref:System.ComponentModel.IEditableObject.EndEdit%2A>). Les implémentations de <xref:System.ComponentModel.IEditableObject> doit effectuer le suivi de s’il <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> a déjà été appelé et ignorer les appels ultérieurs à <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>. Étant donné que cette méthode peut être appelée plusieurs fois, il est important que les appels ultérieurs à celui-ci sont non destructives ; Autrement dit, suivantes <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> appels ne peuvent pas détruire les mises à jour qui ont été apportées ou modifient les données qui a été enregistrées sur le premier <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> appeler.  
  
    -   Le <xref:System.ComponentModel.IEditableObject.EndEdit%2A> méthode transmet les modifications depuis <xref:System.ComponentModel.IEditableObject.BeginEdit%2A> a été appelée dans l’objet sous-jacent, si l’objet est actuellement en mode édition.  
  
    -   Le <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> méthode ignore toutes les modifications apportées à l’objet.  
  
     Pour plus d’informations sur la façon dont <xref:System.ComponentModel.IEditableObject.BeginEdit%2A>, <xref:System.ComponentModel.IEditableObject.EndEdit%2A>, et <xref:System.ComponentModel.IEditableObject.CancelEdit%2A> méthodes de travail, consultez [enregistrer les données dans la base de données](/visualstudio/data-tools/save-data-back-to-the-database).  
  
     Cet aspect transactionnel des fonctionnalités de données est utilisé par le <xref:System.Windows.Forms.DataGridView> contrôle.  
  
-   <xref:System.ComponentModel.ICancelAddNew> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.ICancelAddNew> interface implémente généralement le <xref:System.ComponentModel.IBindingList> interface et vous permet de restaurer un ajout apporté à la source de données avec le <xref:System.ComponentModel.IBindingList.AddNew%2A> (méthode). Si votre source de données implémente la <xref:System.ComponentModel.IBindingList> interface, vous devez également qu’elle implémente le <xref:System.ComponentModel.ICancelAddNew> interface.  
  
-   <xref:System.ComponentModel.IDataErrorInfo> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IDataErrorInfo> interface permet aux objets d’offrir des informations d’erreur personnalisées aux contrôles liés :  
  
    -   Le <xref:System.ComponentModel.IDataErrorInfo.Error%2A> propriété retourne le texte du message d’erreur général (par exemple, « une erreur s’est produite »).  
  
    -   Le <xref:System.ComponentModel.IDataErrorInfo.Item%2A> propriété retourne une chaîne avec le message d’erreur spécifique à partir de la colonne (par exemple, « la valeur dans la `State` colonne n’est pas valide »).  
  
-   <xref:System.Collections.IEnumerable> interface  
  
     Une classe qui implémente le <xref:System.Collections.IEnumerable> interface est généralement utilisée par [!INCLUDE[vstecasp](../../../includes/vstecasp-md.md)]. Prise en charge de Windows Forms de cette interface est disponible uniquement via le <xref:System.Windows.Forms.BindingSource> composant.  
  
    > [!NOTE]
    >  Le <xref:System.Windows.Forms.BindingSource> composant copie tous les <xref:System.Collections.IEnumerable> éléments dans une liste séparée pour la liaison.  
  
-   <xref:System.ComponentModel.ITypedList> interface  
  
     Une classe de collections qui implémente le <xref:System.ComponentModel.ITypedList> interface offre la possibilité de contrôler l’ordre et le jeu de propriétés exposées au contrôle dépendant.  
  
    > [!NOTE]
    >  Lorsque vous implémentez le <xref:System.ComponentModel.ITypedList.GetItemProperties%2A> (méthode) et le <xref:System.ComponentModel.PropertyDescriptor> tableau n’est pas null, la dernière entrée dans le tableau sera le descripteur de propriété qui décrit la propriété de liste est une autre liste d’éléments.  
  
-   <xref:System.ComponentModel.ICustomTypeDescriptor> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.ICustomTypeDescriptor> interface fournit des informations dynamiques sur elle-même. Cette interface est similaire à <xref:System.ComponentModel.ITypedList> mais est utilisé pour les objets plutôt que les listes. Cette interface est utilisée par <xref:System.Data.DataRowView> pour projeter le schéma des lignes sous-jacentes. Une implémentation simple de <xref:System.ComponentModel.ICustomTypeDescriptor> est fournie par la <xref:System.ComponentModel.CustomTypeDescriptor> classe.  
  
    > [!NOTE]
    >  Pour prendre en charge la liaison au moment du design pour les types qui implémentent <xref:System.ComponentModel.ICustomTypeDescriptor>, le type doit également implémenter <xref:System.ComponentModel.IComponent> et exister en tant qu’instance sur le formulaire.  
  
-   <xref:System.ComponentModel.IListSource> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IListSource> interface permet la liaison de liste basée sur les objets non-list. Le <xref:System.ComponentModel.IListSource.GetList%2A> méthode de <xref:System.ComponentModel.IListSource> est utilisée pour retourner une liste pouvant être liée à partir d’un objet qui n’hérite pas de <xref:System.Collections.IList>. <xref:System.ComponentModel.IListSource> est utilisé par le <xref:System.Data.DataSet> classe.  
  
-   <xref:System.ComponentModel.IRaiseItemChangedEvents> interface  
  
     Une classe qui implémente le <xref:System.ComponentModel.IRaiseItemChangedEvents> interface est une liste pouvant être liée qui implémente également le <xref:System.ComponentModel.IBindingList> interface. Cette interface est utilisée pour indiquer si votre type déclenche <xref:System.ComponentModel.IBindingList.ListChanged> événements de type <xref:System.ComponentModel.ListChangedType.ItemChanged> via son <xref:System.ComponentModel.IRaiseItemChangedEvents.RaisesItemChangedEvents%2A> propriété.  
  
    > [!NOTE]
    >  Vous devez implémenter le <xref:System.ComponentModel.IRaiseItemChangedEvents> si votre source de données fournit la conversion de propriété en liste décrite précédemment et interagit avec le <xref:System.Windows.Forms.BindingSource> composant. Sinon, le <xref:System.Windows.Forms.BindingSource> exécute également la propriété à une conversion d’événement de liste ce qui entraîne une baisse des performances.  
  
-   <xref:System.ComponentModel.ISupportInitialize> interface  
  
     Un composant qui implémente le <xref:System.ComponentModel.ISupportInitialize> interface tire parti des optimisations par lots pour définir les propriétés et initialiser les propriétés codépendantes. Le <xref:System.ComponentModel.ISupportInitialize> contient deux méthodes :  
  
    -   <xref:System.ComponentModel.ISupportInitialize.BeginInit%2A> signale que l’initialisation d’objet démarre.  
  
    -   <xref:System.ComponentModel.ISupportInitialize.EndInit%2A> signale que l’initialisation d’objet se termine.  
  
-   <xref:System.ComponentModel.ISupportInitializeNotification> interface  
  
     Un composant qui implémente le <xref:System.ComponentModel.ISupportInitializeNotification> interface également implémente le <xref:System.ComponentModel.ISupportInitialize> interface. Cette interface vous permet de notifier d’autres <xref:System.ComponentModel.ISupportInitialize> composants que l’initialisation est terminée. Le <xref:System.ComponentModel.ISupportInitializeNotification> interface contient deux membres :  
  
    -   <xref:System.ComponentModel.ISupportInitializeNotification.IsInitialized%2A> Retourne un `boolean` valeur indiquant si le composant est initialisé.  
  
    -   <xref:System.ComponentModel.ISupportInitializeNotification.Initialized> Se produit lorsque <xref:System.ComponentModel.ISupportInitialize.EndInit%2A> est appelée.  
  
-   <xref:System.ComponentModel.INotifyPropertyChanged> interface  
  
     Une classe qui implémente cette interface est un type qui déclenche un événement lorsqu’une de ses valeurs de propriété change. Cette interface est conçue pour remplacer le modèle d’événement de modification pour chaque propriété d’un contrôle. Lorsqu’il est utilisé dans un <xref:System.ComponentModel.BindingList%601>, un objet métier doit implémenter le <xref:System.ComponentModel.INotifyPropertyChanged> interface et BindingList\`1 convertira <xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged> événements à <xref:System.ComponentModel.BindingList%601.ListChanged> événements de type <xref:System.ComponentModel.ListChangedType.ItemChanged>.  
  
    > [!NOTE]
    >  Pour modifier notification peut se produire dans une liaison entre un client lié et les données de source de votre type de source de données liée doit implémenter le <xref:System.ComponentModel.INotifyPropertyChanged> interface (recommandé) ou vous pouvez fournir *propertyName* `Changed` événements pour le type de limite, mais vous ne devez pas faire les deux.  
  
### <a name="interfaces-for-implementation-by-component-authors"></a>Interfaces pour implémentation par des auteurs de composants  
 Les interfaces suivantes sont conçues pour une utilisation par le moteur de liaison de données Windows Forms :  
  
-   <xref:System.Windows.Forms.IBindableComponent> interface  
  
     Une classe qui implémente cette interface est un composant qui n’est pas un contrôle et qui prend en charge la liaison de données. Cette classe retourne les liaisons de données et le contexte de liaison du composant via le <xref:System.Windows.Forms.IBindableComponent.DataBindings%2A> et <xref:System.Windows.Forms.IBindableComponent.BindingContext%2A> propriétés de cette interface.  
  
    > [!NOTE]
    >  Si votre composant hérite <xref:System.Windows.Forms.Control>, vous n’avez pas besoin d’implémenter le <xref:System.Windows.Forms.IBindableComponent> interface.  
  
-   <xref:System.Windows.Forms.ICurrencyManagerProvider> interface  
  
     Une classe qui implémente le <xref:System.Windows.Forms.ICurrencyManagerProvider> interface est un composant qui fournit son propre <xref:System.Windows.Forms.CurrencyManager> pour gérer les liaisons associées à ce composant particulier. Accès à la personnalisée <xref:System.Windows.Forms.CurrencyManager> est fournie par le <xref:System.Windows.Forms.ICurrencyManagerProvider.CurrencyManager%2A> propriété.  
  
    > [!NOTE]
    >  Une classe qui hérite de <xref:System.Windows.Forms.Control> gère les liaisons automatiquement via son <xref:System.Windows.Forms.Control.BindingContext%2A> propriété, dans ce cas dans lequel vous devez implémenter le <xref:System.Windows.Forms.ICurrencyManagerProvider> sont relativement rares.  
  
## <a name="see-also"></a>Voir aussi

- [Liaison de données et Windows Forms](data-binding-and-windows-forms.md)
- [Procédure : créer un contrôle à liaison simple dans un formulaire Windows](how-to-create-a-simple-bound-control-on-a-windows-form.md)
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
