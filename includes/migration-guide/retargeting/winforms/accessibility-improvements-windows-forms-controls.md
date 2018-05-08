### <a name="accessibility-improvements-in-windows-forms-controls"></a><span data-ttu-id="5aa56-101">Améliorations apportées aux fonctionnalités d’accessibilité dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5aa56-101">Accessibility improvements in Windows Forms controls</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5aa56-102">Détails</span><span class="sxs-lookup"><span data-stu-id="5aa56-102">Details</span></span>|<span data-ttu-id="5aa56-103">Windows Forms améliore la façon dont il utilise les technologies d’accessibilité pour mieux répondre aux besoins de ses clients.</span><span class="sxs-lookup"><span data-stu-id="5aa56-103">Windows Forms is improving how it works with accessibility technologies to better support Windows Forms customers.</span></span> <span data-ttu-id="5aa56-104">Citons notamment les changements suivants :</span><span class="sxs-lookup"><span data-stu-id="5aa56-104">These include the following changes:</span></span><ul><li><span data-ttu-id="5aa56-105">Changements visant à améliorer l’affichage en mode Contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="5aa56-105">Changes to improve display during High Contrast mode.</span></span></li><li><span data-ttu-id="5aa56-106">Changements visant à améliorer l’expérience dans l’explorateur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="5aa56-106">Changes to improve the property browser experience.</span></span> <span data-ttu-id="5aa56-107">Améliorations apportées à l’explorateur de propriétés. Parmi celles-ci :</span><span class="sxs-lookup"><span data-stu-id="5aa56-107">Property browser improvements include:</span></span></li><li><span data-ttu-id="5aa56-108">Une meilleure navigation au clavier via les différentes fenêtres de sélection de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5aa56-108">Better keyboard navigation through the various drop-down selection windows.</span></span></li><li><span data-ttu-id="5aa56-109">Une réduction des taquets de tabulation inutiles.</span><span class="sxs-lookup"><span data-stu-id="5aa56-109">Reduced unnecessary tab stops.</span></span></li><li><span data-ttu-id="5aa56-110">Des rapports plus élaborés sur les types de contrôles.</span><span class="sxs-lookup"><span data-stu-id="5aa56-110">Better reporting of control types.</span></span></li><li><span data-ttu-id="5aa56-111">Un comportement amélioré du Narrateur.</span><span class="sxs-lookup"><span data-stu-id="5aa56-111">Improved narrator behavior.</span></span></li><li><span data-ttu-id="5aa56-112">Changements visant à implémenter les modèles d’accessibilité de l’interface utilisateur manquants dans les contrôles.</span><span class="sxs-lookup"><span data-stu-id="5aa56-112">Changes to implement missing UI accessibility patterns in controls.</span></span></li></ul>|
|<span data-ttu-id="5aa56-113">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5aa56-113">Suggestion</span></span>|<span data-ttu-id="5aa56-114"><strong>Comment accepter ou refuser ces changements</strong>L’application doit s’exécuter sur le .NET Framework 4.7.1 ou ultérieur pour tirer parti de ces changements.</span><span class="sxs-lookup"><span data-stu-id="5aa56-114"><strong>How to opt in or out of these changes</strong>In order for the application to benefit from these changes, it must run on the .NET Framework 4.7.1 or later.</span></span> <span data-ttu-id="5aa56-115">Pour que l’application bénéficie de ces changements, procédez de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="5aa56-115">The application can benefit from these changes in either of the following ways:</span></span><ul><li><span data-ttu-id="5aa56-116">Recompilez-la pour qu’elle cible le .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="5aa56-116">It is recompiled to target the .NET Framework 4.7.1.</span></span> <span data-ttu-id="5aa56-117">Ces changements d’accessibilité sont activés par défaut sur les applications Windows Forms qui ciblent le .NET Framework 4.7.1 ou ultérieur.</span><span class="sxs-lookup"><span data-stu-id="5aa56-117">These accessibility changes are enabled by default on Windows Forms applications that target the .NET Framework 4.7.1 or later.</span></span></li><li><span data-ttu-id="5aa56-118">Refusez les comportements d’accessibilité hérités en ajoutant le [commutateur AppContext](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier app.config et en lui affectant la valeur <code>false</code>, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5aa56-118">It opts out of the legacy accessibility behaviors by adding the following [AppContext switch](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) to the <code>&lt;runtime&gt;</code> section of the app.config file and setting it to <code>false</code>, as the following example shows.</span></span></li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre><span data-ttu-id="5aa56-119">Si votre application cible le .NET Framework 4.7.1 ou ultérieur et que vous souhaitez conserver le comportement d’accessibilité hérité, choisissez d’utiliser les fonctionnalités d’accessibilité héritées en affectant explicitement à ce commutateur AppContext la valeur <code>true</code>. Pour obtenir une présentation générale d’UI automation, consultez [Vue d’ensemble d’UI Automation](~/docs/framework/ui-automation/ui-automation-overview.md).<strong>Prise en charge des modèles et des propriétés d’UI Automation</strong>Les clients d’accessibilité peuvent tirer parti des nouvelles fonctionnalités d’accessibilité WinForms à l’aide de modèles d’appel publics.</span><span class="sxs-lookup"><span data-stu-id="5aa56-119">Applications that target the .NET Framework 4.7.1 or later and want to preserve the legacy accessibility behavior can opt in to the use of legacy accessibility features by explicitly setting this AppContext switch to <code>true</code>.For an overview of UI automation, see the [UI Automation Overview](~/docs/framework/ui-automation/ui-automation-overview.md).<strong>Added support for UI Automation patterns and properties</strong>Accessibility clients can take advantage of new WinForms accessibility functionality by using common, publicly described invocation patterns.</span></span> <span data-ttu-id="5aa56-120">Ces modèles ne sont pas spécifiques à WinForms.</span><span class="sxs-lookup"><span data-stu-id="5aa56-120">These patterns are not WinForms-specific.</span></span> <span data-ttu-id="5aa56-121">Par exemple, les clients d’accessibilité peuvent appeler la méthode QueryInterface sur l’interface IAccessible (MAAS) pour obtenir une interface IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="5aa56-121">For instance, accessibility clients can call the QueryInterface method on the IAccessible interface (MAAS) to obtain an IServiceProvider interface.</span></span> <span data-ttu-id="5aa56-122">Si cette interface est disponible, les clients peuvent utiliser sa méthode QueryService pour demander une interface IAccessibleEx.</span><span class="sxs-lookup"><span data-stu-id="5aa56-122">If this interface is available, clients can use its QueryService method to request an IAccessibleEx interface.</span></span> <span data-ttu-id="5aa56-123">Pour plus d’informations, consultez [Utilisation d’IAccessibleEx à partir d’un client](https://msdn.microsoft.com/library/windows/desktop/dd561924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5aa56-123">For more information, see [Using IAccessibleEx from a Client](https://msdn.microsoft.com/library/windows/desktop/dd561924.aspx).</span></span> <span data-ttu-id="5aa56-124">À compter du .NET Framework 4.7.1, IServiceProvider et [IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561898.aspx) (le cas échéant) sont disponibles pour les objets d’accessibilité WinForms. Le .NET Framework 4.7.1 ajoute la prise en charge des modèles et des propriétés UI Automation suivants :</span><span class="sxs-lookup"><span data-stu-id="5aa56-124">Starting with the .NET Framework 4.7.1, IServiceProvider and [IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561898.aspx) (where applicable) are available for WinForms accessibility objects.The .NET Framework 4.7.1 adds support for the following UI automation patterns and properties:</span></span><ul><li><span data-ttu-id="5aa56-125">Les contrôles <code>T:System.Windows.Forms.ToolStripSplitButton</code> et <code>T:System.Windows.Forms.ComboBox</code> prennent en charge le [modèle Développer/Réduire](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="5aa56-125">The <code>T:System.Windows.Forms.ToolStripSplitButton</code> and <code>T:System.Windows.Forms.ComboBox</code> controls support the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="5aa56-126">Le contrôle <code>T:System.Windows.Forms.ToolStripMenuItem</code> a une valeur de propriété [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) égale à <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-126">The <code>T:System.Windows.Forms.ToolStripMenuItem</code> control has a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="5aa56-127">Le contrôle <code>T:System.Windows.Forms.ToolStripItem</code> prend en charge la propriété [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) et le [modèle Développer/Réduire](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="5aa56-127">The <code>T:System.Windows.Forms.ToolStripItem</code> control supports the [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) property and [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="5aa56-128">Le contrôle <code>T:System.Windows.Forms.ToolStripDropDownItem</code> prend en charge <xref:System.Windows.Forms.AccessibleEvents> indiquant StateChange et NameChange quand la liste déroulante est développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="5aa56-128">The <code>T:System.Windows.Forms.ToolStripDropDownItem</code> control supports <xref:System.Windows.Forms.AccessibleEvents> indicating StateChange and NameChange when drop down is expanded or collapsed.</span></span></li><li><span data-ttu-id="5aa56-129">Le contrôle <code>T:System.Windows.Forms.ToolStripDropDownButton</code> a une valeur de propriété [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) égale à <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-129">The <code>T:System.Windows.Forms.ToolStripDropDownButton</code> control has a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value of <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="5aa56-130">Le contrôle <code>T:System.Windows.Forms.DataGridViewCheckBoxCell</code> prend en charge le [modèle Basculer](xref:System.Windows.Automation.TogglePattern).</span><span class="sxs-lookup"><span data-stu-id="5aa56-130">The <code>T:System.Windows.Forms.DataGridViewCheckBoxCell</code> control supports the [Toggle Pattern](xref:System.Windows.Automation.TogglePattern).</span></span></li><li><span data-ttu-id="5aa56-131">Les contrôles <code>T:System.Windows.Forms.NumericUpDown</code> et <code>T:System.Windows.Forms.DomainUpDown</code> prennent en charge [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) et ont un [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-spinner-control-type.md) égal à <xref:System.Windows.Automation.ControlType.Spinner?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-131">The <code>T:System.Windows.Forms.NumericUpDown</code> and <code>T:System.Windows.Forms.DomainUpDown</code> controls support the [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) and have a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-spinner-control-type.md) of <xref:System.Windows.Automation.ControlType.Spinner?displayProperty=nameWithType>.</span></span></li></ul><span data-ttu-id="5aa56-132"><strong>Améliorations apportées au contrôle PropertyGrid</strong>Le .NET Framework 4.7.1 ajoute les améliorations suivantes au contrôle PropertyBrowser :</span><span class="sxs-lookup"><span data-stu-id="5aa56-132"><strong>Improvements to the PropertyGrid control</strong>The .NET Framework 4.7.1 adds the following improvements to the PropertyBrowser control:</span></span><ul><li><span data-ttu-id="5aa56-133">Le bouton <strong>Détails</strong>, qui se trouve dans la boîte de dialogue d’erreur qui s’affiche quand l’utilisateur entre une valeur incorrecte dans le contrôle <code>T:System.Windows.Forms.PropertyGrid</code>, prend en charge le [modèle Développer/Réduire](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md), les notifications de changement de nom et d’état, et une propriété [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) avec la valeur <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-133">The <strong>Details</strong> button in the error dialog that is displayed when the user enters an incorrect value in the <code>T:System.Windows.Forms.PropertyGrid</code> control supports the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md), state and name change notifications, and a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property with a value of <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>.</span></span></li><li><span data-ttu-id="5aa56-134">Le volet de messages, qui s’affiche quand le bouton <strong>Détails</strong> de la boîte de dialogue d’erreur est développé, est désormais accessible au moyen du clavier et permet au Narrateur d’annoncer le contenu du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5aa56-134">The message pane displayed when the <strong>Details</strong> button of the error dialog is expanded is now keyboard accessible and allows Narrator to announce the content of the error message.</span></span></li><li><span data-ttu-id="5aa56-135">Le <xref:System.Windows.Forms.AccessibleRole> des lignes dans le contrôle <code>T:System.Windows.Forms.PropertyGrid</code> est passé de &quot;Row&quot; à &quot;Cell&quot;.</span><span class="sxs-lookup"><span data-stu-id="5aa56-135">The <xref:System.Windows.Forms.AccessibleRole> of rows in <code>T:System.Windows.Forms.PropertyGrid</code> control have changed from &quot;Row&quot; to &quot;Cell&quot;.</span></span> <span data-ttu-id="5aa56-136">La cellule est mappée au ControlType UIA &quot;DataItem&quot;, ce qui lui permet de prendre en charge les raccourcis clavier appropriés et les annonces du Narrateur.</span><span class="sxs-lookup"><span data-stu-id="5aa56-136">The cell maps to UIA ControlType &quot;DataItem&quot;, which allows it to support appropriate keyboard shortcuts and Narrator announcements.</span></span></li><li><span data-ttu-id="5aa56-137">Les lignes du contrôle <code>T:System.Windows.Forms.PropertyGrid</code>, qui représentent les éléments d’en-tête quand le contrôle <code>T:System.Windows.Forms.PropertyGrid</code> a une propriété <code>P:System.Windows.Forms.PropertySort</code> dont la valeur est <code>F:System.Windows.Forms.PropertySory.Categorized</code>, ont une valeur de propriété [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) égale à <xref:System.Windows.Automation.ControlType.Button?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-137">The <code>T:System.Windows.Forms.PropertyGrid</code> control rows which represent header items when the <code>T:System.Windows.Forms.PropertyGrid</code> control has a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> have a [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) property value of <xref:System.Windows.Automation.ControlType.Button?displayProperty=nameWithType></span></span></li><li><span data-ttu-id="5aa56-138">Les lignes du contrôle <code>T:System.Windows.Forms.PropertyGrid</code>, qui représentent les éléments d’en-tête quand le contrôle <code>T:System.Windows.Forms.PropertyGrid</code> a une propriété <code>P:System.Windows.Forms.PropertySort</code> dont la valeur est <code>F:System.Windows.Forms.PropertySory.Categorized</code>, prennent en charge le [modèle Développer/Réduire](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="5aa56-138">The <code>T:System.Windows.Forms.PropertyGrid</code> control rows which represent header items when the <code>T:System.Windows.Forms.PropertyGrid</code> control has a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> support the [Expand/Collapse pattern](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md).</span></span></li><li><span data-ttu-id="5aa56-139">Navigation au clavier améliorée entre la grille et de la barre d’outils située au-dessus.</span><span class="sxs-lookup"><span data-stu-id="5aa56-139">Improved keyboard navigation between the grid and the ToolBar above it.</span></span> <span data-ttu-id="5aa56-140">Le fait d’appuyer sur &quot;Maj+Tab&quot; sélectionne désormais le premier bouton de la barre d’outils, et non la barre d’outils entière.</span><span class="sxs-lookup"><span data-stu-id="5aa56-140">Pressing &quot;Shift-Tab&quot; now selects the first ToolBar button, instead of the whole ToolBar</span></span></li><li><span data-ttu-id="5aa56-141">Les contrôles <code>T:System.Windows.Forms.PropertyGrid</code> affichés en mode Contraste élevé dessinent désormais un rectangle de focus autour du bouton de barre d’outils qui correspond à la valeur de propriété <code>P:System.Windows.Forms.PropertySort</code> actuelle.</span><span class="sxs-lookup"><span data-stu-id="5aa56-141"><code>T:System.Windows.Forms.PropertyGrid</code> controls displayed in High Contrast mode will now draw a focus rectangle around the ToolBar button which corresponds to the current <code>P:System.Windows.Forms.PropertySort</code> property value.</span></span></li><li><span data-ttu-id="5aa56-142">Les contrôles <code>T:System.Windows.Forms.PropertyGrid</code> affichés en mode Contraste élevé et dont la propriété <code>P:System.Windows.Forms.PropertySort</code> est définie avec la valeur <code>F:System.Windows.Forms.PropertySory.Categorized</code> affichent désormais l’arrière-plan des en-têtes de catégorie dans une couleur très contrastée.</span><span class="sxs-lookup"><span data-stu-id="5aa56-142"><code>T:System.Windows.Forms.PropertyGrid</code> controls displayed in High Contrast mode and with a <code>P:System.Windows.Forms.PropertySort</code> property set to <code>F:System.Windows.Forms.PropertySory.Categorized</code> will now display the background of category headers in a highly contrasting color.</span></span></li><li><span data-ttu-id="5aa56-143">Les contrôles <code>T:System.Windows.Forms.PropertyGrid</code> permettent de mieux distinguer les éléments de barre d’outils ayant le focus de ceux qui indiquent la valeur actuelle de la propriété <code>P:System.Windows.Forms.PropertySort</code>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-143"><code>T:System.Windows.Forms.PropertyGrid</code> controls better differentiates between ToolBar items with focus and the ToolBar items which indicate the current value of the <code>P:System.Windows.Forms.PropertySort</code> property.</span></span> <span data-ttu-id="5aa56-144">Ce correctif se compose de deux changements : l’un visant le mode Contraste élevé et l’autre les scénarios n’utilisant pas ce mode.</span><span class="sxs-lookup"><span data-stu-id="5aa56-144">This fix consists of a High Contrast change and a change for non-High Contrast scenarios.</span></span></li><li><span data-ttu-id="5aa56-145">Les éléments de barre d’outils du contrôle <code>T:System.Windows.Forms.PropertyGrid</code>, qui indiquent la valeur actuelle de la propriété <code>P:System.Windows.Forms.PropertySort</code>, prennent en charge le [modèle Basculer](xref:System.Windows.Automation.TogglePattern).</span><span class="sxs-lookup"><span data-stu-id="5aa56-145"><code>T:System.Windows.Forms.PropertyGrid</code> control ToolBar items which indicates the current value of the <code>P:System.Windows.Forms.PropertySort</code> property support the [Toggle Pattern](xref:System.Windows.Automation.TogglePattern).</span></span></li><li><span data-ttu-id="5aa56-146">Prise en charge améliorée du Narrateur pour distinguer l’alignement sélectionné dans le sélecteur d’alignement.</span><span class="sxs-lookup"><span data-stu-id="5aa56-146">Improved Narrator support for distinguishing the selected alignment in the Alignment Picker.</span></span></li><li><span data-ttu-id="5aa56-147">Quand un contrôle <code>T:System.Windows.Forms.PropertyGrid</code> vide est affiché sur un formulaire, il reçoit désormais le focus. Ce n’était pas le cas avant.</span><span class="sxs-lookup"><span data-stu-id="5aa56-147">When an empty <code>T:System.Windows.Forms.PropertyGrid</code> control is displayed on a form, it will now receive focus where previously it would not.</span></span></li></ul><span data-ttu-id="5aa56-148"><strong>Utilisation des couleurs définies par le système d’exploitation dans les thèmes à contraste élevé</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-148"><strong>Use of OS-defined colors in High Contrast themes</strong></span></span><ul><li><span data-ttu-id="5aa56-149">Les contrôles <code>T:System.Windows.Forms.Button</code> et <code>T:System.Windows.Forms.CheckBox</code> dont le <code>P:System.Windows.Forms.Control.FlatStyle</code> est défini avec la valeur <xref:System.Windows.Forms.FlatStyle.System?displayProperty=nameWithType>, le style par défaut, utilisent désormais les couleurs définies par le système d’exploitation dans le thème à contraste élevé quand celui-ci est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5aa56-149"><code>T:System.Windows.Forms.Button</code> and <code>T:System.Windows.Forms.CheckBox</code> controls with <code>P:System.Windows.Forms.Control.FlatStyle</code> set to <xref:System.Windows.Forms.FlatStyle.System?displayProperty=nameWithType>, which is the default style, now use OS-defined colors in High Contrast theme when selected.</span></span> <span data-ttu-id="5aa56-150">Avant, les couleurs du texte et de l’arrière-plan n’étaient pas contrastées et étaient difficiles à lire.</span><span class="sxs-lookup"><span data-stu-id="5aa56-150">Previously, text and background colors were not contrasting and were hard to read.</span></span></li><li><span data-ttu-id="5aa56-151">Les contrôles <code>T:System.Windows.Forms.Button</code>, <code>T:System.Windows.Forms.CheckBox</code>, <code>T:System.Windows.Forms.RadioButton</code>, <code>T:System.Windows.Forms.Label</code>, <code>T:System.Windows.Forms.LinkLabel</code> et <code>T:System.Windows.Forms.GroupBox</code> dont le <code>P:System.Windows.Forms.Control.Enabled</code> est défini avec la valeur <em>false</em> utilisaient une couleur ombrée pour afficher le texte dans les thèmes à contraste élevé, ce qui aboutissait à un faible contraste par rapport à l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5aa56-151"><code>T:System.Windows.Forms.Button</code>, <code>T:System.Windows.Forms.CheckBox</code>, <code>T:System.Windows.Forms.RadioButton</code>, <code>T:System.Windows.Forms.Label</code>, <code>T:System.Windows.Forms.LinkLabel</code> and <code>T:System.Windows.Forms.GroupBox</code> with<code>P:System.Windows.Forms.Control.Enabled</code> set to <em>false</em>, used a shaded color to render text in High Contrast themes, resulting in low contrast against the background.</span></span> <span data-ttu-id="5aa56-152">Ces contrôles utilisent à présent la couleur &quot;Texte désactivé&quot; définie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5aa56-152">Now these controls use &quot;Disabled Text&quot; color defined by the OS.</span></span> <span data-ttu-id="5aa56-153">Ce correctif s’applique aux contrôles dont la propriété <code>P:System.Windows.Forms.Control.FlatStyle</code> est définie avec une valeur autre que <code>F:System.Windows.Forms.FlatStyle.System</code>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-153">This fix applies to controls with <code>P:System.Windows.Forms.Control.FlatStyle</code> property set to a value other than <code>F:System.Windows.Forms.FlatStyle.System</code>.</span></span> <span data-ttu-id="5aa56-154">Ces derniers contrôles sont affichés par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5aa56-154">The latter controls are rendered by the OS.</span></span></li><li><span data-ttu-id="5aa56-155"><code>T:System.Windows.Forms.DataGridView</code> affiche maintenant un rectangle visible autour du contenu de la cellule qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="5aa56-155"><code>T:System.Windows.Forms.DataGridView</code> now renders a visible rectangle around the content of the cell which has the current focus.</span></span> <span data-ttu-id="5aa56-156">Ce rectangle était invisible dans certains thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="5aa56-156">Previously, this was not visible in certain High Contrast themes.</span></span></li><li><span data-ttu-id="5aa56-157">Les contrôles <code>T:System.Windows.Forms.ToolStripMenuItem</code> dont la propriété <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> a la valeur <em>false</em> utilisent maintenant la couleur &quot;Texte désactivé&quot; définie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5aa56-157"><code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> property set to <em>false</em> now use the &quot;Disabled Text&quot; color defined by the OS.</span></span></li><li><span data-ttu-id="5aa56-158">Les contrôles <code>T:System.Windows.Forms.ToolStripMenuItem</code> dont la propriété <code>P:System.Windows.Forms.ToolStripItem.Checked</code> a la valeur <em>true</em> affichent maintenant la coche associée dans une couleur système contrastée.</span><span class="sxs-lookup"><span data-stu-id="5aa56-158"><code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Checked</code> property set to <em>true</em> now render the associated check mark in a contrasting system color.</span></span>  <span data-ttu-id="5aa56-159">Avant, la couleur de la coche n’était pas suffisamment contrastée et était invisible dans les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="5aa56-159">Previously the check mark color was not contrasting enough and not visible in High Contrast themes.</span></span></li></ul><span data-ttu-id="5aa56-160">REMARQUE : Les valeurs de certaines couleurs système à contraste élevé ont changé dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5aa56-160">NOTE: Windows10 has changed values for some high contrast system colors.</span></span> <span data-ttu-id="5aa56-161">Windows Forms Framework est basé sur le framework Win32.</span><span class="sxs-lookup"><span data-stu-id="5aa56-161">Windows Forms Framework is based on the Win32 framework.</span></span> <span data-ttu-id="5aa56-162">Pour une expérience optimale, procédez à une exécution sur la dernière version de Windows et choisissez les derniers changements du système d’exploitation en ajoutant un fichier app.manifest dans une application de test et en décommentant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="5aa56-162">For the best experience, run on the latest version of Windows and opt in to the latest OS changes by adding an app.manifest file in a test application and uncommenting the following code:</span></span><pre><code>&lt;!-- Windows 10 --&gt;&#13;&#10;&lt;supportedOS Id=&quot;{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}&quot; /&gt;&#13;&#10;</code></pre><span data-ttu-id="5aa56-163"><strong>Navigation au clavier améliorée</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-163"><strong>Improved keyboard navigation</strong></span></span><ul><li><span data-ttu-id="5aa56-164">Quand le <code>P:System.Windows.Forms.ComboBox.DropDownStyle</code> d’un contrôle <code>T:System.Windows.Forms.ComboBox</code> a la valeur <code>F:System.Windows.Forms.DropDownStyle.DropDownList</code> et qu’il s’agit du premier contrôle dans l’ordre de tabulation sur le formulaire, un rectangle de focus apparaît désormais quand le formulaire parent est ouvert à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="5aa56-164">When a <code>T:System.Windows.Forms.ComboBox</code> control has <code>P:System.Windows.Forms.ComboBox.DropDownStyle</code> set to <code>F:System.Windows.Forms.DropDownStyle.DropDownList</code> and is the first control in the tab order on the form, it now displays a focus rectangle when the parent form is opened using the keyboard.</span></span> <span data-ttu-id="5aa56-165">Avant ce changement, le focus clavier était sur ce contrôle, mais aucun indicateur de focus n’était affiché.</span><span class="sxs-lookup"><span data-stu-id="5aa56-165">Before this change, keyboard focus was on this control, but a focus indicator was not rendered.</span></span></li></ul><span data-ttu-id="5aa56-166"><strong>Prise en charge améliorée du Narrateur</strong></span><span class="sxs-lookup"><span data-stu-id="5aa56-166"><strong>Improved Narrator support</strong></span></span><ul><li><span data-ttu-id="5aa56-167">Le contrôle <code>T:System.Windows.Forms.MonthCalendar</code> prend désormais en charge les technologies d’assistance pour accéder au contrôle, notamment la possibilité pour le Narrateur de lire la valeur du contrôle, ce qui n’était pas possible avant.</span><span class="sxs-lookup"><span data-stu-id="5aa56-167">The <code>T:System.Windows.Forms.MonthCalendar</code> control has added support for assistive technologies to access the control, including the ability for Narrator to read the value of the control when previously it could not.</span></span></li><li><span data-ttu-id="5aa56-168">Le contrôle <code>T:System.Windows.Forms.CheckedListBox</code> avertit désormais le Narrateur quand la propriété <code>P:System.Windows.Forms.CheckState</code> change.</span><span class="sxs-lookup"><span data-stu-id="5aa56-168">The <code>T:System.Windows.Forms.CheckedListBox</code> control now notifies Narrator when the <code>P:System.Windows.Forms.CheckState</code> property has been changed.</span></span> <span data-ttu-id="5aa56-169">Le Narrateur ne recevait aucune notification, et les utilisateurs n’étaient pas informés de la mise à jour de <code>P:System.Windows.Forms.CheckState</code>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-169">Previously, Narrator did not recieve notification and as a result users would not be informed that the <code>P:System.Windows.Forms.CheckState</code> had been updated.</span></span></li><li><span data-ttu-id="5aa56-170">Le contrôle <code>T:System.Windows.Forms.LinkLabel</code> notifie le Narrateur du texte présent dans le contrôle de manière différente.</span><span class="sxs-lookup"><span data-stu-id="5aa56-170">The <code>T:System.Windows.Forms.LinkLabel</code> control has changed the way it notifies Narrator of the text of in the control.</span></span> <span data-ttu-id="5aa56-171">Avant, le Narrateur annonçait ce texte à deux reprises et lisait les symboles &quot; &amp; &quot; comme du texte réel, alors qu’ils n’étaient pas visibles.</span><span class="sxs-lookup"><span data-stu-id="5aa56-171">Previously, Narrator announced this text twice and read &quot;&amp;&quot; symbols as real text even though they are not visible to a user.</span></span> <span data-ttu-id="5aa56-172">Le texte en double a été supprimé des annonces du Narrateur, ainsi que les symboles &quot;&amp;&quot; inutiles.</span><span class="sxs-lookup"><span data-stu-id="5aa56-172">The duplicated text was removed from the Narrator announcements, as well as unnecessary &quot;&amp;&quot; symbols.</span></span></li><li><span data-ttu-id="5aa56-173">Les types de contrôle <code>T:System.Windows.Forms.DataGridViewCell</code> signalent désormais correctement l’état en lecture seule au Narrateur et à d’autres technologies d’assistance.</span><span class="sxs-lookup"><span data-stu-id="5aa56-173">The <code>T:System.Windows.Forms.DataGridViewCell</code> control types now correctly report the read-only status to Narrator and other assistive technologies.</span></span></li><li><span data-ttu-id="5aa56-174">Le Narrateur peut désormais lire le menu système des fenêtres enfants dans les applications à [interface multidocument](~/docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5aa56-174">Narrator is now able to read the System Menu of child windows in [Multiple-Document Interface](~/docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md) applications.</span></span></li><li><span data-ttu-id="5aa56-175">Le Narrateur peut désormais lire les contrôles <code>T:System.Windows.Forms.ToolStripMenuItem</code> dont la propriété <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> a la valeur <em>false</em>.</span><span class="sxs-lookup"><span data-stu-id="5aa56-175">Narrator is now able to read <code>T:System.Windows.Forms.ToolStripMenuItem</code> controls with a <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> property set to <em>false</em>.</span></span> <span data-ttu-id="5aa56-176">Avant, le Narrateur ne pouvait pas lire le contenu des éléments de menu désactivés.</span><span class="sxs-lookup"><span data-stu-id="5aa56-176">Previously, Narrator was unable to focus on disabled menu items to read hte content.</span></span></li></ul>|
|<span data-ttu-id="5aa56-177">Portée</span><span class="sxs-lookup"><span data-stu-id="5aa56-177">Scope</span></span>|<span data-ttu-id="5aa56-178">Majeur</span><span class="sxs-lookup"><span data-stu-id="5aa56-178">Major</span></span>|
|<span data-ttu-id="5aa56-179">Version</span><span class="sxs-lookup"><span data-stu-id="5aa56-179">Version</span></span>|<span data-ttu-id="5aa56-180">4.7.1</span><span class="sxs-lookup"><span data-stu-id="5aa56-180">4.7.1</span></span>|
|<span data-ttu-id="5aa56-181">Type</span><span class="sxs-lookup"><span data-stu-id="5aa56-181">Type</span></span>|<span data-ttu-id="5aa56-182">Reciblage</span><span class="sxs-lookup"><span data-stu-id="5aa56-182">Retargeting</span></span>|
|<span data-ttu-id="5aa56-183">API affectées</span><span class="sxs-lookup"><span data-stu-id="5aa56-183">Affected APIs</span></span>|<ul><li><xref:System.Windows.Forms.ToolStripDropDownButton.CreateAccessibilityInstance?displayProperty=nameWithType></li><li><xref:System.Windows.Forms.DomainUpDown.DomainUpDownAccessibleObject.Name?displayProperty=nameWithType></li><li>[<span data-ttu-id="5aa56-184">MonthCalendar.AccessibilityObject</span><span class="sxs-lookup"><span data-stu-id="5aa56-184">MonthCalendar.AccessibilityObject</span></span>](xref:System.Windows.Forms.Control.AccessibilityObject)</li></ul>|
