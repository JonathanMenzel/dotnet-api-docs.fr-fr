### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a><span data-ttu-id="c079f-101">List&lt;T&gt;.ForEach peut lever une exception quand vous modifiez un élément de la liste</span><span class="sxs-lookup"><span data-stu-id="c079f-101">List&lt;T&gt;.ForEach can throw exception when modifying list item</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c079f-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c079f-102">Details</span></span>|<span data-ttu-id="c079f-103">À compter de .NET 4.5, un énumérateur <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> lève une exception <xref:System.InvalidOperationException?displayProperty=name> si un élément de la collection appelante est modifié.</span><span class="sxs-lookup"><span data-stu-id="c079f-103">Beginning in .NET 4.5, a <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> enumerator will throw an <xref:System.InvalidOperationException?displayProperty=name> exception if an element in the calling collection is modified.</span></span> <span data-ttu-id="c079f-104">Avant, il ne levait pas d’exception, mais pouvait entraîner des conditions de concurrence.</span><span class="sxs-lookup"><span data-stu-id="c079f-104">Previously, this would not throw an exception but could lead to race conditions.</span></span>|
|<span data-ttu-id="c079f-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c079f-105">Suggestion</span></span>|<span data-ttu-id="c079f-106">Dans l’idéal, le code doit être corrigé de manière à ne pas modifier les listes pendant l’énumération de leurs éléments, car cela n’est jamais une opération sûre.</span><span class="sxs-lookup"><span data-stu-id="c079f-106">Ideally, code should be fixed to not modify lists while enumerating their elements because that is never a safe operation.</span></span> <span data-ttu-id="c079f-107">Cependant, pour restaurer le comportement précédent, une application peut cibler le .NET 4.0.</span><span class="sxs-lookup"><span data-stu-id="c079f-107">To revert to the previous behavior, though, an app may target .NET 4.0.</span></span>|
|<span data-ttu-id="c079f-108">Portée</span><span class="sxs-lookup"><span data-stu-id="c079f-108">Scope</span></span>|<span data-ttu-id="c079f-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c079f-109">Edge</span></span>|
|<span data-ttu-id="c079f-110">Version</span><span class="sxs-lookup"><span data-stu-id="c079f-110">Version</span></span>|<span data-ttu-id="c079f-111">4.5</span><span class="sxs-lookup"><span data-stu-id="c079f-111">4.5</span></span>|
|<span data-ttu-id="c079f-112">Type</span><span class="sxs-lookup"><span data-stu-id="c079f-112">Type</span></span>|<span data-ttu-id="c079f-113">Reciblage</span><span class="sxs-lookup"><span data-stu-id="c079f-113">Retargeting</span></span>|
|<span data-ttu-id="c079f-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="c079f-114">Affected APIs</span></span>|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|
