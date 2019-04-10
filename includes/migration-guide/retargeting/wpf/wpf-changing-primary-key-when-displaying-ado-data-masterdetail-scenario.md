---
ms.openlocfilehash: 1d9841b9c8989a07820c75ac07940c90e5c0753e
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760838"
---
### <a name="wpf-changing-a-primary-key-when-displaying-ado-data-in-a-masterdetail-scenario"></a>WPF : Modification d’une clé primaire lors de l’affichage de données ADO dans un scénario maître/détail

|   |   |
|---|---|
|Détails|Supposez que vous avez une collection ADO d’éléments de type <code>Order</code> avec une relation nommée &quot;OrderDetails&quot; mise en relation avec une collection d’éléments de type <code>Detail</code> via la clé primaire &quot;OrderID&quot;. Dans votre application WPF, vous pouvez lier un contrôle de liste aux détails d’un ordre spécifique :<pre><code class="lang-xml">&lt;ListBox ItemsSource=&quot;{Binding Path=OrderDetails}&quot; &gt;&#13;&#10;</code></pre>où DataContext est un <code>Order</code>. WPF obtient la valeur de la propriété <code>OrderDetails</code> - une collection D de tous les éléments <code>Detail</code> dont <code>OrderID</code> correspond au <code>OrderID</code> de l’élément principal. Le changement de comportement se produit lorsque vous modifiez la clé primaire <code>OrderID</code> de l’élément principal. ADO modifie automatiquement le <code>OrderID</code> de chacun des enregistrements concernés dans la collection de détails (à savoir les enregistrements copiés dans la collection D).  Qu'advient-il ensuite de la collection D ?<ul><li>Ancien comportement :   la collection D est effacée.   L’élément principal ne déclenche <em>aucune</em> notification de modification pour la propriété <code>OrderDetails</code>.  La zone de liste continue d’utiliser la collection D, qui est maintenant vide.</li><li>Nouveau comportement :  la collection D reste inchangée.   Chacun de ses éléments déclenche une notification de modification pour la propriété <code>OrderID</code>.  La zone de liste continue d’utiliser la collection D et affiche les détails avec le nouveau <code>OrderID</code>.</li></ul>WPF implémente le nouveau comportement en créant la collection D d’une autre manière : en appelant la méthode ADO <xref:System.Data.DataRowView.CreateChildView(System.Data.DataRelation,System.Boolean)?displayProperty=nameWithType> avec l’argument <code>followParent</code> défini sur <code>true</code>.|
|Suggestion|Une application obtient le nouveau comportement à l’aide du commutateur AppContext suivant.<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Data.DoNotUseFollowParentWhenBindingToADODataRelation=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;&#13;&#10;</code></pre>Le commutateur par défaut est <code>true</code> (ancien comportement) pour les applications qui ciblent .NET 4.7.1 ou version antérieure, et <code>false</code> (nouveau comportement) pour les applications qui ciblent .NET 4.7.2 ou version ultérieure.|
|Portée|Mineur|
|Version|4.7.2|
|Type|Reciblage|

