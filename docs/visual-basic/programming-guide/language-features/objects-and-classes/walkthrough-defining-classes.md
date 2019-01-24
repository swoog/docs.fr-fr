---
title: Définition de Classes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- execution [Visual Basic], ending
- objects [Visual Basic], initializing
- Initialize event [Visual Basic]
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- objects [Visual Basic], creating
- program termination
- classes [Visual Basic], walkthroughs
- class modules, walkthroughs
- Terminate event [Visual Basic]
- execution [Visual Basic], stopping
ms.assetid: 07018828-2d49-4cf5-a44b-19fb15d9efea
ms.openlocfilehash: c41d3b2c8d905395f1249b15709da8dbdf5d4632
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640431"
---
# <a name="walkthrough-defining-classes-visual-basic"></a>Procédure pas à pas : Définition de Classes (Visual Basic)

Cette procédure pas à pas montre comment définir des classes que vous pouvez ensuite utiliser pour créer des objets. Il vous montre comment ajouter des propriétés et méthodes à la nouvelle classe et vous montre comment initialiser un objet.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="to-define-a-class"></a>Pour définir une classe
  
1.  Créez un projet en cliquant sur **nouveau projet** sur le **fichier** menu. La boîte de dialogue **Nouveau projet** s’affiche.  
  
2.  Sélectionnez les applications Windows à partir de la liste des modèles de projet Visual Basic pour afficher le nouveau projet.  
  
3.  Ajoutez une nouvelle classe au projet en cliquant sur **ajouter une classe** sur le **projet** menu. La boîte de dialogue **Ajouter un nouvel élément** s’affiche.  
  
4.  Sélectionnez le **classe** modèle.  
  
5.  Nommez la nouvelle classe `UserNameInfo.vb`, puis cliquez sur **ajouter** pour afficher le code pour la nouvelle classe.  
  
     [!code-vb[VbVbalrOOP#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#5)]
  
    > [!NOTE]
    >  Vous pouvez utiliser Visual Basic **éditeur de Code** pour ajouter une classe à votre formulaire de démarrage en tapant le `Class` mot clé suivie du nom de la nouvelle classe. Le **éditeur de Code** fournit un correspondant `End Class` instruction pour vous.  
  
6.  Définir un champ privé pour la classe en ajoutant le code suivant entre les `Class` et `End Class` instructions :  
  
     [!code-vb[VbVbalrOOP#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#7)]
  
     Déclaration du champ en tant que `Private` signifie qu’il peut être utilisé uniquement dans la classe. Vous pouvez rendre les champs disponibles à partir de l’extérieur d’une classe à l’aide des modificateurs d’accès comme `Public` qui fournissent un accès plus. Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
7.  Définir une propriété pour la classe en ajoutant le code suivant :  
  
     [!code-vb[VbVbalrOOP#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#8)]
  
8.  Définissez une méthode pour la classe en ajoutant le code suivant :  
  
     [!code-vb[VbVbalrOOP#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#9)]
  
9. Définir un constructeur paramétrable pour la nouvelle classe en ajoutant une procédure nommée `Sub New`:  
  
     [!code-vb[VbVbalrOOP#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#10)]
  
     Le `Sub New` est appelé automatiquement lorsqu’un objet basé sur cette classe est créé. Ce constructeur définit la valeur du champ qui contient le nom d’utilisateur.  
  
## <a name="to-create-a-button-to-test-the-class"></a>Pour créer un bouton pour tester la classe
  
1.  Modifiez le formulaire de démarrage en mode design en cliquant sur son nom dans **l’Explorateur de solutions** , puis en cliquant sur **Concepteur de vues**. Par défaut, le formulaire de démarrage pour les projets d’Application de Windows est nommé Form1.vb. Le formulaire principal s’affiche alors.  
  
2.  Ajoutez un bouton au formulaire principal et double-cliquez dessus pour afficher le code pour le `Button1_Click` Gestionnaire d’événements. Ajoutez le code suivant pour appeler la procédure de test :  
  
     [!code-vb[VbVbalrOOP#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#12)]
  
## <a name="to-run-your-application"></a>Pour exécuter votre application
  
1.  Exécutez votre application en appuyant sur F5. Cliquez sur le bouton sur le formulaire pour appeler la procédure de test. Il affiche un message indiquant que l’original `UserName` est « MOORE, BOBBY », car la procédure appelée le `Capitalize` méthode de l’objet.  
  
2.  Cliquez sur **OK** pour fermer la boîte de message. Le `Button1 Click` procédure modifie la valeur de la `UserName` propriété et affiche un message indiquant que la nouvelle valeur de `UserName` est « Worden, Joe ».  
  
## <a name="see-also"></a>Voir aussi

- [Programmation orientée objet (Visual Basic)](../../concepts/object-oriented-programming.md)
- [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
