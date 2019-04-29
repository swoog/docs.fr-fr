---
title: GetCustomUI
ms.date: 03/30/2017
helpviewer_keywords:
- custom error messages [WPF]
ms.assetid: e55180fc-35bb-4f80-a136-772b5eb3e4e5
ms.openlocfilehash: 30084143949d2243fd310448c52e6b861505ad66
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947964"
---
# <a name="getcustomui"></a>GetCustomUI
Appelé par PresentationHost.exe pour obtenir des messages d’erreur et de progression personnalisée à partir de l’hôte, si implémenté.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCustomUI( [out] BSTR* pwzProgressAssemblyName, [out] BSTR* pwzProgressClassName, [out] BSTR* pwzErrorAssemblyName, [out] BSTR* pwzErrorClassName );  
```  
  
## <a name="parameters"></a>Paramètres  
 `pwzProgressAssemblyName`  
  
 [out] Pointeur vers l’assembly qui contient l’interface utilisateur de progression fourni par l’hôte.  
  
 `pwzProgressClassName`  
  
 [out] Le nom de la classe qui est l’interface utilisateur de progression fourni par l’hôte, de préférence un [!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)] de fichiers avec <xref:System.Windows.Controls.Page> comme élément de niveau supérieur. Cette classe réside dans l’assembly spécifié par `pwzProgressAssemblyName`.  
  
 `pwzErrorAssemblyName`  
  
 [out] Pointeur vers l’assembly qui contient l’interface utilisateur d’erreur fourni par l’hôte.  
  
 `pwzErrorClassName`  
  
 [out] Le nom de la classe qui est l’utilisateur d’erreur fourni par l’hôte de l’interface, de préférence un fichier XAML avec <xref:System.Windows.Controls.Page> comme élément de niveau supérieur. Cette classe réside dans l’assembly spécifié par `pwzErrorAssemblyName`.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT : Ignoré.  
  
## <a name="remarks"></a>Notes  
 Une application hôte peut avoir un thème spécifique des interfaces utilisateur de PresentationHost.exe par défaut n’est peut-être pas conforme à. Si c’est le cas, l’application hôte peut implémenter [GetCustomUI](getcustomui.md) pour retourner les interfaces utilisateur progression et erreur à PresentationHost.exe. PresentationHost.exe appellera toujours [GetCustomUI](getcustomui.md) avant d’utiliser ses interfaces d’utilisateur par défaut.  
  
 Cette fonction est appelée une fois pendant l’initialisation de PresentationHost.  
  
## <a name="see-also"></a>Voir aussi

- [IWpfHostSupport](iwpfhostsupport.md)
