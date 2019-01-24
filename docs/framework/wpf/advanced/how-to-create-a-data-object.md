---
title: 'Procédure : Créer un objet de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataObject class [WPF], creating
- data objects [WPF], creating
- drag-and-drop [WPF], creating data objects
ms.assetid: 022fa142-717d-4fea-a53c-3b52e9d91aff
ms.openlocfilehash: edc301cb896dc8e704a0e17e8e22366d82cc0c17
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687191"
---
# <a name="how-to-create-a-data-object"></a><span data-ttu-id="5f6a6-102">Procédure : Créer un objet de données</span><span class="sxs-lookup"><span data-stu-id="5f6a6-102">How to: Create a Data Object</span></span>
<span data-ttu-id="5f6a6-103">Les exemples suivants montrent différentes manières de créer un objet de données à l’aide des constructeurs fournis par le <xref:System.Windows.DataObject> classe.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-103">The following examples show various ways to create a data object using the constructors provided by the <xref:System.Windows.DataObject> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f6a6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f6a6-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="5f6a6-105">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-105">Description</span></span>  
 <span data-ttu-id="5f6a6-106">L’exemple de code suivant crée un nouvel objet de données et utilise l’un des constructeurs surchargés (<xref:System.Windows.DataObject.%23ctor%28System.Object%29>) pour initialiser l’objet de données avec une chaîne.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-106">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.Object%29>) to initialize the data object with a string.</span></span>  <span data-ttu-id="5f6a6-107">Dans ce cas, un format de données approprié est déterminé automatiquement selon le type des données stockées, et la conversion automatique des données stockées est autorisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-107">In this case, an appropriate data format is determined automatically according to the stored data's type, and auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-108">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-108">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_simple)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_simple)]  
  
### <a name="description"></a><span data-ttu-id="5f6a6-109">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-109">Description</span></span>  
 <span data-ttu-id="5f6a6-110">L’exemple de code suivant est une version condensée de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-110">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-111">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple_Condensed](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_simple_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Simple_Condensed](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_simple_condensed)]  
  
## <a name="example"></a><span data-ttu-id="5f6a6-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f6a6-112">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="5f6a6-113">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-113">Description</span></span>  
 <span data-ttu-id="5f6a6-114">L’exemple de code suivant crée un nouvel objet de données et utilise l’un des constructeurs surchargés (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%29>) pour initialiser l’objet de données avec une chaîne et un format de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-114">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%29>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="5f6a6-115">Dans ce cas, le format de données est spécifié par une chaîne ; le <xref:System.Windows.DataFormats> classe fournit un ensemble de chaînes de type prédéfini.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-115">In this case the data format is specified by a string; the <xref:System.Windows.DataFormats> class provides a set of pre-defined type strings.</span></span> <span data-ttu-id="5f6a6-116">La conversion automatique des données stockées est autorisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-116">Auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-117">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-117">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_typestring)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_typestring)]  
  
### <a name="description"></a><span data-ttu-id="5f6a6-118">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-118">Description</span></span>  
 <span data-ttu-id="5f6a6-119">L’exemple de code suivant est une version condensée de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-119">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-120">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-120">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString_Condensed](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_typestring_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_TypeString_Condensed](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_typestring_condensed)]  
  
## <a name="example"></a><span data-ttu-id="5f6a6-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f6a6-121">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="5f6a6-122">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-122">Description</span></span>  
 <span data-ttu-id="5f6a6-123">L’exemple de code suivant crée un nouvel objet de données et utilise l’un des constructeurs surchargés (<xref:System.Windows.DataObject.%23ctor%2A>) pour initialiser l’objet de données avec une chaîne et un format de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-123">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%2A>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="5f6a6-124">Dans ce cas, le format de données est spécifié par un <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-124">In this case the data format is specified by a <xref:System.Type> parameter.</span></span>  <span data-ttu-id="5f6a6-125">La conversion automatique des données stockées est autorisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-125">Auto-converting of the stored data is allowed by default.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-126">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-126">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_type)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_type)]  
  
### <a name="description"></a><span data-ttu-id="5f6a6-127">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-127">Description</span></span>  
 <span data-ttu-id="5f6a6-128">L’exemple de code suivant est une version condensée de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-128">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-129">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-129">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type_Condensed](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_type_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_Type_Condensed](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_type_condensed)]  
  
## <a name="example"></a><span data-ttu-id="5f6a6-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f6a6-130">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="5f6a6-131">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-131">Description</span></span>  
 <span data-ttu-id="5f6a6-132">L’exemple de code suivant crée un nouvel objet de données et utilise l’un des constructeurs surchargés (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%2CSystem.Boolean%29>) pour initialiser l’objet de données avec une chaîne et un format de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-132">The following example code creates a new data object and uses one of the overloaded constructors (<xref:System.Windows.DataObject.%23ctor%28System.String%2CSystem.Object%2CSystem.Boolean%29>) to initialize the data object with a string and a specified data format.</span></span>  <span data-ttu-id="5f6a6-133">Dans ce cas, le format de données est spécifié par une chaîne ; le <xref:System.Windows.DataFormats> classe fournit un ensemble de chaînes de type prédéfini.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-133">In this case the data format is specified by a string; the <xref:System.Windows.DataFormats> class provides a set of pre-defined type strings.</span></span> <span data-ttu-id="5f6a6-134">Cette surcharge de constructeur particulière permet à l’appelant de spécifier si la conversion automatique est autorisée.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-134">This particular constructor overload enables the caller to specify whether auto-converting is allowed.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-135">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-135">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_autoconvert)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_autoconvert)]  
  
### <a name="description"></a><span data-ttu-id="5f6a6-136">Description</span><span class="sxs-lookup"><span data-stu-id="5f6a6-136">Description</span></span>  
 <span data-ttu-id="5f6a6-137">L’exemple de code suivant est une version condensée de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5f6a6-137">The following example code is a condensed version of the code shown above.</span></span>  
  
### <a name="code"></a><span data-ttu-id="5f6a6-138">Code</span><span class="sxs-lookup"><span data-stu-id="5f6a6-138">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert_Condensed](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_createdataobject_autoconvert_condensed)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_CreateDataObject_AutoConvert_Condensed](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_createdataobject_autoconvert_condensed)]  
  
## <a name="see-also"></a><span data-ttu-id="5f6a6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f6a6-139">See also</span></span>
- <xref:System.Windows.IDataObject>
