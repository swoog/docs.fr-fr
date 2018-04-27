### <a name="wpf-layout-rounding-of-margins-has-changed"></a>L’arrondi des marges dans la disposition WPF a changé

|   |   |
|---|---|
|Détails|La façon dont les marges sont arrondies, les bordures et l'arrière-plan ont changé. Résultat de cette modification :<ul><li>La largeur ou la hauteur d'éléments peut croître ou diminuer d'un pixel au plus.</li><li>La position d'un objet peut se déplacer d'un pixel au plus.</li><li>Les éléments centrés peuvent être décalés verticalement ou horizontalement d'un pixel au plus.</li></ul>Par défaut, cette nouvelle disposition est activée uniquement pour les applications qui ciblent le .NET. Framework 4.6.|
|Suggestion|Dans la mesure où cette modification tend à éliminer le découpage droit ou inférieur des contrôles WPF dont le PPP est élevé, vous pouvez choisir ce nouveau comportement pour les applications qui ciblent les versions antérieures du .NET Framework, mais qui s’exécutent sur .NET Framework 4.6, en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config : <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>Pour les applications qui ciblent .NET Framework 4.6, vous pouvez faire en sorte que les contrôles WPF soient affichés à l’aide de l’algorithme de disposition en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config : <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|

