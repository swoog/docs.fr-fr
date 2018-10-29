---
title: Création de la classe Game1
ms.date: 03/30/2017
ms.assetid: 47932ce3-2ba5-476f-a26b-3ddfd5226f27
ms.openlocfilehash: c96fa846d11947af03faec26dd6de99e0aeec052
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452795"
---
# <a name="creating-the-game1-class"></a>Création de la classe Game1
Comme dans tous les projets Microsoft XNA, la classe Game1 dérive de la classe [Microsoft.Xna.Framework.Game](https://docs.microsoft.com/previous-versions/windows/xna/bb197040%28v%3dxnagamestudio.41%29) qui fournit l’initialisation de base des périphériques graphiques, la logique de jeu et le code de rendu pour les jeux XNA. La classe Game1 est relativement simple dans la mesure où la majeure partie du travail est effectuée dans les classes GamePiece et GamePieceCollection.  
  
## <a name="creating-the-code"></a>Création du code  
 Les membres privés de la classe se composent d’un objet **GamePieceCollection** pour contenir les pièces de jeu, d’un objet [GraphicsDeviceManager](https://docs.microsoft.com/previous-versions/windows/xna/bb197317%28v%3dxnagamestudio.41%29) et d’un objet [SpriteBatch](https://docs.microsoft.com/previous-versions/windows/xna/bb199034%28v%3dxnagamestudio.41%29) pour le rendu des pièces de jeu.  
  
 [!code-csharp[ManipulationXNA#_Game1_PrivateMembers](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_privatemembers)]  
  
 Pendant l'initialisation du jeu, ces objets sont instanciés.  
  
 [!code-csharp[ManipulationXNA#_Game1_ConstructorInitialize](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_constructorinitialize)]  
  
 Quand la méthode [LoadContent](https://docs.microsoft.com/previous-versions/windows/xna/bb975766%28v%3dxnagamestudio.41%29) est appelée, les pièces de jeu sont créées et assignées à l’objet **GamePieceCollection**. Il existe deux types de pièces de jeu. Le facteur d'échelle pour les pièces est légèrement modifié pour créer des pièces plus petites et d'autres plus grandes.  
  
 [!code-csharp[ManipulationXNA#_Game1_LoadContent](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_loadcontent)]  
  
 La méthode [Update](https://docs.microsoft.com/previous-versions/windows/xna/bb199616%28v%3dxnagamestudio.41%29) est appelée plusieurs fois par XNA Framework pendant l’exécution du jeu. La méthode [Update](https://docs.microsoft.com/previous-versions/windows/xna/bb199616%28v%3dxnagamestudio.41%29) appelle les méthodes **ProcessInertia** et **UpdateFromMouse** dans la collection de pièces de jeu. Ces méthodes sont décrites dans [Création de la classe GamePieceCollection](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md).  
  
 [!code-csharp[ManipulationXNA#_Game1_UpdateGame](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_updategame)]  
  
 La méthode [Draw](https://docs.microsoft.com/previous-versions/windows/xna/bb196422%28v%3dxnagamestudio.41%29) est également appelée plusieurs fois par XNA Framework pendant l’exécution du jeu. La méthode [Draw](https://docs.microsoft.com/previous-versions/windows/xna/bb196422%28v%3dxnagamestudio.41%29) effectue le rendu des pièces de jeu en appelant la méthode **Draw** de l’objet **GamePieceCollection**. Cette méthode est décrite dans [Création de la classe GamePieceCollection](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md).  
  
 [!code-csharp[ManipulationXNA#_Game1_DrawGame](../../../samples/snippets/csharp/VS_Snippets_Misc/manipulationxna/cs/game1.cs#_game1_drawgame)]  
  
## <a name="see-also"></a>Voir aussi  
 [Manipulations et inertie](../../../docs/framework/common-client-technologies/manipulations-and-inertia.md)  
 [Utilisation de manipulations et de l'inertie dans une application XNA](../../../docs/framework/common-client-technologies/use-manipulations-and-inertia-in-an-xna-application.md)  
 [Création de la classe GamePiece](../../../docs/framework/common-client-technologies/creating-the-gamepiece-class.md)  
 [Création de la classe GamePieceCollection](../../../docs/framework/common-client-technologies/creating-the-gamepiececollection-class.md)  
 [Listes complètes des codes](../../../docs/framework/common-client-technologies/full-code-listings.md)
