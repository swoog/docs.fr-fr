---
title: "Procédure : Ajouter des données personnalisées aux données de l'encre"
ms.date: 03/30/2017
helpviewer_keywords:
- ink data [WPF], adding custom data
- InkCanvas [WPF], displaying
ms.assetid: f02aac6f-3436-4f7c-b6ea-0452cba5332c
ms.openlocfilehash: c524e30943a21426e2e5e8fe6ae009999924fead
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57361666"
---
# <a name="how-to-add-custom-data-to-ink-data"></a><span data-ttu-id="e4c79-102">Procédure : Ajouter des données personnalisées aux données de l'encre</span><span class="sxs-lookup"><span data-stu-id="e4c79-102">How to: Add Custom Data to Ink Data</span></span>
<span data-ttu-id="e4c79-103">Vous pouvez ajouter des données personnalisées à l’encre qui est enregistré lorsque l’encre est enregistré en tant que format de l’encre sérialisée (ISF).</span><span class="sxs-lookup"><span data-stu-id="e4c79-103">You can add custom data to ink that will be saved when the ink is saved as ink serialized format (ISF).</span></span>  <span data-ttu-id="e4c79-104">Vous pouvez enregistrer les données personnalisées pour le <xref:System.Windows.Ink.DrawingAttributes>, le <xref:System.Windows.Ink.StrokeCollection>, ou le <xref:System.Windows.Ink.Stroke>.</span><span class="sxs-lookup"><span data-stu-id="e4c79-104">You can save the custom data to the <xref:System.Windows.Ink.DrawingAttributes>, the <xref:System.Windows.Ink.StrokeCollection>, or the <xref:System.Windows.Ink.Stroke>.</span></span>  <span data-ttu-id="e4c79-105">La possibilité d’enregistrer des données personnalisées sur trois objets vous donne la possibilité de choisir le meilleur emplacement pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="e4c79-105">Being able to save custom data on three objects gives you the ability to decide the best place to save the data.</span></span>  <span data-ttu-id="e4c79-106">Les trois classes utilisent des méthodes similaires pour stocker et accéder aux données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e4c79-106">All three classes use similar methods to store and access custom data.</span></span>  
  
 <span data-ttu-id="e4c79-107">Seuls les types suivants peuvent être enregistrés en tant que données personnalisées :</span><span class="sxs-lookup"><span data-stu-id="e4c79-107">Only the following types can be saved as custom data:</span></span>  
  
-   <xref:System.Boolean>  
  
-   <span data-ttu-id="e4c79-108"><xref:System.Boolean>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-108"><xref:System.Boolean>[]</span></span>  
  
-   <xref:System.Byte>  
  
-   <span data-ttu-id="e4c79-109"><xref:System.Byte>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-109"><xref:System.Byte>[]</span></span>  
  
-   <xref:System.Char>  
  
-   <span data-ttu-id="e4c79-110"><xref:System.Char>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-110"><xref:System.Char>[]</span></span>  
  
-   <xref:System.DateTime>  
  
-   <span data-ttu-id="e4c79-111"><xref:System.DateTime>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-111"><xref:System.DateTime>[]</span></span>  
  
-   <xref:System.Decimal>  
  
-   <span data-ttu-id="e4c79-112"><xref:System.Decimal>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-112"><xref:System.Decimal>[]</span></span>  
  
-   <xref:System.Double>  
  
-   <span data-ttu-id="e4c79-113"><xref:System.Double>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-113"><xref:System.Double>[]</span></span>  
  
-   <xref:System.Int16>  
  
-   <span data-ttu-id="e4c79-114"><xref:System.Int16>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-114"><xref:System.Int16>[]</span></span>  
  
-   <xref:System.Int32>  
  
-   <span data-ttu-id="e4c79-115"><xref:System.Int32>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-115"><xref:System.Int32>[]</span></span>  
  
-   <xref:System.Int64>  
  
-   <span data-ttu-id="e4c79-116"><xref:System.Int64>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-116"><xref:System.Int64>[]</span></span>  
  
-   <xref:System.Single>  
  
-   <span data-ttu-id="e4c79-117"><xref:System.Single>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-117"><xref:System.Single>[]</span></span>  
  
-   <xref:System.String>  
  
-   <xref:System.UInt16>  
  
-   <span data-ttu-id="e4c79-118"><xref:System.UInt16>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-118"><xref:System.UInt16>[]</span></span>  
  
-   <xref:System.UInt32>  
  
-   <span data-ttu-id="e4c79-119"><xref:System.UInt32>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-119"><xref:System.UInt32>[]</span></span>  
  
-   <xref:System.UInt64>  
  
-   <span data-ttu-id="e4c79-120"><xref:System.UInt64>[]</span><span class="sxs-lookup"><span data-stu-id="e4c79-120"><xref:System.UInt64>[]</span></span>  
  
## <a name="example"></a><span data-ttu-id="e4c79-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4c79-121">Example</span></span>  
 <span data-ttu-id="e4c79-122">L’exemple suivant montre comment ajouter et récupérer des données personnalisées à partir d’un <xref:System.Windows.Ink.StrokeCollection>.</span><span class="sxs-lookup"><span data-stu-id="e4c79-122">The following example demonstrates how to add and retrieve custom data from a <xref:System.Windows.Ink.StrokeCollection>.</span></span>  
  
 [!code-csharp[HowToAddCustomDataToInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#1)]  
  
 <span data-ttu-id="e4c79-123">L’exemple suivant crée une application qui affiche un <xref:System.Windows.Controls.InkCanvas> et deux boutons.</span><span class="sxs-lookup"><span data-stu-id="e4c79-123">The following example creates an application that displays an <xref:System.Windows.Controls.InkCanvas> and two buttons.</span></span>  <span data-ttu-id="e4c79-124">Le bouton, `switchAuthor`, permet à deux stylets utilisable par deux auteurs différents.</span><span class="sxs-lookup"><span data-stu-id="e4c79-124">The button, `switchAuthor`, enables two pens to be used by two different authors.</span></span>  <span data-ttu-id="e4c79-125">Le bouton `changePenColors` modifie la couleur de chaque trait sur le <xref:System.Windows.Controls.InkCanvas> en fonction de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e4c79-125">The button `changePenColors` changes the color of each stroke on the <xref:System.Windows.Controls.InkCanvas> according to the author.</span></span>  <span data-ttu-id="e4c79-126">L’application définit deux <xref:System.Windows.Ink.DrawingAttributes> objets et ajoute une propriété personnalisée à chacun d’eux qui indique l’auteur ayant dessiné le <xref:System.Windows.Ink.Stroke>.</span><span class="sxs-lookup"><span data-stu-id="e4c79-126">The application defines two <xref:System.Windows.Ink.DrawingAttributes> objects and adds a custom property to each one that indicates which author drew the <xref:System.Windows.Ink.Stroke>.</span></span>  <span data-ttu-id="e4c79-127">Lorsque l’utilisateur clique sur `changePenColors`, l’application modifie l’apparence du trait selon la valeur de la propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e4c79-127">When the user clicks `changePenColors`, the application changes the appearance of the stroke according to the value of the custom property.</span></span>  
  
 [!code-xaml[HowToAddCustomDataToInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[HowToAddCustomDataToInk#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#3)]
