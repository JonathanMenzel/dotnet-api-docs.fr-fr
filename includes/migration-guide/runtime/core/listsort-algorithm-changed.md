### <a name="listsort-algorithm-changed"></a><span data-ttu-id="c9120-101">Algorithme List.Sort modifié</span><span class="sxs-lookup"><span data-stu-id="c9120-101">List.Sort algorithm changed</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c9120-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c9120-102">Details</span></span>|<span data-ttu-id="c9120-103">À compter de .NET Framework 4.5, l’algorithme de tri de <xref:System.Collections.Generic.List%601?displayProperty=name> a changé (pour correspondre à un tri approfondi au lieu d’un tri rapide).</span><span class="sxs-lookup"><span data-stu-id="c9120-103">Beginning in .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>'s sort algorithm has changed (to be an introspective sort instead of a quick sort).</span></span> <span data-ttu-id="c9120-104">Le tri de <xref:System.Collections.Generic.List%601?displayProperty=name> n’a jamais été stable, mais cette modification peut aboutir à des tris instables dans le cadre de différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="c9120-104"><xref:System.Collections.Generic.List%601?displayProperty=name>'s sort has never been stable, but this change may cause different scenarios to sort in unstable ways.</span></span> <span data-ttu-id="c9120-105">Cela signifie simplement que des éléments équivalents peuvent être triés dans des ordres différents lors des appels suivants de l’API.</span><span class="sxs-lookup"><span data-stu-id="c9120-105">That simply means that equivalent items may sort in different orders in subsequent calls of the API.</span></span>|
|<span data-ttu-id="c9120-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c9120-106">Suggestion</span></span>|<span data-ttu-id="c9120-107">Comme l’ancien algorithme de tri était également instable (de manière légèrement différente, toutefois), aucun code ne doit dépendre du tri dans un ordre particulier des éléments équivalents.</span><span class="sxs-lookup"><span data-stu-id="c9120-107">Because the old sort algorithm was also unstable (though in slightly different ways), there should be no code that depends on equivalent items always sorting in a particular order.</span></span> <span data-ttu-id="c9120-108">Si des instances de code présentent cette dépendance et réussissent avec l’ancien comportement, ce code doit être mis à jour pour utiliser un comparateur qui va trier de façon déterministe les éléments dans l’ordre souhaité.</span><span class="sxs-lookup"><span data-stu-id="c9120-108">If there are instances of code depending upon that and being lucky with the old behavior, that code should be updated to use a comparer that will deterministically sort the items in the desired order.</span></span>|
|<span data-ttu-id="c9120-109">Portée</span><span class="sxs-lookup"><span data-stu-id="c9120-109">Scope</span></span>|<span data-ttu-id="c9120-110">Transparent</span><span class="sxs-lookup"><span data-stu-id="c9120-110">Transparent</span></span>|
|<span data-ttu-id="c9120-111">Version</span><span class="sxs-lookup"><span data-stu-id="c9120-111">Version</span></span>|<span data-ttu-id="c9120-112">4.5</span><span class="sxs-lookup"><span data-stu-id="c9120-112">4.5</span></span>|
|<span data-ttu-id="c9120-113">Type</span><span class="sxs-lookup"><span data-stu-id="c9120-113">Type</span></span>|<span data-ttu-id="c9120-114">Runtime</span><span class="sxs-lookup"><span data-stu-id="c9120-114">Runtime</span></span>|
|<span data-ttu-id="c9120-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="c9120-115">Affected APIs</span></span>|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|
