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
ms.openlocfilehash: 589e28b3c05496e3fc17055b98240e389faed068
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62007485"
---
# <a name="how-to-use-an-application-scope-resource-dictionary"></a>Procédure : Utiliser un dictionnaire de ressources de portée application
Cet exemple montre comment définir et utiliser un dictionnaire de ressources personnalisé de portée application.  
  
## <a name="example"></a>Exemple  
 <xref:System.Windows.Application> expose un magasin de portée application pour les ressources partagées : <xref:System.Windows.Application.Resources%2A>. Par défaut, le <xref:System.Windows.Application.Resources%2A> propriété est initialisée avec une instance de la <xref:System.Windows.ResourceDictionary> type. Vous utilisez cette instance lorsque vous obtenez et définissez les propriétés de portée application à l’aide de <xref:System.Windows.Application.Resources%2A>. Pour plus d'informations, voir [Procédure : Obtenir et définir une ressource de portée Application](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).
  
 Si vous disposez de plusieurs ressources que vous définissez à l’aide de <xref:System.Windows.Application.Resources%2A>, vous pouvez utiliser un dictionnaire de ressources personnalisé pour stocker ces ressources et définir <xref:System.Windows.Application.Resources%2A> avec lui à la place. L’exemple suivant montre comment déclarer un dictionnaire de ressources personnalisé à l’aide de XAML.
  
 [!code-xaml[HOWTOResourceDictionaries#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MyResourceDictionary.xaml#1)]  
  
 Le remplacement de dictionnaires de ressources entiers à l’aide de <xref:System.Windows.Application.Resources%2A> vous permet de prendre en charge des thèmes de portée application, où chaque thème est encapsulé par un dictionnaire de ressources unique. L'exemple suivant montre comment définir <xref:System.Windows.ResourceDictionary>.  
  
 [!code-xaml[HOWTOResourceDictionaries#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/App.xaml#2)]  
  
 L’exemple suivant montre comment vous pouvez obtenir des ressources de portée application à partir du dictionnaire de ressources exposé par <xref:System.Windows.Application.Resources%2A> dans XAML.  
  
 [!code-xaml[HOWTOResourceDictionaries#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml#4)]  
  
 Voici également comment obtenir les ressources dans le code.  
  
 [!code-csharp[HOWTOResourceDictionaries#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml.cs#3)]
 [!code-vb[HOWTOResourceDictionaries#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToResourceDictionaries/VB/MainWindow.xaml.vb#3)]  
  
 Il existe deux considérations à prendre lorsque vous utilisez <xref:System.Windows.Application.Resources%2A>. Tout d’abord, le dictionnaire *clé* est un objet, vous devez donc utiliser exactement la même instance d’objet lors du paramétrage et l’obtention d’une valeur de propriété. (Notez qu’en cas d’utilisation d’une chaîne, la clé respecte la casse.) Ensuite, le dictionnaire *valeur* est un objet, donc vous devrez convertir la valeur vers le type souhaité lors de l’obtention d’une valeur de propriété.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.ResourceDictionary>
- <xref:System.Windows.Application.Resources%2A>
- [Ressources XAML](../advanced/xaml-resources.md)
- [Dictionnaires de ressources fusionnés](../advanced/merged-resource-dictionaries.md)
