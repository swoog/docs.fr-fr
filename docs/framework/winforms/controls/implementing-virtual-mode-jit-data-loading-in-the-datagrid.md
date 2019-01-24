---
title: Implémentation du mode virtuel avec le chargement de données juste-à-temps dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], just-in-time data loading
- data [Windows Forms], managing large data sets
- DataGridView control [Windows Forms], virtual mode
- just-in-time data loading
- DataGridView control [Windows Forms], large data sets
- virtual mode [Windows Forms], just-in-time data loading
ms.assetid: c2a052b9-423c-4ff7-91dc-d8c7c79345f6
ms.openlocfilehash: c8290fe7722dba564bf5addab662a9f6b62d924f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607879"
---
# <a name="implementing-virtual-mode-with-just-in-time-data-loading-in-the-windows-forms-datagridview-control"></a>Implémentation du mode virtuel avec le chargement de données juste-à-temps dans le contrôle DataGridView Windows Forms
Une des raisons d’implémenter le mode virtuel dans le <xref:System.Windows.Forms.DataGridView> contrôle consiste à récupérer des données uniquement qu’il est nécessaire. Il s’agit *lors du chargement de données juste-à-temps*.  
  
 Si vous travaillez avec une table très volumineuse dans une base de données distante, par exemple, vous souhaiterez éviter les retards de démarrage en extrayant uniquement les données qui sont nécessaires pour l’affichage et des données supplémentaires uniquement lorsque l’utilisateur fait défiler de nouvelles lignes dans la vue. Si les ordinateurs clients exécutant votre application ont une quantité limitée de mémoire disponible pour le stockage des données, vous souhaiterez également ignorer les données inutilisées lors de la récupération de nouvelles valeurs à partir de la base de données.  
  
 Les sections suivantes décrivent comment utiliser un <xref:System.Windows.Forms.DataGridView> contrôle avec un cache juste-à-temps.  
  
 Pour copier le code dans cette rubrique sous forme de liste unique, consultez [Comment : Implémenter le Mode virtuel avec le chargement de données juste-à-temps dans les Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/virtual-mode-with-just-in-time-data-loading-in-the-datagrid.md).  
  
## <a name="the-form"></a>Le formulaire  
 L’exemple de code suivant définit un formulaire contenant en lecture seule <xref:System.Windows.Forms.DataGridView> contrôle interagit avec un `Cache` objet via un <xref:System.Windows.Forms.DataGridView.CellValueNeeded> Gestionnaire d’événements. Le `Cache` objet gère les valeurs stockées localement et utilise un `DataRetriever` objet pour récupérer des valeurs à partir de la table Orders de la base de données exemple Northwind. Le `DataRetriever` objet qui implémente le `IDataPageRetriever` interface requise par le `Cache` class, est également utilisé pour initialiser le <xref:System.Windows.Forms.DataGridView> contrôler les lignes et colonnes.  
  
 Le `IDataPageRetriever`, `DataRetriever`, et `Cache` types sont décrits plus loin dans cette rubrique.  
  
> [!NOTE]
>  Le stockage d'informations sensibles (telles qu'un mot de passe) dans la chaîne de connexion peut affecter la sécurité de votre application. L'utilisation de l'authentification Windows (également appelée sécurité intégrée) offre un moyen plus sûr de contrôler l'accès à une base de données. Pour plus d’informations, consultez [Protection des informations de connexion](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
 [!code-csharp[System.Windows.Forms.DataGridView.Virtual_lazyloading#100](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/CS/lazyloading.cs#100)]
 [!code-vb[System.Windows.Forms.DataGridView.Virtual_lazyloading#100](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/VB/lazyloading.vb#100)]  
  
## <a name="the-idatapageretriever-interface"></a>L’Interface IDataPageRetriever  
 L’exemple de code suivant définit la `IDataPageRetriever` interface, qui est implémentée par le `DataRetriever` classe. La seule méthode déclarée dans cette interface est le `SupplyPageOfData` (méthode), qui requiert un index de ligne initial et un décompte du nombre de lignes dans une seule page de données. Ces valeurs sont utilisées par l’implémenteur pour récupérer un sous-ensemble de données à partir d’une source de données.  
  
 Un `Cache` objet utilise une implémentation de cette interface pendant la construction pour charger les deux premières pages de données. Chaque fois qu’une valeur non mis en cache est nécessaire, le cache ignore l’une de ces pages et demande une nouvelle page contenant la valeur à partir de la `IDataPageRetriever`.  
  
 [!code-csharp[System.Windows.Forms.DataGridView.Virtual_lazyloading#201](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/CS/lazyloading.cs#201)]
 [!code-vb[System.Windows.Forms.DataGridView.Virtual_lazyloading#201](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/VB/lazyloading.vb#201)]  
  
## <a name="the-dataretriever-class"></a>La classe DataRetriever  
 L’exemple de code suivant définit la `DataRetriever` classe qui implémente le `IDataPageRetriever` interface pour récupérer les pages de données à partir d’un serveur. Le `DataRetriever` classe fournit également `Columns` et `RowCount` propriétés, ce qui le <xref:System.Windows.Forms.DataGridView> contrôle utilise pour créer les colonnes nécessaires et ajouter le nombre approprié de lignes vides pour les <xref:System.Windows.Forms.DataGridView.Rows%2A> collection. Ajout de lignes vides est nécessaire afin que le contrôle se comporte comme s’il contient toutes les données dans la table. Cela signifie que la case de défilement dans la barre de défilement aura la taille appropriée, et l’utilisateur sera en mesure d’accéder à n’importe quelle ligne dans la table. Les lignes sont remplies par la <xref:System.Windows.Forms.DataGridView.CellValueNeeded> Gestionnaire d’événements uniquement lorsqu’ils défilent dans l’affichage.  
  
 [!code-csharp[System.Windows.Forms.DataGridView.Virtual_lazyloading#200](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/CS/lazyloading.cs#200)]
 [!code-vb[System.Windows.Forms.DataGridView.Virtual_lazyloading#200](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/VB/lazyloading.vb#200)]  
  
## <a name="the-cache-class"></a>La classe de Cache  
 L’exemple de code suivant définit la `Cache` (classe), qui gère deux pages de données remplies via un `IDataPageRetriever` implémentation. Le `Cache` classe définit interne `DataPage` structure qui contient un <xref:System.Data.DataTable> pour stocker les valeurs dans un seul cache page et qui calcule les index de ligne qui représentent les limites supérieures et inférieures de la page.  
  
 Le `Cache` classe charge deux pages de données au moment de la construction. Chaque fois que le <xref:System.Windows.Forms.DataGridView.CellValueNeeded> événement demande une valeur, le `Cache` objet détermine si la valeur est disponible dans un de ses deux pages et, dans ce cas, il retourne. Si la valeur n’est pas disponible localement, le `Cache` objet détermine laquelle de ses deux pages est le plus éloigné de lignes actuellement affichées et remplace la page avec un fichier contenant la valeur demandée, elle retourne ensuite.  
  
 En supposant que le nombre de lignes dans une page de données est le même que le nombre de lignes qui peuvent être affichés à la fois sur l’écran, ce modèle permet aux utilisateurs la pagination via la table de retourner efficacement à la dernière page affichée.  
  
 [!code-csharp[System.Windows.Forms.DataGridView.Virtual_lazyloading#300](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/CS/lazyloading.cs#300)]
 [!code-vb[System.Windows.Forms.DataGridView.Virtual_lazyloading#300](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.Virtual_lazyloading/VB/lazyloading.vb#300)]  
  
## <a name="additional-considerations"></a>Considérations supplémentaires  
 Les exemples de code précédents sont fournis comme démonstration juste-à-temps de chargement de données. Vous devrez modifier le code pour vos propres besoins pour obtenir une efficacité maximale. Au minimum, vous devez choisir une valeur appropriée pour le nombre de lignes par page de données dans le cache. Cette valeur est passée dans le `Cache` constructeur. Le nombre de lignes par page doit être non inférieur au nombre de lignes qui peuvent être affichées simultanément dans votre <xref:System.Windows.Forms.DataGridView> contrôle.  
  
 Pour de meilleurs résultats, vous devrez effectuer des tests de performances et facilité d’utilisation des tests pour déterminer les besoins de votre système et vos utilisateurs. Plusieurs facteurs dont vous aurez besoin de prendre en considération incluent la quantité de mémoire dans les ordinateurs clients exécutant votre application, la bande passante disponible de la connexion réseau utilisée et la latence du serveur utilisé. La bande passante et la latence doivent être déterminées dans certains cas d’utilisation maximale.  
  
 Pour améliorer les performances de défilement de votre application, vous pouvez augmenter la quantité de données stockées localement. Pour améliorer les temps de démarrage, toutefois, vous devez éviter de charger trop de données initialement. Vous pouvez souhaiter modifier le `Cache` classe pour augmenter le nombre de pages de données qu’elle peut stocker. L’utilisation de plusieurs pages de données peut améliorer l’efficacité de défilement, mais vous devrez déterminer le nombre idéal de lignes dans une page de données, en fonction de la bande passante disponible et la latence du serveur. Avec des pages plus petites, le serveur est accessible plus fréquemment, mais prend moins de temps pour renvoyer les données demandées. Si la latence est plus un problème que la bande passante, vous souhaiterez utiliser les pages de données plus volumineux.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>
- [Réglage des performances dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/performance-tuning-in-the-windows-forms-datagridview-control.md)
- [Meilleures pratiques pour la mise à l'échelle du contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)
- [Mode virtuel dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/virtual-mode-in-the-windows-forms-datagridview-control.md)
- [Procédure pas à pas : Implémentation du Mode virtuel dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/implementing-virtual-mode-wf-datagridview-control.md)
- [Guide pratique pour Implémenter le Mode virtuel avec le chargement de données juste-à-temps dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/virtual-mode-with-just-in-time-data-loading-in-the-datagrid.md)
