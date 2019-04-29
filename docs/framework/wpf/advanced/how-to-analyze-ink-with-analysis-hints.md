---
title: 'Procédure : Analyser l’entrée manuscrite avec des indications d’analyse'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], analyzing
- analyzing ink [WPF]
- ink [WPF], AnalysisHintNode objects [WPF]
- AnalysisHintNode objects [WPF]
ms.assetid: d4421ed4-77f5-4640-829e-9f1de50b2ff2
ms.openlocfilehash: a4c38ddf52e9054fe9126df4b7e172548617b90d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776998"
---
# <a name="how-to-analyze-ink-with-analysis-hints"></a>Procédure : Analyser l’entrée manuscrite avec des indications d’analyse
Un [System.Windows.Ink.AnalysisHintNode](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) fournit une indication pour le [System.Windows.Ink.InkAnalyze](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) auquel il est joint.  L’indicateur s’applique à la zone spécifiée par le [System.Windows.Ink.ContextNode.Location%2A](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms594508(v=vs.90)) propriété de la [System.Windows.Ink.AnalysisHintNode](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) et fournit un contexte supplémentaire à l’Analyseur de l’encre à améliorer la précision de la reconnaissance. Le [System.Windows.Ink.InkAnalyze](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms616754(v=vs.90)) applique ces informations de contexte lors de l’analyse de l’encre obtenue dans la zone de l’indication.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant est une application qui utilise plusieurs [System.Windows.Ink.AnalysisHintNode](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms610344(v=vs.90)) objets sur un formulaire qui accepte l’entrée d’encre. L’application utilise le [System.Windows.Ink.AnalysisHintNode.Factoid%2A](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms594341(v=vs.90)) propriété afin de fournir des informations de contexte pour chaque entrée sur le formulaire.  L’application utilise l’analyse de l’arrière-plan pour analyser l’encre et efface le formulaire de l’encre toutes les cinq secondes, une fois que l’utilisateur arrête l’ajout de l’encre.  
  
 [!code-xaml[HowToAnalyzeInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml#1)]  
  
 [!code-csharp[HowToAnalyzeInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAnalyzeInk/CSharp/FormAnalyzer.xaml.cs#2)]
 [!code-vb[HowToAnalyzeInk#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToAnalyzeInk/VisualBasic/FormAnalyzer.xaml.vb#2)]
