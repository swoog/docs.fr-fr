---
title: 'Procédure pas à pas : disposition des contrôles Windows Forms avec le remplissage, les marges et la propriété AutoSize'
ms.date: 03/30/2017
f1_keywords:
- Margin.Bottom
- Margin.Left
- Margin.Top
- Margin.All
- Margin.Right
helpviewer_keywords:
- Margin property [Windows Forms], walkthroughs
- walkthroughs [Windows Forms], layout
- AutoSize property [Windows Forms], walkthroughs
- Padding property [Windows Forms], walkthroughs
- layout [Windows Forms], margins and padding
- Windows Forms, layout
ms.assetid: f8ae2a6b-db13-4630-8e25-d104091205c7
ms.openlocfilehash: c07afa1e408c2950ea45f206f43125fc9329ad14
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59167867"
---
# <a name="walkthrough-laying-out-windows-forms-controls-with-padding-margins-and-the-autosize-property"></a>Procédure pas à pas : disposition des contrôles Windows Forms avec le remplissage, les marges et la propriété AutoSize
Le positionnement précis des contrôles sur votre formulaire constitue une haute priorité pour de nombreuses applications. Le **Windows Forms Designer** vous offre de nombreux outils de disposition pour effectuer cette opération. Trois des plus importants sont la <xref:System.Windows.Forms.Control.Margin%2A>, <xref:System.Windows.Forms.Control.Padding%2A>, et <xref:System.Windows.Forms.Control.AutoSize%2A> propriétés, qui sont présentes sur tous les contrôles Windows Forms.  
  
 La propriété <xref:System.Windows.Forms.Control.Margin%2A> définit l'espace autour du contrôle qui maintient les autres contrôles à une distance spécifiée des bordures du contrôle.  
  
 La propriété <xref:System.Windows.Forms.Control.Padding%2A> définit l'espace à l'intérieur d'un contrôle qui maintient le contenu du contrôle (par exemple la valeur de sa propriété <xref:System.Windows.Forms.Control.Text%2A>) à une distance spécifiée des bordures du contrôle.  
  
 L'illustration suivante montre les propriétés <xref:System.Windows.Forms.Control.Padding%2A> et <xref:System.Windows.Forms.Control.Margin%2A> d'un contrôle.  
  
 ![Remplissage et marge pour les Windows Forms contrôles](./media/vs-winformpadmargin.gif "VS_WinFormPadMargin")  
  
 Le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété indique à un contrôle d’ajuster automatiquement sa taille à son contenu. Il ne se redimensionnera pas pour être plus petite que la valeur de son état d’origine <xref:System.Windows.Forms.Control.Size%2A> propriété et il représentera la valeur de son <xref:System.Windows.Forms.Control.Padding%2A> propriété.  
  
 Cette procédure pas à pas décrit notamment les tâches suivantes :  
  
-   Création d’un projet Windows Forms  
  
-   Définition des marges de vos contrôles  
  
-   Définition du remplissage de vos contrôles  
  
-   Dimensionnement automatique de vos contrôles  
  
 À l’issue de cette procédure, vous comprendrez le rôle joué par ces fonctionnalités de disposition importantes.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
## <a name="prerequisites"></a>Prérequis  
 Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :  
  
-   Autorisations suffisantes pour pouvoir créer et exécuter des projets d’application Windows Forms sur l’ordinateur où Visual Studio est installé.  
  
## <a name="creating-the-project"></a>Création du projet  
 La première étape consiste à créer le projet et à configurer le formulaire.  
  
#### <a name="to-create-the-project"></a>Pour créer le projet  
  
1.  Créer un **Windows Application** projet appelé `LayoutExample`. Pour plus d'informations, voir [Procédure : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) .  
  
2.  Sélectionnez le formulaire dans le **Windows Forms Designer**.  
  
## <a name="setting-margins-for-your-controls"></a>Définition des marges de vos contrôles  
 Vous pouvez définir la distance par défaut entre vos contrôles à l’aide de la <xref:System.Windows.Forms.Control.Margin%2A> propriété. Lorsque vous déplacez un contrôle suffisamment proches d’un autre contrôle, vous voyez une ligne d’alignement qui affiche les marges pour les deux contrôles. Le contrôle que vous déplacez s’aligne également à la distance définie par les marges.  
  
#### <a name="to-arrange-controls-on-your-form-using-the-margin-property"></a>Pour réorganiser des contrôles sur votre formulaire à l’aide de la propriété Margin  
  
1.  Faites glisser deux <xref:System.Windows.Forms.Button> des contrôles de la **boîte à outils** vers votre formulaire.  
  
2.  Sélectionnez une de la <xref:System.Windows.Forms.Button> contrôle et déplacez-le proche de l’autre, jusqu'à ce qu’ils se touchent presque.  
  
     Observez la ligne d’alignement qui apparaît entre eux. Cette distance est la somme des deux contrôles <xref:System.Windows.Forms.Control.Margin%2A> valeurs. Le contrôle que vous déplacez s’aligne sur cette distance. Pour plus d’informations, consultez [procédure pas à pas : Organisation des contrôles dans les Windows Forms à l’aide des lignes d’alignement](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).  
  
3.  Modification la <xref:System.Windows.Forms.Control.Margin%2A> propriété de l’un des contrôles en développant le <xref:System.Windows.Forms.Control.Margin%2A> entrée dans le **propriétés** fenêtre et en définissant le <xref:System.Windows.Forms.Padding.All%2A> propriété à 20.  
  
4.  Sélectionnez une de la <xref:System.Windows.Forms.Button> contrôle et déplacez-le proche de l’autre.  
  
     La ligne d’alignement définissant la somme des valeurs de marge est plus longue et que le contrôle s’aligne sur une distance supérieure à partir de l’autre contrôle.  
  
5.  Modification la <xref:System.Windows.Forms.Control.Margin%2A> propriété du contrôle sélectionné en développant le <xref:System.Windows.Forms.Control.Margin%2A> entrée dans le **propriétés** fenêtre et en définissant le <xref:System.Windows.Forms.Padding.Top%2A> propriété à 5.  
  
6.  Déplacer le contrôle sélectionné sous l’autre contrôle et observez que la ligne d’alignement est plus courte. Déplacer le contrôle sélectionné vers la gauche de l’autre contrôle et observez que la ligne d’alignement conserve la valeur observée à l’étape 4.  
  
7.  Vous pouvez définir chacun des aspects de la <xref:System.Windows.Forms.Control.Margin%2A> propriété, <xref:System.Windows.Forms.Padding.Left%2A>, <xref:System.Windows.Forms.Padding.Top%2A>, <xref:System.Windows.Forms.Padding.Right%2A>, <xref:System.Windows.Forms.Padding.Bottom%2A>, pour des valeurs différentes, ou vous peut affecter tous la même valeur avec le <xref:System.Windows.Forms.Padding.All%2A> propriété.  
  
## <a name="setting-padding-for-your-controls"></a>Définition du remplissage de vos contrôles  
 Pour obtenir la disposition précise requise pour votre application, vos contrôles contient souvent des contrôles enfants. Lorsque vous souhaitez spécifier la proximité de la bordure du contrôle de l’enfant sur sa bordure du contrôle parent, utilisez le contrôle parent <xref:System.Windows.Forms.Control.Padding%2A> propriété conjointement avec le contrôle enfant <xref:System.Windows.Forms.Control.Margin%2A> propriété. Le <xref:System.Windows.Forms.Control.Padding%2A> propriété est également utilisée pour contrôler la proximité du contenu d’un contrôle (par exemple, un <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Text%2A> propriété) à ses bordures.  
  
#### <a name="to-arrange-controls-on-your-form-using-padding"></a>Pour réorganiser des contrôles sur votre formulaire à l’aide de la marge intérieure  
  
1.  Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **boîte à outils** vers le formulaire.  
  
2.  Affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Control.AutoSize%2A> du contrôle <xref:System.Windows.Forms.Button>.  
  
3.  Modification la <xref:System.Windows.Forms.Control.Padding%2A> en développant le <xref:System.Windows.Forms.Control.Padding%2A> entrée dans le **propriétés** fenêtre et en définissant le <xref:System.Windows.Forms.Padding.All%2A> propriété à 5.  
  
     Le contrôle se développe pour fournir la place pour le nouveau remplissage.  
  
4.  Faites glisser un contrôle <xref:System.Windows.Forms.GroupBox> de la **boîte à outils** vers le formulaire. Faites glisser un <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** dans le <xref:System.Windows.Forms.GroupBox> contrôle. Position du <xref:System.Windows.Forms.Button> contrôler par conséquent, il est aligné dans le coin inférieur droit de la <xref:System.Windows.Forms.GroupBox> contrôle.  
  
     Observez les lignes d’alignement apparaissent sous la forme la <xref:System.Windows.Forms.Button> contrôle approche les bordures inférieure et droite de la <xref:System.Windows.Forms.GroupBox> contrôle. Ces lignes d’alignement correspondent à la <xref:System.Windows.Forms.Control.Margin%2A> propriété de la <xref:System.Windows.Forms.Button>.  
  
5.  Modification la <xref:System.Windows.Forms.GroupBox> du contrôle <xref:System.Windows.Forms.Control.Padding%2A> en développant le <xref:System.Windows.Forms.Control.Padding%2A> entrée dans le **propriétés** fenêtre et en définissant le <xref:System.Windows.Forms.Padding.All%2A> propriété à 20.  
  
6.  Sélectionnez le <xref:System.Windows.Forms.Button> contrôler au sein de la <xref:System.Windows.Forms.GroupBox> contrôle et déplacez-le vers le centre de la <xref:System.Windows.Forms.GroupBox>.  
  
     Les lignes d’alignement apparaissent à une distance supérieure à partir des bordures de la <xref:System.Windows.Forms.GroupBox> contrôle. Cette distance est la somme de la <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Margin%2A> propriété et la <xref:System.Windows.Forms.GroupBox> du contrôle <xref:System.Windows.Forms.Control.Padding%2A> propriété.  
  
## <a name="automatically-sizing-your-controls"></a>Dimensionnement automatique de vos contrôles  
 Dans certaines applications, la taille d’un contrôle aura le même en cours d’exécution tel qu’il était au moment du design. Le texte d’un <xref:System.Windows.Forms.Button> contrôle, par exemple, peut-être être prise à partir d’une base de données, et sa longueur ne sera pas connue à l’avance.  
  
 Lorsque le <xref:System.Windows.Forms.Control.AutoSize%2A> propriété est définie sur `true`, le contrôle ajuste sa taille à son contenu. Pour plus d’informations, consultez [vue d’ensemble de la propriété AutoSize](autosize-property-overview.md).  
  
#### <a name="to-arrange-controls-on-your-form-using-the-autosize-property"></a>Pour réorganiser des contrôles sur votre formulaire à l’aide de la propriété AutoSize  
  
1.  Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **boîte à outils** vers le formulaire.  
  
2.  Affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Control.AutoSize%2A> du contrôle <xref:System.Windows.Forms.Button>.  
  
3.  Modifier le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Text%2A> propriété à « **ce bouton a une longue chaîne pour sa propriété Text** »  
  
     Lorsque vous validez la modification, le <xref:System.Windows.Forms.Button> contrôle est redimensionné pour s’adapter au nouveau texte.  
  
4.  Faites glisser un autre <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** vers votre formulaire.  
  
5.  Modifier le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Text%2A> propriété à « **ce bouton a une longue chaîne pour sa propriété Text.** »  
  
     Lorsque vous validez la modification, le <xref:System.Windows.Forms.Button> contrôle ne se redimensionne pas, et le texte est découpé par le bord droit du contrôle.  
  
6.  Modification la <xref:System.Windows.Forms.Control.Padding%2A> en développant le <xref:System.Windows.Forms.Control.Padding%2A> entrée dans le **propriétés** fenêtre et en définissant le <xref:System.Windows.Forms.Padding.All%2A> propriété à 5.  
  
     Le texte de l’intérieur du contrôle est découpé sur les quatre côtés.  
  
7.  Modifier le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.AutoSize%2A> propriété `true`.  
  
     Le <xref:System.Windows.Forms.Button> contrôle redimensionne pour contenir la chaîne entière. En outre, le remplissage a été ajouté autour du texte, à l’origine le <xref:System.Windows.Forms.Button> contrôle pour développer dans toutes les directions.  
  
8.  Faites glisser un contrôle <xref:System.Windows.Forms.Button> de la **boîte à outils** vers le formulaire. Placez-le près du coin inférieur droit du formulaire.  
  
9. Affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Control.AutoSize%2A> du contrôle <xref:System.Windows.Forms.Button>.  
  
10. Définir le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété <xref:System.Windows.Forms.AnchorStyles.Right>, <xref:System.Windows.Forms.AnchorStyles.Bottom>.  
  
11. Modifier le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Text%2A> propriété à « **ce bouton a une longue chaîne pour sa propriété Text.** »  
  
     Lorsque vous validez la modification, le <xref:System.Windows.Forms.Button> contrôle redimensionne vers la gauche. En règle générale, le dimensionnement automatique augmente la taille d’un contrôle dans la direction opposée son <xref:System.Windows.Forms.Control.Anchor%2A> paramètre de propriété.  
  
## <a name="autosize-and-autosizemode-properties"></a>Propriétés AutoSize et AutoSizeMode  
 Certains contrôles prennent en charge le `AutoSizeMode` propriété, ce qui vous donne un contrôle plus précis sur le comportement de dimensionnement automatique d’un contrôle.  
  
#### <a name="to-use-the-autosizemode-property"></a>Pour utiliser la propriété AutoSizeMode  
  
1.  Faites glisser un contrôle <xref:System.Windows.Forms.Panel> de la **boîte à outils** vers le formulaire.  
  
2.  Définissez la valeur de la <xref:System.Windows.Forms.Panel> du contrôle <xref:System.Windows.Forms.Control.AutoSize%2A> propriété `true`.  
  
3.  Faites glisser un <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** dans le <xref:System.Windows.Forms.Panel> contrôle.  
  
4.  Place le <xref:System.Windows.Forms.Button> contrôle près du coin inférieur droit de la <xref:System.Windows.Forms.Panel> contrôle.  
  
5.  Sélectionnez le <xref:System.Windows.Forms.Panel> contrôler et saisissez la poignée de redimensionnement inférieure droite. Redimensionner le <xref:System.Windows.Forms.Panel> contrôle pour être plus grand et plus petit.  
  
    > [!NOTE]
    >  Vous pouvez redimensionner librement le <xref:System.Windows.Forms.Panel> contrôle, mais vous ne pouvez pas rendre plus petit que la position de la <xref:System.Windows.Forms.Button> bas à droite du contrôle. Ce comportement est spécifié par la valeur par défaut de la `AutoSizeMode` propriété, qui est <xref:System.Windows.Forms.AutoSizeMode.GrowOnly>.  
  
6.  Définissez la valeur de la <xref:System.Windows.Forms.Panel> du contrôle `AutoSizeMode` propriété <xref:System.Windows.Forms.AutoSizeMode.GrowAndShrink>.  
  
     Le <xref:System.Windows.Forms.Panel> contrôle se redimensionne autour du <xref:System.Windows.Forms.Button> contrôle. Vous ne pouvez pas redimensionner le <xref:System.Windows.Forms.Panel> contrôle.  
  
7.  Faites glisser le <xref:System.Windows.Forms.Button> contrôle vers le coin supérieur gauche de la <xref:System.Windows.Forms.Panel> contrôle.  
  
     Le <xref:System.Windows.Forms.Panel> contrôle est redimensionné à la <xref:System.Windows.Forms.Button> nouvelle position du contrôle.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Il existe de nombreuses autres fonctionnalités de disposition pour organiser les contrôles dans vos applications Windows Forms. Voici certaines combinaisons, que vous pouvez essayer :  
  
-   Créez un formulaire avec un <xref:System.Windows.Forms.TableLayoutPanel> contrôle. Pour plus d’informations, consultez [procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md). Essayez de modifier les valeurs de la <xref:System.Windows.Forms.TableLayoutPanel> du contrôle <xref:System.Windows.Forms.Control.Padding%2A> propriété, ainsi que le <xref:System.Windows.Forms.Control.Margin%2A> propriété sur ses contrôles enfants.  
  
-   Essayez la même expérience à l’aide un <xref:System.Windows.Forms.FlowLayoutPanel> contrôle. Pour plus d’informations, consultez [procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md).  
  
-   Expérience avec l’ancrage des contrôles enfants dans un <xref:System.Windows.Forms.Panel> contrôle. Le <xref:System.Windows.Forms.Control.Padding%2A> propriété est une réalisation plus générale de la <xref:System.Windows.Forms.ScrollableControl.DockPadding%2A> propriété et vous pouvez satisfaire à vous-même que c’est le cas en plaçant un contrôle enfant dans un <xref:System.Windows.Forms.Panel> contrôle et en définissant le contrôle enfant <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>. Définir le <xref:System.Windows.Forms.Panel> du contrôle <xref:System.Windows.Forms.Control.Padding%2A> propriété différentes valeurs et notez l’effet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.AutoSize%2A>
- <xref:System.Windows.Forms.ScrollableControl.DockPadding%2A>
- <xref:System.Windows.Forms.Control.Margin%2A>
- <xref:System.Windows.Forms.Control.Padding%2A>
- [Vue d'ensemble de la propriété AutoSize](autosize-property-overview.md)
- [Procédure pas à pas : organisation des contrôles dans Windows Forms à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Procédure pas à pas : organisation des contrôles dans des Windows Forms à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Procédure pas à pas : organisation des contrôles dans des Windows Forms à l’aide de lignes d’alignement](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
