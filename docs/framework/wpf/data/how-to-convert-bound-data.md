---
title: 'Procédure : Convertir des données liées'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- converting [WPF], bound data
- data binding [WPF], converting bound data
- binding data [WPF], converting bound data
ms.assetid: b00aaa19-c6df-4c3b-a9fd-88a0b488df2b
ms.openlocfilehash: 40699bec1c6cd775f7f8495b7a49eda15fb2ed83
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093798"
---
# <a name="how-to-convert-bound-data"></a><span data-ttu-id="7764b-102">Procédure : Convertir des données liées</span><span class="sxs-lookup"><span data-stu-id="7764b-102">How to: Convert Bound Data</span></span>
<span data-ttu-id="7764b-103">Cet exemple montre comment appliquer la conversion de données qui sont utilisées dans les liaisons.</span><span class="sxs-lookup"><span data-stu-id="7764b-103">This example shows how to apply conversion to data that is used in bindings.</span></span>  
  
 <span data-ttu-id="7764b-104">Pour convertir des données pendant la liaison, vous devez créer une classe qui implémente le <xref:System.Windows.Data.IValueConverter> interface, ce qui inclut le <xref:System.Windows.Data.IValueConverter.Convert%2A> et <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> méthodes.</span><span class="sxs-lookup"><span data-stu-id="7764b-104">To convert data during binding, you must create a class that implements the <xref:System.Windows.Data.IValueConverter> interface, which includes the <xref:System.Windows.Data.IValueConverter.Convert%2A> and <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> methods.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7764b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="7764b-105">Example</span></span>  
 <span data-ttu-id="7764b-106">L’exemple suivant montre l’implémentation d’un convertisseur de date qui convertit la valeur de date passée pour qu’il affiche uniquement l’année, mois et jour.</span><span class="sxs-lookup"><span data-stu-id="7764b-106">The following example shows the implementation of a date converter that converts the date value passed in so that it only shows the year, the month, and the day.</span></span> <span data-ttu-id="7764b-107">Lorsque vous implémentez le <xref:System.Windows.Data.IValueConverter> interface, il est conseillé pour décorer l’implémentation avec un <xref:System.Windows.Data.ValueConversionAttribute> attribut pour indiquer au développement des outils les types de données impliqués dans la conversion, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7764b-107">When implementing the <xref:System.Windows.Data.IValueConverter> interface, it is a good practice to decorate the implementation with a <xref:System.Windows.Data.ValueConversionAttribute> attribute to indicate to development tools the data types involved in the conversion, as in the following example:</span></span>  
  
 [!code-csharp[DataBindingLab#18](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DateConverter.cs#18)]
 [!code-vb[DataBindingLab#18](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/DateConverter.vb#18)]  
  
 <span data-ttu-id="7764b-108">Une fois que vous avez créé un convertisseur, vous pouvez l’ajouter en tant que ressource dans votre [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier.</span><span class="sxs-lookup"><span data-stu-id="7764b-108">Once you have created a converter, you can add it as a resource in your [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file.</span></span> <span data-ttu-id="7764b-109">Dans l’exemple suivant, *src* est mappé à l’espace de noms dans lequel *convertisseur de date* est défini.</span><span class="sxs-lookup"><span data-stu-id="7764b-109">In the following example, *src* maps to the namespace in which *DateConverter* is defined.</span></span>  
  
 [!code-xaml[DataBindingLab#15](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#15)]  
  
 <span data-ttu-id="7764b-110">Enfin, vous pouvez utiliser le convertisseur dans votre liaison à l’aide de la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="7764b-110">Finally, you can use the converter in your binding using the following syntax.</span></span> <span data-ttu-id="7764b-111">Dans l’exemple suivant, le contenu textuel de la <xref:System.Windows.Controls.TextBlock> est lié à *StartDate*, qui est une propriété de source de données externe.</span><span class="sxs-lookup"><span data-stu-id="7764b-111">In the following example, the text content of the <xref:System.Windows.Controls.TextBlock> is bound to *StartDate*, which is a property of an external data source.</span></span>  
  
 [!code-xaml[DataBindingLab#17](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#17)]  
  
 <span data-ttu-id="7764b-112">Les ressources de style référencées dans l’exemple ci-dessus sont définies dans une section de ressources ne pas présentée dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7764b-112">The style resources referenced in the above example are defined in a resource section not shown in this topic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7764b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7764b-113">See also</span></span>

- [<span data-ttu-id="7764b-114">Implémenter la validation de la liaison</span><span class="sxs-lookup"><span data-stu-id="7764b-114">Implement Binding Validation</span></span>](how-to-implement-binding-validation.md)
- [<span data-ttu-id="7764b-115">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="7764b-115">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="7764b-116">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="7764b-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
