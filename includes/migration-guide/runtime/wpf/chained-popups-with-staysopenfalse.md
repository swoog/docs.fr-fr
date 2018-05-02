### <a name="chained-popups-with-staysopenfalse"></a>Fenêtres contextuelles chaînées avec StaysOpen=False

|   |   |
|---|---|
|Détails|Une fenêtre contextuelle avec StaysOpen=False est supposée se fermer quand vous cliquez en dehors de la fenêtre contextuelle. Quand plusieurs de ces fenêtres contextuelles sont chaînées (c’est-à-dire quand une fenêtre en contient une autre), de nombreux problèmes apparaissaient, notamment :<ul><li>Ouvrez deux niveaux, cliquez en dehors de P2 mais à l’intérieur de P1.  Rien ne se produit.</li><li>Ouvrez deux niveaux, cliquez en dehors de P1.  Les deux fenêtres contextuelles se ferment.</li><li>Ouvrez et fermez les deux niveaux.  Essayez à nouveau d’ouvrir P2.  Rien ne se produit.</li><li>Essayez d’ouvrir trois niveaux.  Vous ne pouvez pas.  (Rien ne se passe ou les deux premiers niveaux se ferment, selon l’endroit où vous cliquez.) Ces cas (et d’autres variantes) fonctionnent désormais comme attendu.</li></ul>|
|Portée|Microsoft Edge|
|Version|4.7.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

