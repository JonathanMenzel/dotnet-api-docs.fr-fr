### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a><span data-ttu-id="6c4b1-101">Certaines API .NET provoquent des exceptions EntryPointNotFoundExceptions de première chance (gérées)</span><span class="sxs-lookup"><span data-stu-id="6c4b1-101">Some .NET APIs cause first chance (handled) EntryPointNotFoundExceptions</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6c4b1-102">Détails</span><span class="sxs-lookup"><span data-stu-id="6c4b1-102">Details</span></span>|<span data-ttu-id="6c4b1-103">Dans .NET Framework 4.5, un petit nombre de méthodes .NET levaient des exceptions <xref:System.EntryPointNotFoundException?displayProperty=name> de première chance.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-103">In the .NET Framework 4.5, a small number of .NET methods began throwing first chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.</span></span> <span data-ttu-id="6c4b1-104">Ces exceptions étaient gérées dans le .NET Framework, mais pouvaient arrêter l’automatisation des tests, car celle-ci ne s’attendait pas à des exceptions de première chance.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-104">These exceptions were handled within the .Net Framework, but could break test automation that did not expect the first chance exceptions.</span></span> <span data-ttu-id="6c4b1-105">Ces mêmes API provoquent l’arrêt de certaines exécutions ApiVerifier lorsque HighVersionLie est activé.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-105">These same APIs break some ApiVerifier scenarios when HighVersionLie is enabled.</span></span>|
|<span data-ttu-id="6c4b1-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="6c4b1-106">Suggestion</span></span>|<span data-ttu-id="6c4b1-107">Vous pouvez éviter ce problème en effectuant une mise à niveau vers .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-107">This bug can be avoided by upgrading to .NET Framework 4.5.1.</span></span> <span data-ttu-id="6c4b1-108">Vous pouvez aussi mettre à jour le code d’automatisation des tests pour que son exécution ne soit pas arrêtée en cas d’exceptions <xref:System.EntryPointNotFoundException?displayProperty=name> de première chance.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-108">Alternatively, test automation can be updated to not break on first-chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.</span></span>|
|<span data-ttu-id="6c4b1-109">Portée</span><span class="sxs-lookup"><span data-stu-id="6c4b1-109">Scope</span></span>|<span data-ttu-id="6c4b1-110">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6c4b1-110">Edge</span></span>|
|<span data-ttu-id="6c4b1-111">Version</span><span class="sxs-lookup"><span data-stu-id="6c4b1-111">Version</span></span>|<span data-ttu-id="6c4b1-112">4.5</span><span class="sxs-lookup"><span data-stu-id="6c4b1-112">4.5</span></span>|
|<span data-ttu-id="6c4b1-113">Type</span><span class="sxs-lookup"><span data-stu-id="6c4b1-113">Type</span></span>|<span data-ttu-id="6c4b1-114">Runtime</span><span class="sxs-lookup"><span data-stu-id="6c4b1-114">Runtime</span></span>|
|<span data-ttu-id="6c4b1-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="6c4b1-115">Affected APIs</span></span>|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|
