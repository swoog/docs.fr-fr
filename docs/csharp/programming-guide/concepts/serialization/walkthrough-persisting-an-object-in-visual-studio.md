---
title: 'Procédure pas à pas : persistance d’un objet avec C#'
ms.date: 04/26/2018
ms.openlocfilehash: c3cff57f008eb524c2d2bec406431e4c41dca617
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44262098"
---
# <a name="walkthrough-persisting-an-object-using-c"></a><span data-ttu-id="f473b-102">Procédure pas à pas : persistance d’un objet avec C#</span><span class="sxs-lookup"><span data-stu-id="f473b-102">Walkthrough: persisting an object using C#</span></span> #

<span data-ttu-id="f473b-103">Vous pouvez utiliser la sérialisation pour rendre les données d’un objet persistantes entre les instances, ce qui vous permet de stocker des valeurs et de les récupérer lors de la prochaine instanciation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f473b-103">You can use serialization to persist an object's data between instances, which enables you to store values and retrieve them the next time that the object is instantiated.</span></span>

<span data-ttu-id="f473b-104">Dans cette procédure pas à pas, vous créez un objet `Loan` de base et vous stockez ses données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f473b-104">In this walkthrough, you will create a basic `Loan` object and persist its data to a file.</span></span> <span data-ttu-id="f473b-105">Vous récupérerez ensuite les données du fichier lors de la recréation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f473b-105">You will then retrieve the data from the file when you re-create the object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f473b-106">Cet exemple crée un fichier s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="f473b-106">This example creates a new file if the file does not already exist.</span></span> <span data-ttu-id="f473b-107">Si une application doit créer un fichier, elle doit disposer de l’autorisation `Create` pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="f473b-107">If an application must create a file, that application must have `Create` permission for the folder.</span></span> <span data-ttu-id="f473b-108">Les autorisations sont définies à l’aide de listes de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="f473b-108">Permissions are set by using access control lists.</span></span> <span data-ttu-id="f473b-109">Si le fichier existe déjà, l’application a uniquement besoin de l’autorisation `Write`, ce qui représente une autorisation inférieure.</span><span class="sxs-lookup"><span data-stu-id="f473b-109">If the file already exists, the application needs only `Write` permission, a lesser permission.</span></span> <span data-ttu-id="f473b-110">Quand c’est possible, il est plus sûr de créer le fichier lors du déploiement et d’accorder l’autorisation `Read` sur un seul fichier (au lieu d’accorder l’autorisation Créer pour un dossier).</span><span class="sxs-lookup"><span data-stu-id="f473b-110">Where possible, it's more secure to create the file during deployment and only grant `Read` permissions to a single file (instead of Create permissions for a folder).</span></span> <span data-ttu-id="f473b-111">Par ailleurs, il est plus sûr d’écrire les données dans des dossiers utilisateur que dans le dossier racine ou le dossier Program Files.</span><span class="sxs-lookup"><span data-stu-id="f473b-111">Also, it's more secure to write data to user folders than to the root folder or the Program Files folder.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f473b-112">Cet exemple stocke les données dans un fichier au format binaire.</span><span class="sxs-lookup"><span data-stu-id="f473b-112">This example stores data in a binary format file.</span></span> <span data-ttu-id="f473b-113">Ces formats ne doivent pas être utilisés pour des données sensibles, telles que les mots de passe ou les informations relatives à la carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="f473b-113">These formats should not be used for sensitive data, such as passwords or credit-card information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f473b-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f473b-114">Prerequisites</span></span>

* <span data-ttu-id="f473b-115">Pour générer et exécuter, installez le [SDK .NET Core](https://www.microsoft.com/net/core).</span><span class="sxs-lookup"><span data-stu-id="f473b-115">To build and run, install the [.NET Core SDK](https://www.microsoft.com/net/core).</span></span>

* <span data-ttu-id="f473b-116">Installez votre éditeur de code favori, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="f473b-116">Install your favorite code editor, if you haven't already.</span></span>

> [!TIP]
> <span data-ttu-id="f473b-117">Vous avez besoin d’installer un éditeur de code ?</span><span class="sxs-lookup"><span data-stu-id="f473b-117">Need to install a code editor?</span></span> <span data-ttu-id="f473b-118">Essayez [Visual Studio](https://visualstudio.com/downloads) !</span><span class="sxs-lookup"><span data-stu-id="f473b-118">Try [Visual Studio](https://visualstudio.com/downloads)!</span></span>

<span data-ttu-id="f473b-119">Vous pouvez examiner l’exemple de code en ligne [sur le référentiel GitHub des exemples .NET](https://github.com/dotnet/samples/tree/master/csharp/serialization).</span><span class="sxs-lookup"><span data-stu-id="f473b-119">You can examine the sample code online [at the .NET samples GitHub repository](https://github.com/dotnet/samples/tree/master/csharp/serialization).</span></span>

## <a name="creating-the-loan-object"></a><span data-ttu-id="f473b-120">Création de l’objet loan</span><span class="sxs-lookup"><span data-stu-id="f473b-120">Creating the loan object</span></span>

<span data-ttu-id="f473b-121">La première étape consiste à créer une classe `Loan` et une application console qui utilise cette classe :</span><span class="sxs-lookup"><span data-stu-id="f473b-121">The first step is to create a `Loan` class and a console application that uses the class:</span></span>

1. <span data-ttu-id="f473b-122">Créez une application.</span><span class="sxs-lookup"><span data-stu-id="f473b-122">Create a new application.</span></span> <span data-ttu-id="f473b-123">Tapez `dotnet new console -o serialization` pour créer une application console dans un sous-répertoire nommé `serialization`.</span><span class="sxs-lookup"><span data-stu-id="f473b-123">Type `dotnet new console -o serialization` to create a new console application in a subdirectory named `serialization`.</span></span>
1. <span data-ttu-id="f473b-124">Ouvrez l’application dans votre éditeur, et ajoutez une nouvelle classe nommée `Loan.cs`.</span><span class="sxs-lookup"><span data-stu-id="f473b-124">Open the application in your editor, and add a new class named `Loan.cs`.</span></span>
1. <span data-ttu-id="f473b-125">Ajoutez le code suivant à la classe `Loan` :</span><span class="sxs-lookup"><span data-stu-id="f473b-125">Add the following code to your `Loan` class:</span></span>

[!code-csharp[Loan class definition](../../../../../samples/csharp/serialization/Loan.cs#1)]

<span data-ttu-id="f473b-126">Vous devez également créer une application simple qui utilise la classe `Loan`.</span><span class="sxs-lookup"><span data-stu-id="f473b-126">You will also have to create an application that uses the `Loan` class.</span></span>

## <a name="serialize-the-loan-object"></a><span data-ttu-id="f473b-127">Sérialiser l’objet loan</span><span class="sxs-lookup"><span data-stu-id="f473b-127">Serialize the loan object</span></span>

1. <span data-ttu-id="f473b-128">Ouvrez `Program.cs`.</span><span class="sxs-lookup"><span data-stu-id="f473b-128">Open `Program.cs`.</span></span> <span data-ttu-id="f473b-129">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f473b-129">Add the following code:</span></span>

[!code-csharp[Create a loan object](../../../../../samples/csharp/serialization/Program.cs#1)]

<span data-ttu-id="f473b-130">Ajoutez un gestionnaire d’événements pour l’événement `PropertyChanged`, ainsi que quelques lignes pour modifier l’objet `Loan` et afficher les modifications.</span><span class="sxs-lookup"><span data-stu-id="f473b-130">Add an event handler for the `PropertyChanged` event, and a few lines to modify the `Loan` object and display the changes.</span></span> <span data-ttu-id="f473b-131">Vous pouvez voir les ajouts dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f473b-131">You can see the additions in the following code:</span></span>

[!code-csharp[Listening for the PropertyChanged event](../../../../../samples/csharp/serialization/Program.cs#2)]

<span data-ttu-id="f473b-132">À ce stade, vous pouvez exécuter le code et voir la sortie actuelle :</span><span class="sxs-lookup"><span data-stu-id="f473b-132">At this point, you can run the code, and see the current output:</span></span>

```console
New customer value: Henry Clay
7.5
7.1
```

<span data-ttu-id="f473b-133">L’exécution de cette application à plusieurs reprises écrit toujours les mêmes valeurs.</span><span class="sxs-lookup"><span data-stu-id="f473b-133">Running this application repeatedly always writes the same values.</span></span> <span data-ttu-id="f473b-134">Un nouvel objet Loan est créé chaque fois que vous exécutez le programme.</span><span class="sxs-lookup"><span data-stu-id="f473b-134">A new Loan object is created every time you run the program.</span></span> <span data-ttu-id="f473b-135">Dans la réalité, les taux d’intérêt changent régulièrement, mais pas nécessairement chaque fois que l’application est exécutée.</span><span class="sxs-lookup"><span data-stu-id="f473b-135">In the real world, interest rates change periodically, but not necessarily every time that the application is run.</span></span> <span data-ttu-id="f473b-136">Un code de sérialisation signifie que vous conservez le taux d’intérêt le plus récent entre les instances de l’application.</span><span class="sxs-lookup"><span data-stu-id="f473b-136">Serialization code means you preserve the most recent interest rate between instances of the application.</span></span> <span data-ttu-id="f473b-137">C’est ce que vous ferez à l’étape suivante, en ajoutant la sérialisation à la classe Loan.</span><span class="sxs-lookup"><span data-stu-id="f473b-137">In the next step, you will do just that by adding serialization to the Loan class.</span></span>

## <a name="using-serialization-to-persist-the-object"></a><span data-ttu-id="f473b-138">Utilisation de la sérialisation pour rendre l’objet persistant</span><span class="sxs-lookup"><span data-stu-id="f473b-138">Using Serialization to Persist the Object</span></span>

<span data-ttu-id="f473b-139">Pour rendre les valeurs de la classe Loan persistantes, vous devez d’abord marquer la classe avec l’attribut `Serializable`.</span><span class="sxs-lookup"><span data-stu-id="f473b-139">In order to persist the values for the Loan class, you must first mark the class with the `Serializable` attribute.</span></span> <span data-ttu-id="f473b-140">Ajoutez le code suivant au-dessus de la déclaration de la classe Loan :</span><span class="sxs-lookup"><span data-stu-id="f473b-140">Add the following code above the Loan class definition:</span></span>

[!code-csharp[Loan class definition](../../../../../samples/csharp/serialization/Loan.cs#2)]

<span data-ttu-id="f473b-141"><xref:System.SerializableAttribute> indique au compilateur que tout ce que contient la classe peut être stocké dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f473b-141">The <xref:System.SerializableAttribute> tells the compiler that everything in the class can be persisted to a file.</span></span> <span data-ttu-id="f473b-142">Étant donné que l’événement `PropertyChanged` ne représente pas une partie du graphe d’objets qui doit être stocké, il ne doit pas être sérialisé.</span><span class="sxs-lookup"><span data-stu-id="f473b-142">Because the `PropertyChanged` event does not represent part of the object graph that should be stored, it should not be serialized.</span></span> <span data-ttu-id="f473b-143">Procéder ainsi sérialiserait tous les objets qui sont attachés à cet événement.</span><span class="sxs-lookup"><span data-stu-id="f473b-143">Doing so would serialize all objects that are attached to that event.</span></span> <span data-ttu-id="f473b-144">Vous pouvez ajouter <xref:System.NonSerializedAttribute> à la déclaration du champ pour le gestionnaire d’événements `PropertyChanged`.</span><span class="sxs-lookup"><span data-stu-id="f473b-144">You can add the <xref:System.NonSerializedAttribute> to the field declaration for the `PropertyChanged` event handler.</span></span>

[!code-csharp[Disable serialization for the event handler](../../../../../samples/csharp/serialization/Loan.cs#3)]

<span data-ttu-id="f473b-145">À compter de C# 7.3, vous pouvez attacher des attributs au champ de stockage d’une propriété implémentée automatiquement en utilisant la valeur cible `field`.</span><span class="sxs-lookup"><span data-stu-id="f473b-145">Beginning with C# 7.3, you can attach attributes to the backing field of an auto-implemented property using the `field` target value.</span></span> <span data-ttu-id="f473b-146">Le code suivant ajoute une propriété `TimeLastLoaded` et la marque comme non sérialisable :</span><span class="sxs-lookup"><span data-stu-id="f473b-146">The following code adds a `TimeLastLoaded` property and marks it as not serializable:</span></span>

[!code-csharp[Disable serialization for an auto-implemented property](../../../../../samples/csharp/serialization/Loan.cs#4)]

<span data-ttu-id="f473b-147">L’étape suivante consiste à ajouter le code de sérialisation à l’application LoanApp.</span><span class="sxs-lookup"><span data-stu-id="f473b-147">The next step is to add the serialization code to the LoanApp application.</span></span> <span data-ttu-id="f473b-148">Pour sérialiser la classe et l’écrire dans un fichier, vous utilisez les espaces de noms <xref:System.IO> et <xref:System.Runtime.Serialization.Formatters.Binary>.</span><span class="sxs-lookup"><span data-stu-id="f473b-148">In order to serialize the class and write it to a file, you use the <xref:System.IO> and <xref:System.Runtime.Serialization.Formatters.Binary> namespaces.</span></span> <span data-ttu-id="f473b-149">Pour éviter de taper les noms qualifiés complets, vous pouvez ajouter des références aux espaces de noms nécessaires, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f473b-149">To avoid typing the fully qualified names, you can add references to the necessary namespaces as shown in the following code:</span></span>

[!code-csharp[Adding namespaces for serialization](../../../../../samples/csharp/serialization/Program.cs#3)]

<span data-ttu-id="f473b-150">L’étape suivante consiste à ajouter le code permettant de désérialiser l’objet à partir du fichier lors de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f473b-150">The next step is to add code to deserialize the object from the file when the object is created.</span></span> <span data-ttu-id="f473b-151">Ajoutez une constante à la classe pour le nom de fichier des données sérialisées, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f473b-151">Add a constant to the class for the serialized data's file name as shown in the following code:</span></span>

[!code-csharp[Define the name of the saved file](../../../../../samples/csharp/serialization/Program.cs#4)]

<span data-ttu-id="f473b-152">Ensuite, ajoutez le code suivant après la ligne qui crée l’objet `TestLoan` :</span><span class="sxs-lookup"><span data-stu-id="f473b-152">Next, add the following code after the line that creates the `TestLoan` object:</span></span>

[!code-csharp[Read from a file if it exists](../../../../../samples/csharp/serialization/Program.cs#5)]

<span data-ttu-id="f473b-153">Vous devez d’abord vérifier que le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="f473b-153">You first must check that the file exists.</span></span> <span data-ttu-id="f473b-154">S’il existe, créez une classe <xref:System.IO.Stream> pour lire le fichier binaire et une classe <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> pour convertir le fichier.</span><span class="sxs-lookup"><span data-stu-id="f473b-154">If it exists, create a <xref:System.IO.Stream> class to read the binary file and a <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> class to translate the file.</span></span> <span data-ttu-id="f473b-155">Vous devez également convertir le type de flux en type d’objet Loan.</span><span class="sxs-lookup"><span data-stu-id="f473b-155">You also need to convert from the stream type to the Loan object type.</span></span>

<span data-ttu-id="f473b-156">Vous devez ensuite ajouter du code pour sérialiser la classe dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f473b-156">Next you must add code to serialize the class to a file.</span></span> <span data-ttu-id="f473b-157">Ajoutez le code suivant après le code existant de la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="f473b-157">Add the following code after the existing code in the `Main` method:</span></span>

[!code-csharp[Save the existing Loan object](../../../../../samples/csharp/serialization/Program.cs#6)]

<span data-ttu-id="f473b-158">À ce stade, vous pouvez de nouveau générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="f473b-158">At this point, you can again build and run the application.</span></span> <span data-ttu-id="f473b-159">La première fois qu’elle s’exécute, notez que le taux d’intérêt commence à 7,5, puis qu’il passe à 7,1.</span><span class="sxs-lookup"><span data-stu-id="f473b-159">The first time it runs, notice that the interest rates starts at 7.5, and then changes to 7.1.</span></span> <span data-ttu-id="f473b-160">Fermez l’application et exécutez-la de nouveau.</span><span class="sxs-lookup"><span data-stu-id="f473b-160">Close the application and then run it again.</span></span> <span data-ttu-id="f473b-161">L’application indique maintenant qu’elle a lu le fichier enregistré, et le taux d’intérêt est de 7,1 même avant le code qui le change.</span><span class="sxs-lookup"><span data-stu-id="f473b-161">Now, the application prints the message that it has read the saved file, and the interest rate is 7.1 even before the code that changes it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f473b-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f473b-162">See Also</span></span>

- [<span data-ttu-id="f473b-163">Sérialisation (C#)</span><span class="sxs-lookup"><span data-stu-id="f473b-163">Serialization (C#)</span></span>](index.md)  
- [<span data-ttu-id="f473b-164">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f473b-164">C# Programming Guide</span></span>](../..//index.md)  
