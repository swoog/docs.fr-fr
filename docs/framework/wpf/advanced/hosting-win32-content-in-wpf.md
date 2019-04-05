---
title: Hébergement de contenu Win32 dans WPF
ms.date: 03/30/2017
helpviewer_keywords:
- interoperability [WPF], tutorials
- Win32 code [WPF], WPF interoperation
- interoperability [WPF], Win32
ms.assetid: 3cc8644a-34f3-4082-9ddc-77623e4df2d8
ms.openlocfilehash: 8773cac1e421ecdca036e88d79797dae16f72b17
ms.sourcegitcommit: 68eb5c4928e2b082f178a42c16f73fedf52c2ab8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2019
ms.locfileid: "59055077"
---
# <a name="hosting-win32-content-in-wpf"></a>Hébergement de contenu Win32 dans WPF

## <a name="prerequisites"></a>Prérequis

Consultez [interopérabilité WPF et Win32](wpf-and-win32-interoperation.md).

## <a name="a-walkthrough-of-win32-inside-windows-presentation-framework-hwndhost"></a>Une procédure pas à pas de Win32 à l’intérieur de Windows Presentation Framework (HwndHost)

Pour réutiliser [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] contenu à l’intérieur de [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] applications, utilisez <xref:System.Windows.Interop.HwndHost>, qui est un contrôle qui permet à HWND de ressembler [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu. Comme <xref:System.Windows.Interop.HwndSource>, <xref:System.Windows.Interop.HwndHost> est simple à utiliser : dérivent <xref:System.Windows.Interop.HwndHost> et implémenter `BuildWindowCore` et `DestroyWindowCore` méthodes, puis instanciez votre <xref:System.Windows.Interop.HwndHost> classe dérivée et placez-le à l’intérieur de votre [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application.

Si votre [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] logique est déjà empaquetée comme un contrôle, puis votre `BuildWindowCore` implémentation n’est guère plus qu’un appel à `CreateWindow`. Par exemple, pour créer un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] contrôle LISTBOX dans [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)]:

```cpp
virtual HandleRef BuildWindowCore(HandleRef hwndParent) override {
    HWND handle = CreateWindowEx(0, L"LISTBOX",
    L"this is a Win32 listbox",
    WS_CHILD | WS_VISIBLE | LBS_NOTIFY
    | WS_VSCROLL | WS_BORDER,
    0, 0, // x, y
    30, 70, // height, width
    (HWND) hwndParent.Handle.ToPointer(), // parent hwnd
    0, // hmenu
    0, // hinstance
    0); // lparam

    return HandleRef(this, IntPtr(handle));
}

virtual void DestroyWindowCore(HandleRef hwnd) override {
    // HwndHost will dispose the hwnd for us
}
```

Mais supposons que le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] code n’est pas tout à fait si autonome ? Si vous pouvez donc créer un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] boîte de dialogue zone et incorporer son contenu dans une valeur plus élevée [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application. L’exemple illustre ce dans [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)] et [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)], bien qu’il est également possible de le faire dans une autre langue ou à la ligne de commande.

Démarrer avec une boîte de dialogue simple, qui est compilé dans un [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)] [!INCLUDE[TLA2#tla_dll](../../../../includes/tla2sharptla-dll-md.md)] projet.

Ensuite, introduire la boîte de dialogue dans la plus grande [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application :

- Compilez le [!INCLUDE[TLA2#tla_dll](../../../../includes/tla2sharptla-dll-md.md)] comme géré (`/clr`)

- Activer la boîte de dialogue dans un contrôle

- Définissez la classe dérivée de <xref:System.Windows.Interop.HwndHost> avec `BuildWindowCore` et `DestroyWindowCore` méthodes

- Substituer `TranslateAccelerator` méthode pour gérer les clés de la boîte de dialogue

- Substituer `TabInto` pour prendre en charge la tabulation (méthode)

- Substituer `OnMnemonic` pour prendre en charge les mnémoniques (méthode)

- Instanciez le <xref:System.Windows.Interop.HwndHost> sous-classe et placez-le sous le bon [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] élément

### <a name="turn-the-dialog-into-a-control"></a>Activer la boîte de dialogue dans un contrôle

Vous pouvez activer une boîte de dialogue en un HWND à l’aide de styles WS_CHILD et DS_CONTROL enfant. Aller dans le fichier de ressources (.rc) où la boîte de dialogue est défini et recherchez le début de la définition de la boîte de dialogue :

```
IDD_DIALOG1 DIALOGEX 0, 0, 303, 121
STYLE DS_SETFONT | DS_MODALFRAME | DS_FIXEDSYS | WS_POPUP | WS_CAPTION | WS_SYSMENU
```

Modifier la deuxième ligne à :

```
STYLE DS_SETFONT | WS_CHILD | WS_BORDER | DS_CONTROL
```

Cette action ne pas entièrement l’empaqueter dans un contrôle autonome. Vous devez toujours appeler `IsDialogMessage()` donc [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] peut traiter certains messages, mais la modification du contrôle offre un moyen simple de placer ces contrôles à l’intérieur d’un autre HWND.

## <a name="subclass-hwndhost"></a>Sous-classe HwndHost

Importez les espaces de noms suivants :

```cpp
namespace ManagedCpp
{
    using namespace System;
    using namespace System::Windows;
    using namespace System::Windows::Interop;
    using namespace System::Windows::Input;
    using namespace System::Windows::Media;
    using namespace System::Runtime::InteropServices;
```

Puis créez une classe dérivée de <xref:System.Windows.Interop.HwndHost> et remplacer le `BuildWindowCore` et `DestroyWindowCore` méthodes :

```cpp
public ref class MyHwndHost : public HwndHost, IKeyboardInputSink {
    private:
        HWND dialog;

    protected:
        virtual HandleRef BuildWindowCore(HandleRef hwndParent) override {
            InitializeGlobals();
            dialog = CreateDialog(hInstance,
                MAKEINTRESOURCE(IDD_DIALOG1),
                (HWND) hwndParent.Handle.ToPointer(),
                (DLGPROC) About);
            return HandleRef(this, IntPtr(dialog));
        }

        virtual void DestroyWindowCore(HandleRef hwnd) override {
            // hwnd will be disposed for us
        }
```

Vous utilisez ici le `CreateDialog` pour créer la boîte de dialogue qui est vraiment un contrôle. Dans la mesure où il s’agit d’une des premières méthodes appelée à l’intérieur de la [!INCLUDE[TLA2#tla_dll](../../../../includes/tla2sharptla-dll-md.md)], vous devez faire quelques standard [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] l’initialisation en appelant une fonction que vous définirez ultérieurement, appelée `InitializeGlobals()`:

```cpp
bool initialized = false;
    void InitializeGlobals() {
        if (initialized) return;
        initialized = true;

        // TODO: Place code here.
        MSG msg;
        HACCEL hAccelTable;

        // Initialize global strings
        LoadString(hInstance, IDS_APP_TITLE, szTitle, MAX_LOADSTRING);
        LoadString(hInstance, IDC_TYPICALWIN32DIALOG, szWindowClass, MAX_LOADSTRING);
        MyRegisterClass(hInstance);
```

### <a name="override-translateaccelerator-method-to-handle-dialog-keys"></a>Substituez la méthode TranslateAccelerator pour gérer les clés de la boîte de dialogue

Si vous avez exécuté cet exemple maintenant, vous obtiendriez un contrôle de boîte de dialogue qui affiche, mais il serait ignorer tout du clavier traitement qui rendent une boîte de dialogue une boîte de dialogue fonctionnelle. Vous devez maintenant substituer le `TranslateAccelerator` implémentation (ce qui provient de `IKeyboardInputSink`, une interface qui <xref:System.Windows.Interop.HwndHost> implémente). Cette méthode est appelée lorsque l’application reçoit WM_KEYDOWN et WM_SYSKEYDOWN.

```cpp
#undef TranslateAccelerator
        virtual bool TranslateAccelerator(System::Windows::Interop::MSG% msg,
            ModifierKeys modifiers) override
        {
            ::MSG m = ConvertMessage(msg);

            // Win32's IsDialogMessage() will handle most of our tabbing, but doesn't know
            // what to do when it reaches the last tab stop
            if (m.message == WM_KEYDOWN && m.wParam == VK_TAB) {
                HWND firstTabStop = GetDlgItem(dialog, IDC_EDIT1);
                HWND lastTabStop = GetDlgItem(dialog, IDCANCEL);
                TraversalRequest^ request = nullptr;

                if (GetKeyState(VK_SHIFT) && GetFocus() == firstTabStop) {
                    // this code should work, but there’s a bug with interop shift-tab in current builds
                    request = gcnew TraversalRequest(FocusNavigationDirection::Last);
                }
                else if (!GetKeyState(VK_SHIFT) && GetFocus() == lastTabStop) {
                    request = gcnew TraversalRequest(FocusNavigationDirection::Next);
                }

                if (request != nullptr)
                    return ((IKeyboardInputSink^) this)->KeyboardInputSite->OnNoMoreTabStops(request);

            }

            // Only call IsDialogMessage for keys it will do something with.
            if (msg.message == WM_SYSKEYDOWN || msg.message == WM_KEYDOWN) {
                switch (m.wParam) {
                    case VK_TAB:
                    case VK_LEFT:
                    case VK_UP:
                    case VK_RIGHT:
                    case VK_DOWN:
                    case VK_EXECUTE:
                    case VK_RETURN:
                    case VK_ESCAPE:
                    case VK_CANCEL:
                        IsDialogMessage(dialog, &m);
                        // IsDialogMessage should be called ProcessDialogMessage --
                        // it processes messages without ever really telling you
                        // if it handled a specific message or not
                        return true;
                }
            }

            return false; // not a key we handled
        }
```

Il s’agit d’une grande quantité de code en une seule pièce, il pouvait ainsi utiliser certains des explications plus détaillées. Tout d’abord, le code à l’aide [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)] et [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)] macros ; vous devez être conscient qu’il existe déjà une macro nommée `TranslateAccelerator`, qui est défini dans winuser.h :

```cpp
#define TranslateAccelerator  TranslateAcceleratorW
```

Veillez à définir un `TranslateAccelerator` (méthode) et non un `TranslateAcceleratorW` (méthode).

De même, il est à la fois le winuser.h MSG non managé et managé `Microsoft::Win32::MSG` struct. Vous pouvez supprimer l’ambiguïté entre les deux à l’aide de la [!INCLUDE[TLA#tla_cpp](../../../../includes/tlasharptla-cpp-md.md)] `::` opérateur.

```cpp
virtual bool TranslateAccelerator(System::Windows::Interop::MSG% msg,
    ModifierKeys modifiers) override
{
    ::MSG m = ConvertMessage(msg);
}

Both MSGs have the same data, but sometimes it is easier to work with the unmanaged definition, so in this sample you can define the obvious conversion routine:

```cpp
::MSG ConvertMessage(System::Windows::Interop::MSG% msg) {
    ::MSG m;
    m.hwnd = (HWND) msg.hwnd.ToPointer();
    m.lParam = (LPARAM) msg.lParam.ToPointer();
    m.message = msg.message;
    m.wParam = (WPARAM) msg.wParam.ToPointer();

    m.time = msg.time;

    POINT pt;
    pt.x = msg.pt_x;
    pt.y = msg.pt_y;
    m.pt = pt;

    return m;
}
```

À `TranslateAccelerator`. Le principe de base consiste à appeler le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fonction `IsDialogMessage` aux tâches autant que possible, mais `IsDialogMessage` n’a pas accès à rien en dehors de la boîte de dialogue. Comme onglet utilisateur autour de la boîte de dialogue, lorsque la tabulation s’exécute après le dernier contrôle dans notre boîte de dialogue, vous devez définir le focus sur le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] partie en appelant `IKeyboardInputSite::OnNoMoreStops`.

```cpp
// Win32's IsDialogMessage() will handle most of the tabbing, but doesn't know
// what to do when it reaches the last tab stop
if (m.message == WM_KEYDOWN && m.wParam == VK_TAB) {
    HWND firstTabStop = GetDlgItem(dialog, IDC_EDIT1);
    HWND lastTabStop = GetDlgItem(dialog, IDCANCEL);
    TraversalRequest^ request = nullptr;

    if (GetKeyState(VK_SHIFT) && GetFocus() == firstTabStop) {
        request = gcnew TraversalRequest(FocusNavigationDirection::Last);
    }
    else if (!GetKeyState(VK_SHIFT) && GetFocus() ==  lastTabStop) { {
        request = gcnew TraversalRequest(FocusNavigationDirection::Next);
    }

    if (request != nullptr)
        return ((IKeyboardInputSink^) this)->KeyboardInputSite->OnNoMoreTabStops(request);
}
```

Pour finir, appelez `IsDialogMessage`. Mais une des responsabilités d’un `TranslateAccelerator` signale à méthode [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] si vous avez géré ou non la séquence de touches. Si vous n’avez pas géré il, l’événement d’entrée peut créer un tunnel et se propage à travers le reste de l’application. Ici, vous exposerez une particularité de la gestion des messages clavier et la nature de l’architecture d’entrée dans [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)]. Malheureusement, `IsDialogMessage` ne retourne pas de quelque manière s’il gère une séquence de touches particulière. Pire encore, il appellera `DispatchMessage()` sur les séquences de touches qu’il ne doit pas gérer !  Afin d’avoir à procéder à la rétroconception `IsDialogMessage`et appeler uniquement pour les clés que vous savez qu’il gérera :

```cpp
// Only call IsDialogMessage for keys it will do something with.
if (msg.message == WM_SYSKEYDOWN || msg.message == WM_KEYDOWN) {
    switch (m.wParam) {
        case VK_TAB:
        case VK_LEFT:
        case VK_UP:
        case VK_RIGHT:
        case VK_DOWN:
        case VK_EXECUTE:
        case VK_RETURN:
        case VK_ESCAPE:
        case VK_CANCEL:
            IsDialogMessage(dialog, &m);
            // IsDialogMessage should be called ProcessDialogMessage --
            // it processes messages without ever really telling you
            // if it handled a specific message or not
            return true;
    }
```

### <a name="override-tabinto-method-to-support-tabbing"></a>Substituer la méthode TabInto pour la prise en charge la tabulation

Maintenant que vous avez implémenté `TranslateAccelerator`, un utilisateur peut tabuler à l’intérieur de la boîte de dialogue tab dans la plus grande et boîte [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application. Mais un utilisateur ne peut pas onglet dans la boîte de dialogue. Pour résoudre ce problème, vous substituez `TabInto`:

```cpp
public:
    virtual bool TabInto(TraversalRequest^ request) override {
        if (request->FocusNavigationDirection == FocusNavigationDirection::Last) {
            HWND lastTabStop = GetDlgItem(dialog, IDCANCEL);
            SetFocus(lastTabStop);
        }
        else {
            HWND firstTabStop = GetDlgItem(dialog, IDC_EDIT1);
            SetFocus(firstTabStop);
        }
        return true;
    }
```

Le `TraversalRequest` paramètre indique si l’action de l’onglet est un onglet ou MAJ.

### <a name="override-onmnemonic-method-to-support-mnemonics"></a>Substituer la méthode OnMnemonic pour prendre en charge les mnémoniques

Gestion du clavier est presque terminée, mais il en existe une chose qui manque – mnémoniques ne fonctionnent pas. Si un utilisateur appuie sur alt-F, le focus ne saute pas à la « First name : « zone d’édition. Par conséquent, vous substituez le `OnMnemonic` méthode :

```cpp
virtual bool OnMnemonic(System::Windows::Interop::MSG% msg, ModifierKeys modifiers) override {
    ::MSG m = ConvertMessage(msg);

    // If it's one of our mnemonics, set focus to the appropriate hwnd
    if (msg.message == WM_SYSCHAR && GetKeyState(VK_MENU /*alt*/)) {
        int dialogitem = 9999;
        switch (m.wParam) {
            case 's': dialogitem = IDOK; break;
            case 'c': dialogitem = IDCANCEL; break;
            case 'f': dialogitem = IDC_EDIT1; break;
            case 'l': dialogitem = IDC_EDIT2; break;
            case 'p': dialogitem = IDC_EDIT3; break;
            case 'a': dialogitem = IDC_EDIT4; break;
            case 'i': dialogitem = IDC_EDIT5; break;
            case 't': dialogitem = IDC_EDIT6; break;
            case 'z': dialogitem = IDC_EDIT7; break;
        }
        if (dialogitem != 9999) {
            HWND hwnd = GetDlgItem(dialog, dialogitem);
            SetFocus(hwnd);
            return true;
        }
    }
    return false; // key unhandled
};
```

Pourquoi ne pas appeler `IsDialogMessage` ici ?  Vous avez le même problème comme avant, vous devez être en mesure d’informer [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] code si votre code a géré ou non, la séquence de touches et `IsDialogMessage` ne peut pas faire. Il existe également un second problème car `IsDialogMessage` refuse de traiter le mnémonique lorsque le HWND ayant le focus ne se trouve pas dans la boîte de dialogue.

### <a name="instantiate-the-hwndhost-derived-class"></a>Instancier la classe dérivée HwndHost

Enfin, maintenant que la prise en charge des clés et l’onglet est en place, vous pouvez placer votre <xref:System.Windows.Interop.HwndHost> dans la plus grande [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application. Si l’application principale est écrite [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], pour placer au bon endroit le plus simple consiste à laisser vide <xref:System.Windows.Controls.Border> élément où vous souhaitez placer le <xref:System.Windows.Interop.HwndHost>. Ici, vous créez un <xref:System.Windows.Controls.Border> nommé `insertHwndHostHere`:

```xaml
<Window x:Class="WPFApplication1.Window1"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    Title="Windows Presentation Framework Application"
    Loaded="Window1_Loaded"
    >
    <StackPanel>
        <Button Content="WPF button"/>
        <Border Name="insertHwndHostHere" Height="200" Width="500"/>
        <Button Content="WPF button"/>
    </StackPanel>
</Window>
```

Puis ne reste qu’à trouver un bon emplacement dans la séquence de code pour instancier le <xref:System.Windows.Interop.HwndHost> et connectez-le à la <xref:System.Windows.Controls.Border>. Dans cet exemple, vous allez le mettre à l’intérieur du constructeur pour la <xref:System.Windows.Window> classe dérivée :

```csharp
public partial class Window1 : Window {
    public Window1() {
    }

    void Window1_Loaded(object sender, RoutedEventArgs e) {
        HwndHost host = new ManagedCpp.MyHwndHost();
        insertHwndHostHere.Child = host;
    }
}
```

Qui vous offre :

![Capture d’écran WPF application](./media/interoparch09.PNG "InteropArch09")

## <a name="see-also"></a>Voir aussi

- [Interopérabilité WPF et Win32](wpf-and-win32-interoperation.md)
