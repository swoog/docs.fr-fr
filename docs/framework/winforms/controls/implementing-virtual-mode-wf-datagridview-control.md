---
title: 'Procédure pas à pas : implémentation du mode virtuel dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data [Windows Forms], managing large data sets
- DataGridView control [Windows Forms], virtual mode
- virtual mode [Windows Forms], walkthroughs
- DataGridView control [Windows Forms], large data sets
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: 74eb5276-5ab8-4ce0-8005-dae751d85f7c
ms.openlocfilehash: 9e7fb3a42b56c40f713d73e3734142f4aab335f4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64649993"
---
# <a name="walkthrough-implementing-virtual-mode-in-the-windows-forms-datagridview-control"></a>Procédure pas à pas : implémentation du mode virtuel dans le contrôle DataGridView Windows Forms
Lorsque vous souhaitez afficher de très grandes quantités de données tabulaires dans un <xref:System.Windows.Forms.DataGridView> contrôle, vous pouvez définir le <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété `true` et gérer explicitement l’interaction du contrôle avec son magasin de données. Cela vous permet d’optimiser les performances du contrôle dans cette situation.  
  
 Le <xref:System.Windows.Forms.DataGridView> contrôle fournit plusieurs événements que vous pouvez gérer pour interagir avec un magasin de données personnalisé. Cette procédure pas à pas vous guide tout au long du processus d’implémentation de ces gestionnaires d’événements. L’exemple de code dans cette rubrique utilise une source de données très simple à titre d’illustration. Dans un environnement de production, vous chargez en général uniquement les lignes que vous avez besoin d’afficher dans un cache et de traiter <xref:System.Windows.Forms.DataGridView> événements manipuler et mettre à jour le cache. Pour plus d’informations, consultez [implémentation du Mode virtuel avec le chargement de données juste à temps dans le contrôle de DataGridView Windows Forms](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)  
  
 Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Implémenter le Mode virtuel dans les Windows Forms DataGridView Control](how-to-implement-virtual-mode-in-the-windows-forms-datagridview-control.md).  
  
## <a name="creating-the-form"></a>Création du formulaire  
  
#### <a name="to-implement-virtual-mode"></a>Pour implémenter le mode virtuel  
  
1. Créez une classe qui dérive de <xref:System.Windows.Forms.Form> et contient un <xref:System.Windows.Forms.DataGridView> contrôle.  
  
     Le code suivant contient une initialisation de base. Il déclare des variables qui seront utilisés dans les étapes ultérieures, fournit un `Main` (méthode) et fournit une disposition de formulaire simple dans le constructeur de classe.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#001](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#001)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#001](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#001)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#001](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#001)]  
    [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#002](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#002)]
    [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#002](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#002)]
    [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#002](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#002)]  
  
2. Implémenter un gestionnaire pour votre formulaire <xref:System.Windows.Forms.Form.Load> événement qui initialise le <xref:System.Windows.Forms.DataGridView> contrôler et remplit le magasin de données avec des exemples de valeurs.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#110](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#110)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#110](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#110)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#110](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#110)]  
  
3. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellValueNeeded> événement qui Récupère la valeur de cellule demandée à partir du magasin de données ou le `Customer` objet en cours de modification.  
  
     Cet événement se produit chaque fois que le <xref:System.Windows.Forms.DataGridView> contrôle doit peindre une cellule.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#120](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#120)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#120](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#120)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#120](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#120)]  
  
4. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellValuePushed> événement qui stocke une valeur de cellule modifiée dans le `Customer` objet qui représente la ligne modifiée. Cet événement se produit chaque fois que l’utilisateur valide une modification de valeur de cellule.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#130](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#130)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#130](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#130)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#130](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#130)]  
  
5. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.NewRowNeeded> événement qui crée un `Customer` objet représentant une ligne nouvellement créée.  
  
     Cet événement se produit chaque fois que l’utilisateur entre dans la ligne pour les nouveaux enregistrements.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#140](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#140)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#140](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#140)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#140](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#140)]  
  
6. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.RowValidated> événement qui enregistre les lignes nouvelles ou modifiées dans le magasin de données.  
  
     Cet événement se produit lorsque l’utilisateur modifie la ligne actuelle.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#150](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#150)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#150](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#150)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#150](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#150)]  
  
7. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded> événement qui indique si le <xref:System.Windows.Forms.DataGridView.CancelRowEdit> événement se produit lorsque l’utilisateur signale une inversion de ligne en appuyant sur ÉCHAP deux fois en mode édition ou qu’une seule fois à l’extérieur en mode édition.  
  
     Par défaut, <xref:System.Windows.Forms.DataGridView.CancelRowEdit> se produit après inversion de ligne lorsque toutes les cellules de la ligne actuelle ont été modifiées, sauf si le <xref:System.Windows.Forms.QuestionEventArgs.Response%2A?displayProperty=nameWithType> propriété est définie sur `true` dans le <xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded> Gestionnaire d’événements. Cet événement est utile lorsque la portée de validation est déterminée au moment de l’exécution.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#160](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#160)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#160](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#160)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#160](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#160)]  
  
8. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CancelRowEdit> événement qui ignore les valeurs de la `Customer` objet représentant la ligne actuelle.  
  
     Cet événement se produit lorsque l’utilisateur signale une inversion de ligne en appuyant sur ÉCHAP deux fois en mode édition ou qu’une seule fois à l’extérieur en mode édition. Cet événement ne se produit pas si aucune cellule dans la ligne actuelle a été modifiée ou si la valeur de la <xref:System.Windows.Forms.QuestionEventArgs.Response%2A?displayProperty=nameWithType> propriété a été définie sur `false` dans un <xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded> Gestionnaire d’événements.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#170](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#170)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#170](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#170)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#170](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#170)]  
  
9. Implémenter un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.UserDeletingRow> événement qui supprime un `Customer` objet à partir du magasin de données ou ignore un non enregistrées `Customer` objet représentant une ligne nouvellement créée.  
  
     Cet événement se produit chaque fois que l’utilisateur supprime une ligne en cliquant sur un en-tête de ligne et en appuyant sur la touche SUPPR.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#180](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#180)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#180](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#180)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#180](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#180)]  
  
10. Implémenter une simple `Customers` classe pour représenter les éléments de données utilisés par cet exemple de code.  
  
     [!code-cpp[System.Windows.Forms.DataGridView.VirtualMode#200](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CPP/virtualmode.cpp#200)]
     [!code-csharp[System.Windows.Forms.DataGridView.VirtualMode#200](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/CS/virtualmode.cs#200)]
     [!code-vb[System.Windows.Forms.DataGridView.VirtualMode#200](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.VirtualMode/VB/virtualmode.vb#200)]  
  
## <a name="testing-the-application"></a>Test de l'application  
 Vous pouvez maintenant tester le formulaire pour vous assurer qu’il se comporte comme prévu.  
  
#### <a name="to-test-the-form"></a>Pour tester le formulaire  
  
- Compilez et exécutez l'application.  
  
     Vous verrez un <xref:System.Windows.Forms.DataGridView> contrôle rempli avec trois enregistrements de client. Vous pouvez modifier les valeurs de plusieurs cellules dans une ligne et appuyez sur ÉCHAP deux fois en mode édition et une fois en dehors du mode d’édition pour rétablir la ligne entière pour ses valeurs d’origine. Lorsque vous modifiez, ajouter ou supprimer des lignes dans le contrôle, `Customer` objets dans le magasin de données soient modifiés, ajoutés ou supprimés.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Cette application vous donne une compréhension élémentaire des événements que vous devez gérer pour implémenter le mode virtuel dans le <xref:System.Windows.Forms.DataGridView> contrôle. Vous pouvez améliorer cette application de base de plusieurs façons :  
  
- Implémenter un magasin de données qui met en cache les valeurs à partir d’une base de données externe. Le cache doit récupérer et ignorer les valeurs en fonction des besoins afin qu’il contienne uniquement ce qui est nécessaire pour l’affichage tout en consommant une petite quantité de mémoire sur l’ordinateur client.  
  
- Optimiser les performances de la banque de données selon vos besoins. Par exemple, vous souhaiterez peut-être compenser pour les connexions réseau lentes plutôt que des limitations de mémoire d’ordinateur du client en utilisant une plus grande taille de cache et en réduisant le nombre de requêtes de base de données.  
  
 Pour plus d’informations sur la mise en cache des valeurs à partir d’une base de données externe, consultez [Comment : Implémenter le Mode virtuel avec le chargement de données juste-à-temps dans les Windows Forms DataGridView Control](virtual-mode-with-just-in-time-data-loading-in-the-datagrid.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>
- <xref:System.Windows.Forms.DataGridView.CellValueNeeded>
- <xref:System.Windows.Forms.DataGridView.CellValuePushed>
- <xref:System.Windows.Forms.DataGridView.NewRowNeeded>
- <xref:System.Windows.Forms.DataGridView.RowValidated>
- <xref:System.Windows.Forms.DataGridView.RowDirtyStateNeeded>
- <xref:System.Windows.Forms.DataGridView.CancelRowEdit>
- <xref:System.Windows.Forms.DataGridView.UserDeletingRow>
- [Réglage des performances dans le contrôle DataGridView Windows Forms](performance-tuning-in-the-windows-forms-datagridview-control.md)
- [Meilleures pratiques pour la mise à l'échelle du contrôle DataGridView Windows Forms](best-practices-for-scaling-the-windows-forms-datagridview-control.md)
- [Implémentation du mode virtuel avec le chargement immédiat des données dans le contrôle DataGridView Windows Forms](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)
- [Guide pratique pour Implémenter le Mode virtuel dans le contrôle de DataGridView Windows Forms](how-to-implement-virtual-mode-in-the-windows-forms-datagridview-control.md)
