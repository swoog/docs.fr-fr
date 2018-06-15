## <a name="introduction"></a>Introduction
Les changements de reciblage affectent les applications qui sont recompilées pour cibler un autre .NET Framework. Elles comprennent :

* Modifications de l'environnement au moment du design. Par exemple, les outils de génération peuvent émettre des avertissements, ce qu'ils ne faisaient pas auparavant.

* Modifications de l'environnement d'exécution. Ces changements affectent uniquement les applications qui ciblent particulièrement le .NET Framework reciblé. Les applications qui ciblent des versions antérieures de .NET Framework se comportent comme elles le faisaient dans ces versions.

Dans les rubriques qui décrivent les changements de reciblage, nous avons classé les éléments individuels en fonction de leur impact, comme suit :

**Majeur** Il s’agit d’un changement important qui affecte un grand nombre d'applications ou qui nécessite de modifier significativement le code.

**Mineur** Il s’agit d’un changement qui affecte un petit nombre d’applications ou qui nécessite peu de modifications du code.

**Cas particulier** Il s’agit d’un changement qui affecte des applications dans des scénarios très spécifiques qui ne sont pas courants.

**Transparent** Il s’agit d’un changement qui n’a pas d’effet visible pour le développeur ou l’utilisateur de l’application. L'application n'a pas besoin d'être modifiée en raison de cette modification.
