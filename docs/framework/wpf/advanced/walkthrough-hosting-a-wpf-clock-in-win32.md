---
title: 'Procédure pas à pas : hébergement d’une horloge WPF dans Win32'
ms.date: 03/30/2017
helpviewer_keywords:
- interoperability [WPF], tutorials
- Win32 code [WPF], WPF interoperation
- interoperability [WPF], Win32
ms.assetid: 555e55a7-0851-4ec8-b1c6-0acba7e9b648
ms.openlocfilehash: 4001c34f6673e036bdbf731baed782c6dc0a16b0
ms.sourcegitcommit: 89fcad7e816c12eb1299128481183f01c73f2c07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "63808047"
---
# <a name="walkthrough-hosting-a-wpf-clock-in-win32"></a>Procédure pas à pas : hébergement d’une horloge WPF dans Win32

Pour placer [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] à l’intérieur de [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] applications, utilisez <xref:System.Windows.Interop.HwndSource>, qui fournit le HWND qui contient votre [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu. Tout d’abord, vous créez le <xref:System.Windows.Interop.HwndSource>, en lui attribuant des paramètres similaires à CreateWindow. Vous indiquez ensuite le <xref:System.Windows.Interop.HwndSource> sur le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu que vous voulez qu’il. Enfin, vous obtenez le HWND de la <xref:System.Windows.Interop.HwndSource>. Cette procédure pas à pas montre comment créer un mixte [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] à l’intérieur de [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] application qui implémente de nouveau le système d’exploitation **propriétés de Date et heure** boîte de dialogue.

## <a name="prerequisites"></a>Prérequis

Consultez [interopérabilité WPF et Win32](wpf-and-win32-interoperation.md).

## <a name="how-to-use-this-tutorial"></a>Comment utiliser ce didacticiel

Ce didacticiel se concentre sur les étapes importantes de la production d’une application d’interopérabilité. Le didacticiel est complété par un exemple, [interopérabilité Win32 Clock, exemple](https://go.microsoft.com/fwlink/?LinkID=160051), mais que l’exemple est reflètent le produit final. Ce didacticiel décrit les étapes comme si vous commenciez avec un existant [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] projet de votre choix, éventuellement un projet préexistant et vous ajoutiez un hébergé [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] à votre application. Vous pouvez comparer votre produit final avec [interopérabilité Win32 Clock, exemple](https://go.microsoft.com/fwlink/?LinkID=160051).

## <a name="a-walkthrough-of-windows-presentation-framework-inside-win32-hwndsource"></a>Procédure pas à pas de Windows Presentation Foundation dans Win32 (HwndSource)

Le graphique suivant illustre le produit final prévu pour ce didacticiel :

![Capture d’écran qui affiche la boîte de dialogue Propriétés de Date et heure.](./media/walkthrough-hosting-a-wpf-clock-in-win32/date-time-properties-dialog.png)

Vous pouvez recréer cette boîte de dialogue en créant un C++ projet Win32 dans Visual Studio et à l’aide de l’éditeur de boîtes de dialogue pour créer les éléments suivants :

![Boîte de dialogue Propriétés de Date et heure recréée](./media/walkthrough-hosting-a-wpf-clock-in-win32/recreated-date-time-properties-dialog.png)

(Vous n’avez pas besoin d’utiliser [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)] à utiliser <xref:System.Windows.Interop.HwndSource>, et vous n’avez pas besoin d’utiliser C++ pour écrire [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] programmes, mais cela est un moyen classique pour ce faire et se prête bien à une explication de didacticiel pas à pas).

Vous devez suivre cinq sous-étapes particulières pour placer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] horloge dans la boîte de dialogue :

1. Activer votre [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] projet pour appeler du code managé (**/CLR**) en modifiant les paramètres du projet dans [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)].

2. Créer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Page> dans une DLL distincte.

3. Put qui [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Page> à l’intérieur d’un <xref:System.Windows.Interop.HwndSource>.

4. Procurez-vous un HWND pour qui <xref:System.Windows.Controls.Page> à l’aide de la <xref:System.Windows.Interop.HwndSource.Handle%2A> propriété.

5. Utilisez [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] décider où placer le HWND dans la plus grande [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] application

## <a name="clr"></a>/clr

La première étape consiste à convertir ce unmanaged [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] projet en une seule peut appeler du code managé. Vous utilisez l’option de compilateur/CLR, qui sera liée aux DLL nécessaires que vous souhaitez utiliser, puis ajustez la méthode Main pour une utilisation avec [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].

Pour activer l’utilisation du code managé dans le projet C++ : Avec le bouton droit sur les projet win32clock, puis sélectionnez **propriétés**. Sur le **général** page de propriétés (valeur par défaut), modifier la prise en charge du Common Language Runtime à `/clr`.

Ensuite, ajoutez des références aux DLL nécessaires pour [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]: PresentationCore.dll, PresentationFramework.dll, System.dll, WindowsBase.dll, UIAutomationProvider.dll et UIAutomationTypes.dll. Les instructions suivantes supposent que le système d’exploitation est installé sur le lecteur C:.

1. Cliquez sur les projet win32clock, puis sélectionnez **références...** et à l’intérieur de cette boîte de dialogue :

2. Cliquez sur les projet win32clock, puis sélectionnez **références...** .

3. Cliquez sur **ajouter une nouvelle référence**, onglet Parcourir, entrez C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationCore.dll, puis cliquez sur OK.

4. Répétez pour PresentationFramework.dll : C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationFramework.dll.

5. Répétez pour WindowsBase.dll : C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\WindowsBase.dll.

6. Répétez pour UIAutomationTypes.dll : C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\UIAutomationTypes.dll.

7. Répétez pour UIAutomationProvider.dll : C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\UIAutomationProvider.dll.

8. Cliquez sur **ajouter une nouvelle référence**, sélectionnez System.dll, puis cliquez sur **OK**.

9. Cliquez sur **OK** pour quitter les Pages de propriétés win32clock pour l’ajout de références.

 Enfin, ajoutez le `STAThreadAttribute` à la `_tWinMain` méthode pour une utilisation avec [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]:

```cpp
[System::STAThreadAttribute]
int APIENTRY _tWinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPTSTR    lpCmdLine,
                     int       nCmdShow)
```

Cet attribut indique à la [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] que lorsqu’il initialise [!INCLUDE[TLA#tla_com](../../../../includes/tlasharptla-com-md.md)], il doit utiliser un modèle de thread unique cloisonné (STA), qui est nécessaire pour [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] (et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]).

## <a name="create-a-windows-presentation-framework-page"></a>Créer une page Windows Presentation Framework

Ensuite, vous créez une DLL qui définit un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Page>. Il est souvent plus facile de créer le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Page> en tant qu’application autonome et d’écriture et de débogage la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] partie de cette façon. Une fois terminé, ce projet peut être activé dans une DLL en double-cliquant sur le projet, en cliquant sur **propriétés**, accédant à l’Application et la modification du type de sortie à la bibliothèque de classes Windows.

Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] projet dll peut être combiné avec le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] (solution comprenant deux projets) avec le bouton droit sur la solution, sélectionnez **projet**.

À utiliser qui [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] dll à partir de la [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] projet, vous devez ajouter une référence :

1. Cliquez sur les projet win32clock, puis sélectionnez **références...** .

2. Cliquez sur **ajouter une nouvelle référence**.

3. Cliquez sur l’onglet **Projets**. Sélectionnez WPFClock, puis cliquez sur OK.

4. Cliquez sur **OK** pour quitter les Pages de propriétés win32clock pour l’ajout de références.

## <a name="hwndsource"></a>HwndSource

Ensuite, vous utilisez <xref:System.Windows.Interop.HwndSource> pour rendre le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Page> ressembler un HWND. Ajoutez ce bloc de code dans un fichier C++ :

```cpp
namespace ManagedCode
{
    using namespace System;
    using namespace System::Windows;
    using namespace System::Windows::Interop;
    using namespace System::Windows::Media;

    HWND GetHwnd(HWND parent, int x, int y, int width, int height) {
        HwndSource^ source = gcnew HwndSource(
            0, // class style
            WS_VISIBLE | WS_CHILD, // style
            0, // exstyle
            x, y, width, height,
            "hi", // NAME
            IntPtr(parent)        // parent window
            );

        UIElement^ page = gcnew WPFClock::Clock();
        source->RootVisual = page;
        return (HWND) source->Handle.ToPointer();
    }
}
}
```

 Il s’agit d’un long bloc de code qui mérite une explication. La première partie est constituée de diverses clauses qui vous évitent d’avoir à qualifier complètement tous les appels :

```cpp
namespace ManagedCode
{
    using namespace System;
    using namespace System::Windows;
    using namespace System::Windows::Interop;
    using namespace System::Windows::Media;
```

 Puis vous définissez une fonction qui crée le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] du contenu, met un <xref:System.Windows.Interop.HwndSource> autour d’elle et retourne le HWND :

```cpp
HWND GetHwnd(HWND parent, int x, int y, int width, int height) {
```

Tout d’abord, vous créez un <xref:System.Windows.Interop.HwndSource>, dont les paramètres sont similaires à CreateWindow :

```cpp
HwndSource^ source = gcnew HwndSource(
    0, // class style
    WS_VISIBLE | WS_CHILD, // style
    0, // exstyle
    x, y, width, height,
    "hi", // NAME
    IntPtr(parent) // parent window
);
```

Ensuite vous créez la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] classe de contenu en appelant son constructeur :

```cpp
UIElement^ page = gcnew WPFClock::Clock();
```

Vous connectez ensuite la page à la <xref:System.Windows.Interop.HwndSource>:

```cpp
source->RootVisual = page;
```

 Et dans la dernière ligne, retournez le HWND pour le <xref:System.Windows.Interop.HwndSource>:

```cpp
return (HWND) source->Handle.ToPointer();
```

## <a name="positioning-the-hwnd"></a>Positionnement du Hwnd

Maintenant que vous avez un HWND contenant le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] horloge, vous devez placer le HWND dans le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] boîte de dialogue. Si vous saviez exactement où placer le HWND, vous suffirait de communiquer cette taille et l’emplacement pour le `GetHwnd` fonction que vous avez défini précédemment. Toutefois, étant donné que vous avez utilisé un fichier de ressources pour définir la boîte de dialogue, vous ne savez pas exactement où les HWND sont positionnés. Vous pouvez utiliser la [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)] éditeur de boîtes de dialogue pour placer un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] statique contrôler l’emplacement où l’horloge (« insérer l’horloge ici ») et l’utiliser pour positionner le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] horloge.

Lorsque vous gérez WM_INITDIALOG, vous utilisez `GetDlgItem` pour récupérer le HWND de l’espace réservé STATIC :

```cpp
HWND placeholder = GetDlgItem(hDlg, IDC_CLOCK);
```

Vous devez calculer la taille et la position de cet espace réservé STATIC, afin de pouvoir placer les [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] d’horloge à cet endroit :

RECT rectangle;

```cpp
GetWindowRect(placeholder, &rectangle);
int width = rectangle.right - rectangle.left;
int height = rectangle.bottom - rectangle.top;
POINT point;
point.x = rectangle.left;
point.y = rectangle.top;
result = MapWindowPoints(NULL, hDlg, &point, 1);
```

Ensuite, masquez l’espace réservé STATIC :

```cpp
ShowWindow(placeholder, SW_HIDE);
```

Et créer le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] HWND dans cet emplacement de l’horloge :

```cpp
HWND clock = ManagedCode::GetHwnd(hDlg, point.x, point.y, width, height);
```

Pour rendre le didacticiel intéressant et créer une véritable [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] horloge, vous devez créer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contrôle d’horloge à ce stade. Cette procédure se fait principalement en langage de balisage, avec quelques gestionnaires d’événements dans le code-behind. Étant donné que ce didacticiel est sur l’interopérabilité et pas la conception des contrôles, le code complet de le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] horloge est fourni ici comme un bloc de code, sans instructions discrètes pour le développement ou la signification de chaque partie. N’hésitez pas à tester ce code pour changer l’apparence ou la fonctionnalité du contrôle.

Voici le code XAML :

[!code-xaml[Win32Clock#AllClockXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/Win32Clock/CS/Clock.xaml#allclockxaml)]

Voici le code-behind correspondant :

[!code-csharp[Win32Clock#AllClockCS](~/samples/snippets/csharp/VS_Snippets_Wpf/Win32Clock/CS/Clock.xaml.cs#allclockcs)]

Le résultat final ressemble à ceci :

![Boîte de dialogue Propriétés de Date et heure de résultat final](./media/walkthrough-hosting-a-wpf-clock-in-win32/final-result-date-time-properties-dialog.png)

Pour comparer votre résultat final au code qui a produit cette capture d’écran, consultez [interopérabilité Win32 Clock, exemple](https://go.microsoft.com/fwlink/?LinkID=160051).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Interop.HwndSource>
- [Interopérabilité WPF et Win32](wpf-and-win32-interoperation.md)
- [Interopérabilité Win32 Clock, exemple](https://go.microsoft.com/fwlink/?LinkID=160051)
