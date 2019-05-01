---
title: 'Procédure : utiliser le modèle de ligne pour personnaliser des lignes dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- DataGridView control [Windows Forms], customizing rows
ms.assetid: 6db61607-7e57-4a84-8d63-9d6a7ed7f9ff
ms.openlocfilehash: cb3a826262a49a8653e3a344bd126d434f2522dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009186"
---
# <a name="how-to-use-the-row-template-to-customize-rows-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="0f5c4-102">Procédure : utiliser le modèle de ligne pour personnaliser des lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0f5c4-102">How to: Use the Row Template to Customize Rows in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="0f5c4-103">Le <xref:System.Windows.Forms.DataGridView> contrôle utilise le modèle de ligne comme base pour toutes les lignes qu’il ajoute au contrôle via la liaison de données ou lorsque vous appelez le <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A?displayProperty=nameWithType> méthode sans spécifier une ligne existante à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-103">The <xref:System.Windows.Forms.DataGridView> control uses the row template as a basis for all rows that it adds to the control either through data binding or when you call the <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A?displayProperty=nameWithType> method without specifying an existing row to use.</span></span>  
  
 <span data-ttu-id="0f5c4-104">Le modèle de ligne vous donne un plus grand contrôle sur l’apparence et le comportement des lignes que la <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> fournit de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-104">The row template gives you greater control over the appearance and behavior of rows than the <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> property provides.</span></span> <span data-ttu-id="0f5c4-105">Avec le modèle de ligne, vous pouvez définir les <xref:System.Windows.Forms.DataGridViewRow> propriétés, y compris <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A>.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-105">With the row template, you can set any <xref:System.Windows.Forms.DataGridViewRow> properties, including <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A>.</span></span>  
  
 <span data-ttu-id="0f5c4-106">Il existe certaines situations où vous devez utiliser le modèle de ligne pour obtenir un résultat particulier.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-106">There are some situations where you must use the row template to achieve a particular effect.</span></span> <span data-ttu-id="0f5c4-107">Par exemple, les informations de hauteur de ligne ne peut pas être stockées dans un <xref:System.Windows.Forms.DataGridViewCellStyle>, vous devez donc utiliser un modèle de ligne pour modifier la hauteur par défaut utilisée par toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-107">For example, row height information cannot be stored in a <xref:System.Windows.Forms.DataGridViewCellStyle>, so you must use a row template to change the default height used by all rows.</span></span> <span data-ttu-id="0f5c4-108">Le modèle de ligne est également utile lorsque vous créez vos propres classes dérivées de <xref:System.Windows.Forms.DataGridViewRow> et vous souhaitez que votre type personnalisé utilisé lorsque de nouvelles lignes sont ajoutées au contrôle.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-108">The row template is also useful when you create your own classes derived from <xref:System.Windows.Forms.DataGridViewRow> and you want your custom type used when new rows are added to the control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f5c4-109">Le modèle de ligne est utilisé uniquement lorsque des lignes sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-109">The row template is used only when rows are added.</span></span> <span data-ttu-id="0f5c4-110">Vous ne pouvez pas modifier les lignes existantes en modifiant le modèle de ligne.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-110">You cannot change existing rows by changing the row template.</span></span>  
  
### <a name="to-use-the-row-template"></a><span data-ttu-id="0f5c4-111">Pour utiliser le modèle de ligne</span><span class="sxs-lookup"><span data-stu-id="0f5c4-111">To use the row template</span></span>  
  
- <span data-ttu-id="0f5c4-112">Définir des propriétés sur l’objet récupéré à partir de la <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-112">Set properties on the object retrieved from the <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> property.</span></span>  
  
     [!code-cpp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CPP/datagridviewrowtemplate.cpp#1)]
     [!code-csharp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CS/datagridviewrowtemplate.cs#1)]
     [!code-vb[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/VB/datagridviewrowtemplate.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0f5c4-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0f5c4-113">Compiling the Code</span></span>  
 <span data-ttu-id="0f5c4-114">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0f5c4-114">This example requires:</span></span>  
  
- <span data-ttu-id="0f5c4-115">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="0f5c4-115">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="0f5c4-116">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0f5c4-116">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f5c4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f5c4-117">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridViewRow>
- <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType>
- [<span data-ttu-id="0f5c4-118">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0f5c4-118">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="0f5c4-119">Styles de cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0f5c4-119">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)
