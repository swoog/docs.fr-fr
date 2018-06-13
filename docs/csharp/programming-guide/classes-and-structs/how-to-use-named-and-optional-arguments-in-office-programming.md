---
title: Guide pratique pour utiliser des arguments nommés et facultatifs dans la programmation Office (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- named and optional arguments [C#], Office programming
- optional arguments [C#], Office programming
- named arguments [C#], Office programming
ms.assetid: 65b8a222-bcd8-454c-845f-84adff5a356f
ms.openlocfilehash: 3fce8a30e9ed663f06fa04c462fc1e1fd249d27a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33321871"
---
# <a name="how-to-use-named-and-optional-arguments-in-office-programming-c-programming-guide"></a><span data-ttu-id="f8a2c-102">Guide pratique pour utiliser des arguments nommés et facultatifs dans la programmation Office (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f8a2c-102">How to: Use Named and Optional Arguments in Office Programming (C# Programming Guide)</span></span>
<span data-ttu-id="f8a2c-103">Les arguments nommés et les arguments facultatifs, qui ont été introduits avec [!INCLUDE[csharp_dev10_long](~/includes/csharp-dev10-long-md.md)], rendent la programmation en C# plus pratique, plus souple et plus lisible.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-103">Named arguments and optional arguments, introduced in [!INCLUDE[csharp_dev10_long](~/includes/csharp-dev10-long-md.md)], enhance convenience, flexibility, and readability in C# programming.</span></span> <span data-ttu-id="f8a2c-104">De plus, ces fonctionnalités facilitent considérablement l’accès aux interfaces COM, telles que les API Microsoft Office Automation.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-104">In addition, these features greatly facilitate access to COM interfaces such as the Microsoft Office automation APIs.</span></span>  
  
 <span data-ttu-id="f8a2c-105">Dans l’exemple suivant, la méthode [ConvertToTable](https://msdn.microsoft.com/library/bb216993.aspx) a seize paramètres qui représentent les caractéristiques d’une table, comme le nombre de colonnes et de lignes, la mise en forme, les bordures, les polices et les couleurs.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-105">In the following example, method [ConvertToTable](https://msdn.microsoft.com/library/bb216993.aspx) has sixteen parameters that represent characteristics of a table, such as number of columns and rows, formatting, borders, fonts, and colors.</span></span> <span data-ttu-id="f8a2c-106">Ces seize paramètres sont facultatifs, car la plupart du temps, il n’est pas nécessaire de spécifier des valeurs pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-106">All sixteen parameters are optional, because most of the time you do not want to specify particular values for all of them.</span></span> <span data-ttu-id="f8a2c-107">Toutefois, en l’absence d’arguments nommés et facultatifs, une valeur ou une valeur d’espace réservé doit être fournie pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-107">However, without named and optional arguments, a value or a placeholder value has to be provided for each parameter.</span></span> <span data-ttu-id="f8a2c-108">Avec les arguments nommés et facultatifs, vous spécifiez des valeurs uniquement pour les paramètres qui sont nécessaires à votre projet.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-108">With named and optional arguments, you specify values only for the parameters that are required for your project.</span></span>  
  
 <span data-ttu-id="f8a2c-109">Pour que vous puissiez effectuer ces procédures, Microsoft Office Word doit être installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-109">You must have Microsoft Office Word installed on your computer to complete these procedures.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-new-console-application"></a><span data-ttu-id="f8a2c-110">Pour créer une application console</span><span class="sxs-lookup"><span data-stu-id="f8a2c-110">To create a new console application</span></span>  
  
1.  <span data-ttu-id="f8a2c-111">Démarrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-111">Start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="f8a2c-112">Dans le menu **Fichier** , pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-112">On the **File** menu, point to **New**, and then click **Project**.</span></span>  
  
3.  <span data-ttu-id="f8a2c-113">Dans le volet **Catégories de modèles**, développez **Visual C#**, puis cliquez sur **Windows**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-113">In the **Templates Categories** pane, expand **Visual C#**, and then click **Windows**.</span></span>  
  
4.  <span data-ttu-id="f8a2c-114">Regardez en haut du volet **Modèles** pour vérifier que **.NET Framework 4**, ou version ultérieure, apparaît dans la zone **Framework cible**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-114">Look in the top of the **Templates** pane to make sure that **.NET Framework 4** appears in the **Target Framework** box.</span></span>  
  
5.  <span data-ttu-id="f8a2c-115">Dans le volet **Modèles**, cliquez sur **Application console**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-115">In the **Templates** pane, click **Console Application**.</span></span>  
  
6.  <span data-ttu-id="f8a2c-116">Attribuez un nom à votre projet dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-116">Type a name for your project in the **Name** field.</span></span>  
  
7.  <span data-ttu-id="f8a2c-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-117">Click **OK**.</span></span>  
  
     <span data-ttu-id="f8a2c-118">Le nouveau projet s’affiche dans l’**Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-118">The new project appears in **Solution Explorer**.</span></span>  
  
### <a name="to-add-a-reference"></a><span data-ttu-id="f8a2c-119">Pour ajouter une référence</span><span class="sxs-lookup"><span data-stu-id="f8a2c-119">To add a reference</span></span>  
  
1.  <span data-ttu-id="f8a2c-120">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le nom de votre projet, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-120">In **Solution Explorer**, right-click your project's name and then click **Add Reference**.</span></span> <span data-ttu-id="f8a2c-121">La boîte de dialogue **Ajouter une référence** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-121">The **Add Reference** dialog box appears.</span></span>  
  
2.  <span data-ttu-id="f8a2c-122">Dans la page **.NET**, sélectionnez **Microsoft.Office.Interop.Word** dans la liste **Nom du composant**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-122">On the **.NET** page, select **Microsoft.Office.Interop.Word** in the **Component Name** list.</span></span>  
  
3.  <span data-ttu-id="f8a2c-123">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-123">Click **OK**.</span></span>  
  
### <a name="to-add-necessary-using-directives"></a><span data-ttu-id="f8a2c-124">Pour ajouter les directives using nécessaires</span><span class="sxs-lookup"><span data-stu-id="f8a2c-124">To add necessary using directives</span></span>  
  
1.  <span data-ttu-id="f8a2c-125">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier **Program.cs**, puis cliquez sur **Afficher le code**.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-125">In **Solution Explorer**, right-click the **Program.cs** file and then click **View Code**.</span></span>  
  
2.  <span data-ttu-id="f8a2c-126">Ajoutez les directives `using` suivantes en début du fichier de code.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-126">Add the following `using` directives to the top of the code file.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#4](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_1.cs)]  
  
### <a name="to-display-text-in-a-word-document"></a><span data-ttu-id="f8a2c-127">Pour afficher du texte dans un document Word</span><span class="sxs-lookup"><span data-stu-id="f8a2c-127">To display text in a Word document</span></span>  
  
1.  <span data-ttu-id="f8a2c-128">Dans la classe `Program` du fichier Program.cs, ajoutez la méthode suivante pour créer une application Word et un document Word.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-128">In the `Program` class in Program.cs, add the following method to create a Word application and a Word document.</span></span> <span data-ttu-id="f8a2c-129">La méthode [Add](https://msdn.microsoft.com/library/microsoft.office.interop.word.documents.add.aspx) comprend quatre paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-129">The [Add](https://msdn.microsoft.com/library/microsoft.office.interop.word.documents.add.aspx) method has four optional parameters.</span></span> <span data-ttu-id="f8a2c-130">Cet exemple utilise leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-130">This example uses their default values.</span></span> <span data-ttu-id="f8a2c-131">Par conséquent, aucun argument n’est nécessaire dans l’instruction appelante.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-131">Therefore, no arguments are necessary in the calling statement.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#6](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_2.cs)]  
  
2.  <span data-ttu-id="f8a2c-132">Ajoutez le code suivant à la fin de la méthode pour définir l’emplacement d’affichage du texte dans le document, ainsi que le texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-132">Add the following code at the end of the method to define where to display text in the document, and what text to display.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#7](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_3.cs)]  
  
### <a name="to-run-the-application"></a><span data-ttu-id="f8a2c-133">Pour exécuter l’application</span><span class="sxs-lookup"><span data-stu-id="f8a2c-133">To run the application</span></span>  
  
1.  <span data-ttu-id="f8a2c-134">Ajoutez l’instruction suivante à Main.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-134">Add the following statement to Main.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#8](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_4.cs)]  
  
2.  <span data-ttu-id="f8a2c-135">Appuyez sur CTRL+F5 pour exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-135">Press CTRL+F5 to run the project.</span></span> <span data-ttu-id="f8a2c-136">Un document Word contenant le texte spécifié s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-136">A Word document appears that contains the specified text.</span></span>  
  
### <a name="to-change-the-text-to-a-table"></a><span data-ttu-id="f8a2c-137">Pour convertir le texte en tableau</span><span class="sxs-lookup"><span data-stu-id="f8a2c-137">To change the text to a table</span></span>  
  
1.  <span data-ttu-id="f8a2c-138">Utilisez la méthode `ConvertToTable` pour inclure le texte dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-138">Use the `ConvertToTable` method to enclose the text in a table.</span></span> <span data-ttu-id="f8a2c-139">La méthode comprend seize paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-139">The method has sixteen optional parameters.</span></span> <span data-ttu-id="f8a2c-140">IntelliSense place les paramètres facultatifs entre crochets, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-140">IntelliSense encloses optional parameters in brackets, as shown in the following illustration.</span></span>  
  
     <span data-ttu-id="f8a2c-141">![Liste des paramètres de la méthode ConvertToTable.](../../../csharp/programming-guide/classes-and-structs/media/convert_tableparameters.png "Convert_TableParameters")</span><span class="sxs-lookup"><span data-stu-id="f8a2c-141">![List of parameters for ConvertToTable method.](../../../csharp/programming-guide/classes-and-structs/media/convert_tableparameters.png "Convert_TableParameters")</span></span>  
<span data-ttu-id="f8a2c-142">Paramètres ConvertToTable</span><span class="sxs-lookup"><span data-stu-id="f8a2c-142">ConvertToTable parameters</span></span>  
  
     <span data-ttu-id="f8a2c-143">Les arguments nommés et facultatifs permettent de spécifier des valeurs uniquement pour les paramètres que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-143">Named and optional arguments enable you to specify values for only the parameters that you want to change.</span></span> <span data-ttu-id="f8a2c-144">Ajoutez le code suivant à la fin de la méthode `DisplayInWord` pour créer un tableau simple.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-144">Add the following code to the end of method `DisplayInWord` to create a simple table.</span></span> <span data-ttu-id="f8a2c-145">L’argument spécifie que les virgules présentes dans le texte de la chaîne comprise dans `range` séparent les cellules du tableau.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-145">The argument specifies that the commas in the text string in `range` separate the cells of the table.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#9](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_5.cs)]  
  
     <span data-ttu-id="f8a2c-146">Dans les versions antérieures du langage C#, l’appel de `ConvertToTable` nécessite un argument de référence pour chaque paramètre, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-146">In earlier versions of C#, the call to `ConvertToTable` requires a reference argument for each parameter, as shown in the following code.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_6.cs)]  
  
2.  <span data-ttu-id="f8a2c-147">Appuyez sur CTRL+F5 pour exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-147">Press CTRL+F5 to run the project.</span></span>  
  
### <a name="to-experiment-with-other-parameters"></a><span data-ttu-id="f8a2c-148">Pour tester d’autres paramètres</span><span class="sxs-lookup"><span data-stu-id="f8a2c-148">To experiment with other parameters</span></span>  
  
1.  <span data-ttu-id="f8a2c-149">Pour modifier le tableau de sorte qu’il comporte une colonne et trois lignes, remplacez la dernière ligne de `DisplayInWord` par l’instruction suivante, puis appuyez sur CTRL+F5.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-149">To change the table so that it has one column and three rows, replace the last line in `DisplayInWord` with the following statement and then type CTRL+F5.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_7.cs)]  
  
2.  <span data-ttu-id="f8a2c-150">Pour spécifier un format prédéfini pour le tableau, remplacez la dernière ligne de `DisplayInWord` par l’instruction suivante, puis appuyez sur CTRL + F5.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-150">To specify a predefined format for the table, replace the last line in `DisplayInWord` with the following statement and then type CTRL+F5.</span></span> <span data-ttu-id="f8a2c-151">Le format peut être n’importe quelle constante [WdTableFormat](https://msdn.microsoft.com/library/microsoft.office.interop.word.wdtableformat.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8a2c-151">The format can be any of the [WdTableFormat](https://msdn.microsoft.com/library/microsoft.office.interop.word.wdtableformat.aspx) constants.</span></span>  
  
     [!code-csharp[csProgGuideNamedAndOptional#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_8.cs)]  
  
## <a name="example"></a><span data-ttu-id="f8a2c-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8a2c-152">Example</span></span>  
 <span data-ttu-id="f8a2c-153">Le code suivant contient l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="f8a2c-153">The following code includes the full example.</span></span>  
  
 [!code-csharp[csProgGuideNamedAndOptional#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-named-and-optional-arguments-in-office-programming_9.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f8a2c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8a2c-154">See Also</span></span>  
 [<span data-ttu-id="f8a2c-155">Arguments nommés et facultatifs</span><span class="sxs-lookup"><span data-stu-id="f8a2c-155">Named and Optional Arguments</span></span>](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)
