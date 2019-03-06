---
title: 'Procédure : Utiliser un dictionnaire de ressources de portée application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dictionaries [WPF], resource
- resource dictionaries [WPF], application-scope
- application-scope resource dictionaries
ms.assetid: 53857682-bd2c-4f2c-8f25-1307d0b451a2
ms.openlocfilehash: a2453ae7fad56205ae06835d8710ca126bba17c7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57369732"
---
# <a name="how-to-use-an-application-scope-resource-dictionary"></a><span data-ttu-id="37a01-102">Procédure : Utiliser un dictionnaire de ressources de portée application</span><span class="sxs-lookup"><span data-stu-id="37a01-102">How to: Use an Application-Scope Resource Dictionary</span></span>
<span data-ttu-id="37a01-103">Cet exemple montre comment définir et utiliser un dictionnaire de ressources personnalisé de portée application.</span><span class="sxs-lookup"><span data-stu-id="37a01-103">This example shows how to define and use an application-scope custom resource dictionary.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37a01-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="37a01-104">Example</span></span>  
 <span data-ttu-id="37a01-105"><xref:System.Windows.Application> expose un magasin de portée application pour les ressources partagées : <xref:System.Windows.Application.Resources%2A>.</span><span class="sxs-lookup"><span data-stu-id="37a01-105"><xref:System.Windows.Application> exposes an application-scope store for shared resources: <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="37a01-106">Par défaut, le <xref:System.Windows.Application.Resources%2A> propriété est initialisée avec une instance de la <xref:System.Windows.ResourceDictionary> type.</span><span class="sxs-lookup"><span data-stu-id="37a01-106">By default, the <xref:System.Windows.Application.Resources%2A> property is initialized with an instance of the <xref:System.Windows.ResourceDictionary> type.</span></span> <span data-ttu-id="37a01-107">Vous utilisez cette instance lorsque vous obtenez et définissez les propriétés de portée application à l’aide de <xref:System.Windows.Application.Resources%2A>.</span><span class="sxs-lookup"><span data-stu-id="37a01-107">You use this instance when you get and set application-scope properties using <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="37a01-108">Pour plus d'informations, voir [Procédure : Obtenir et définir une ressource de portée Application](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="37a01-108">For more information, see [How to: Get and Set an Application-Scope Resource](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).</span></span>
  
 <span data-ttu-id="37a01-109">Si vous disposez de plusieurs ressources que vous définissez à l’aide de <xref:System.Windows.Application.Resources%2A>, vous pouvez utiliser un dictionnaire de ressources personnalisé pour stocker ces ressources et définir <xref:System.Windows.Application.Resources%2A> avec lui à la place.</span><span class="sxs-lookup"><span data-stu-id="37a01-109">If you have multiple resources that you set using <xref:System.Windows.Application.Resources%2A>, you can instead use a custom resource dictionary to store those resources and set <xref:System.Windows.Application.Resources%2A> with it instead.</span></span> <span data-ttu-id="37a01-110">L’exemple suivant montre comment déclarer un dictionnaire de ressources personnalisé à l’aide de XAML.</span><span class="sxs-lookup"><span data-stu-id="37a01-110">The following shows how you declare a custom resource dictionary using XAML.</span></span>
  
 [!code-xaml[HOWTOResourceDictionaries#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MyResourceDictionary.xaml#1)]  
  
 <span data-ttu-id="37a01-111">Le remplacement de dictionnaires de ressources entiers à l’aide de <xref:System.Windows.Application.Resources%2A> vous permet de prendre en charge des thèmes de portée application, où chaque thème est encapsulé par un dictionnaire de ressources unique.</span><span class="sxs-lookup"><span data-stu-id="37a01-111">Swapping entire resource dictionaries using <xref:System.Windows.Application.Resources%2A> allows you to support application-scope themes, where each theme is encapsulated by a single resource dictionary.</span></span> <span data-ttu-id="37a01-112">L'exemple suivant montre comment définir <xref:System.Windows.ResourceDictionary>.</span><span class="sxs-lookup"><span data-stu-id="37a01-112">The following example shows how to set the <xref:System.Windows.ResourceDictionary>.</span></span>  
  
 [!code-xaml[HOWTOResourceDictionaries#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/App.xaml#2)]  
  
 <span data-ttu-id="37a01-113">L’exemple suivant montre comment vous pouvez obtenir des ressources de portée application à partir du dictionnaire de ressources exposé par <xref:System.Windows.Application.Resources%2A> dans XAML.</span><span class="sxs-lookup"><span data-stu-id="37a01-113">The following shows how you can get application-scope resources from the resource dictionary exposed by <xref:System.Windows.Application.Resources%2A> in XAML.</span></span>  
  
 [!code-xaml[HOWTOResourceDictionaries#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml#4)]  
  
 <span data-ttu-id="37a01-114">Voici également comment obtenir les ressources dans le code.</span><span class="sxs-lookup"><span data-stu-id="37a01-114">The following shows how you can also get the resources in code.</span></span>  
  
 [!code-csharp[HOWTOResourceDictionaries#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml.cs#3)]
 [!code-vb[HOWTOResourceDictionaries#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToResourceDictionaries/VB/MainWindow.xaml.vb#3)]  
  
 <span data-ttu-id="37a01-115">Il existe deux considérations à prendre lorsque vous utilisez <xref:System.Windows.Application.Resources%2A>.</span><span class="sxs-lookup"><span data-stu-id="37a01-115">There are two considerations to make when using <xref:System.Windows.Application.Resources%2A>.</span></span> <span data-ttu-id="37a01-116">Tout d’abord, le dictionnaire *clé* est un objet, vous devez donc utiliser exactement la même instance d’objet lors du paramétrage et l’obtention d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="37a01-116">First, the dictionary *key* is an object, so you must use exactly the same object instance when both setting and getting a property value.</span></span> <span data-ttu-id="37a01-117">(Notez qu’en cas d’utilisation d’une chaîne, la clé respecte la casse.) Ensuite, le dictionnaire *valeur* est un objet, donc vous devrez convertir la valeur vers le type souhaité lors de l’obtention d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="37a01-117">(Note that the key is case-sensitive when using a string.) Second, the dictionary *value* is an object, so you will have to convert the value to the desired type when getting a property value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37a01-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37a01-118">See also</span></span>
- <xref:System.Windows.ResourceDictionary>
- <xref:System.Windows.Application.Resources%2A>
- [<span data-ttu-id="37a01-119">Ressources XAML</span><span class="sxs-lookup"><span data-stu-id="37a01-119">XAML Resources</span></span>](../advanced/xaml-resources.md)
- [<span data-ttu-id="37a01-120">Dictionnaires de ressources fusionnés</span><span class="sxs-lookup"><span data-stu-id="37a01-120">Merged Resource Dictionaries</span></span>](../advanced/merged-resource-dictionaries.md)
