---
title: Stofna reglur fyrir Fínstillingarráðgjöf
description: Þetta efnisatriði fjallar um hvernig á að bæta nýjum reglum við Fínstillingarráðgjöfina.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 67e740a1e00c425f0e09b5f0fc960cf2778efd89
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568287"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="95e25-103">Stofna reglur fyrir Fínstillingarráðgjöf</span><span class="sxs-lookup"><span data-stu-id="95e25-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e25-104">Þetta efnisatriði útskýrir hvernig á að stofna nýjar reglur fyrir **Fínstillingarráðgjöf**.</span><span class="sxs-lookup"><span data-stu-id="95e25-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="95e25-105">Til dæmis getur þú búið til nýja reglu sem tilgreinir hvaða tilfelli af tilboðsbeiðnum (RFQ) hafa tóman titil.</span><span class="sxs-lookup"><span data-stu-id="95e25-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="95e25-106">Með því að nota titla á málum er auðveldlega hægt að greina þau og leita að þeim.</span><span class="sxs-lookup"><span data-stu-id="95e25-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="95e25-107">Á einfaldan hátt sýnir þetta dæmi hverju hægt er að ná fram með fínstillingarreglum.</span><span class="sxs-lookup"><span data-stu-id="95e25-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="95e25-108">*Regla* er könnun á forritsgögnum.</span><span class="sxs-lookup"><span data-stu-id="95e25-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="95e25-109">Ef ástandið sem reglan metur sé uppfyllt, eru tækifæri til að fínstilla ferla eða betrumbæta gögn búin til.</span><span class="sxs-lookup"><span data-stu-id="95e25-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="95e25-110">Hægt er að nýta sér möguleikana og, valkvætt, er hægt að mæla áhrif aðgerðanna.</span><span class="sxs-lookup"><span data-stu-id="95e25-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="95e25-111">Til að búa til nýja reglu fyrir **Fínstillingarráðgjafann** skaltu bæta við nýjum klasa sem nær yfir **SelfHealingRule** abstrakt klasann, útfærir **IDiagnosticsRule** viðmótið og er skreyttur af **DiagnosticRule** eigindinni.</span><span class="sxs-lookup"><span data-stu-id="95e25-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="95e25-112">Klasinn verður einnig að hafa aðferð skreyttri með **DiagnosticsRuleSubscription** eigindinni.</span><span class="sxs-lookup"><span data-stu-id="95e25-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="95e25-113">Samkvæmt venju er það gert á **opportunityTitle** aðferðinni, sem verður fjallað um síðar.</span><span class="sxs-lookup"><span data-stu-id="95e25-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="95e25-114">Hægt er að bæta þessum nýja klasa við sérsniðið líkan sem er háð **SelfHealingRules** líkaninu.</span><span class="sxs-lookup"><span data-stu-id="95e25-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="95e25-115">Í eftirfarandi dæmi er reglan sem er framkvæmd kölluð **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="95e25-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="95e25-116">**SelfHealingRule** abstrakt klasinn hefur abstrakt aðferðir sem verða að vera framkvæmdar í skyldum klösum.</span><span class="sxs-lookup"><span data-stu-id="95e25-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="95e25-117">Kjarninn er **meta** aðferðin, sem skilar lista yfir tækifærin sem eru tilgreind í reglunum.</span><span class="sxs-lookup"><span data-stu-id="95e25-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="95e25-118">Tækifæri geta verið fyrir lögaðila eða geta átt við um allt kerfið.</span><span class="sxs-lookup"><span data-stu-id="95e25-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="95e25-119">Aðferðin sem sýnd er hér fyrir ofan lykkjast yfir fyrirtæki og velur RFQ tilvik með tómum titlum í **findRFQCasesWithEmptyTitle** aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="95e25-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="95e25-120">Ef að minnsta kosti eitt slíkt tilvik finnst, þá er sérstakt tækifæri fyrir fyrirtæki búið til með **getOpportunityForCompany** aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="95e25-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="95e25-121">Takið eftir að svæðið **Gögn** í **SelfHealingOpportunity** töflunni er af gerðinni **Geymnir** og getur því innihaldið öll gögn sem skipta máli fyrir rökfræði sem á sérstaklega við þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="95e25-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="95e25-122">Að stilla **OpportunityDate** við núverandi tímastimpil skráir tímann á nýjasta matinu á tækifærinu.</span><span class="sxs-lookup"><span data-stu-id="95e25-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="95e25-123">Tækifæri geta einnig farið á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="95e25-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="95e25-124">Í þessu tilfelli er lykkjan yfir fyrirtækjum ekki nauðsynleg og tækifærið verður að vera búið til með **getOpportunityCrossCompanies** aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="95e25-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="95e25-125">Eftirfarandi kóði sýnir **findRFQCasesWithEmptyTitle** aðferðina, sem skilar kennimerkjum RFQ tilvika sem hafa tóma titla.</span><span class="sxs-lookup"><span data-stu-id="95e25-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="95e25-126">Tvær aðrar aðferðir sem þarf að koma til framkvæmda eru **opportunityTitle** og **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="95e25-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="95e25-127">Sú fyrri skilar stuttum titli fyrir tækifærið, sú seinni skilar nákvæmri lýsingu á tækifærinu, sem einnig getur falið í sér gögn.</span><span class="sxs-lookup"><span data-stu-id="95e25-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="95e25-128">Titlinum sem var skilað af **opportunityTitle** birtist undir **Fínstillingartækifæri** dálkinum á vinnusvæði **Fínstillingarráðgjafar**.</span><span class="sxs-lookup"><span data-stu-id="95e25-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="95e25-129">Hann birtist einnig sem haus á hliðarglugganum sem sýnir fleiri upplýsingar um tækifærið.</span><span class="sxs-lookup"><span data-stu-id="95e25-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="95e25-130">Samkvæmt venju er þessi aðferð skreytt með **DiagnosticRuleSubscription** eigindinni sem tekur við eftirfarandi frumbreytum:</span><span class="sxs-lookup"><span data-stu-id="95e25-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="95e25-131">**Greiningarsvæði** - Fasttexti af gerðinni **DiagnosticArea** sem lýsir hvaða svæði forritsins reglan tilheyrir, eins og **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="95e25-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="95e25-132">**Regluheit** - Strengur með regluheitinu.</span><span class="sxs-lookup"><span data-stu-id="95e25-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="95e25-133">Þetta mun birtast undir dálknum fyrir **Regluheiti** í sniði **Greiningu villuleitarreglu** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="95e25-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="95e25-134">**Keyrslutíðni** - Fasttexti af gerðinni **DiagnosticRunFrequency** sem lýsir hve oft reglan ætti að keyra, eins og **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="95e25-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="95e25-135">**Lýsing á reglu** - Strengur með nánari lýsingu á reglunni.</span><span class="sxs-lookup"><span data-stu-id="95e25-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="95e25-136">Þetta mun birtast í **Lýsing á reglu** dálknum á sniði **Greiningu villuleitarreglu** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="95e25-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="95e25-137">**DiagnosticRuleSubscription** eigindin er nauðsynleg svo reglan virki.</span><span class="sxs-lookup"><span data-stu-id="95e25-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="95e25-138">Venjulega er hún notuð á **opportunityTitle**, en hún getur skreytt hvaða aðferð sem er í klasanum.</span><span class="sxs-lookup"><span data-stu-id="95e25-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="95e25-139">Eftirfarandi er dæmi um framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="95e25-139">The following is an example implementation.</span></span> <span data-ttu-id="95e25-140">Hrástrengir eru notaðir til einföldunar en rétt framkvæmd krefst merkja.</span><span class="sxs-lookup"><span data-stu-id="95e25-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="95e25-141">Lýsingin sem er skilað með **opportunityDetails** birtist í hliðarglugganum sem sýnir frekari upplýsingar um tækifærið.</span><span class="sxs-lookup"><span data-stu-id="95e25-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="95e25-142">Þetta tekur **SelfHealingOpportunity** frumbreytuna, sem er **Gagna** reitur sem hægt er að nota til að veita frekari upplýsingar um tækifærið.</span><span class="sxs-lookup"><span data-stu-id="95e25-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="95e25-143">Í dæminu skilar aðferðin auðkenni RFQ tilvikanna með tómum titli.</span><span class="sxs-lookup"><span data-stu-id="95e25-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="95e25-144">Abstrakt aðferðirnar tvær sem á eftir að framkvæma eru **provideHealingAction** og **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="95e25-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="95e25-145">**provideHealingAction** skilar rétt ef græðandi aðgerð er útveguð, annars skilar það rangt.</span><span class="sxs-lookup"><span data-stu-id="95e25-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="95e25-146">Ef skilað er rétt, þá verður að framkvæma aðferðina **performAction** eða villa mun koma upp.</span><span class="sxs-lookup"><span data-stu-id="95e25-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="95e25-147">**PerformAction** aðferðin tekur **SelfHealingOpportunity** frumbreytu, þar sem hægt er að nota gögnin fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="95e25-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="95e25-148">Í dæminu opnast aðgerðin **PurchRFQCaseTableListPage**, fyrir handvirka leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="95e25-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="95e25-149">Það fer eftir reglunum, en það getur verið mögulegt að gera sjálfvirkar ráðstafanir með því að nota tækifærisgögnin.</span><span class="sxs-lookup"><span data-stu-id="95e25-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="95e25-150">Í þessu dæmi gæti kerfið sjálfkrafa búið til titla fyrir RFQ tilvik.</span><span class="sxs-lookup"><span data-stu-id="95e25-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="95e25-151">**securityMenuItem** skilar heiti aðgerðar íí valmyndaratriði þannig að reglan sé aðeins sýnileg notendum sem geta nálgast aðgerð í valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="95e25-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="95e25-152">Öryggi gæti krafist þess að tilgreindar reglur og tækifæri séu aðeins aðgengilegar samþykktum notendum.</span><span class="sxs-lookup"><span data-stu-id="95e25-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="95e25-153">Í dæminu geta aðeins notendur með aðgang að **PurchRFQCaseTitleAction** skoðað tækifærið.</span><span class="sxs-lookup"><span data-stu-id="95e25-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="95e25-154">Taktu eftir því að þessi aðgerð valmyndaratriðis var búin til fyrir þetta dæmi og var bætt við sem aðgangsstaður fyrir **PurchRFQCaseTableMaintain** öryggisréttindi.</span><span class="sxs-lookup"><span data-stu-id="95e25-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="95e25-155">Valmyndaratriðið verður að vera aðgerð valmyndaratriðis svo öryggi starfi rétt.</span><span class="sxs-lookup"><span data-stu-id="95e25-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="95e25-156">Aðrar gerðir valmyndaratriða líkt og **Yfirlitsvalmyndaratriði** munu ekki starfa rétt.</span><span class="sxs-lookup"><span data-stu-id="95e25-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="95e25-157">Eftir að reglan hefur verið þýdd skaltu keyra eftirfarandi verk til að það birtist í notandaviðmótinu (UI).</span><span class="sxs-lookup"><span data-stu-id="95e25-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="95e25-158">Reglan birtist á sniði **Greiningar villuleitarreglu**, sem er tiltæk hjá **Kerfisstjórnun** > **Reglubundin verkefni** > **Viðhalda greiningum á villuleitarreglu**.</span><span class="sxs-lookup"><span data-stu-id="95e25-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="95e25-159">Til að meta það, farðu í **Kerfisstjórnun** > **Reglubundin verkefni** > **Áætlun greiningar á villuleitarreglu**, veldu tíðni reglunnar, eins og **Daglega**.</span><span class="sxs-lookup"><span data-stu-id="95e25-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="95e25-160">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95e25-160">Click **OK**.</span></span> <span data-ttu-id="95e25-161">Farðu í **Kerfisstjórnun** > **Fínstillingarráðgjöf** til að skoða nýja tækifærið.</span><span class="sxs-lookup"><span data-stu-id="95e25-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="95e25-162">Eftirfarandi dæmi er kóðabútur með drög að reglu sem inniheldur allar nauðsynlegar aðferðir og eigindi.</span><span class="sxs-lookup"><span data-stu-id="95e25-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="95e25-163">Hún auðveldar þér að hefjast handa við að skrifa nýjar reglur.</span><span class="sxs-lookup"><span data-stu-id="95e25-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="95e25-164">Merkin og aðgerðir valmyndaratriða í þessu dæmi eru eingöngu notuð til útskýringar.</span><span class="sxs-lookup"><span data-stu-id="95e25-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="95e25-165">Nánari upplýsingar má fá með því að horfa á stutt YouTube myndband: [Fínstillingarráðgjöf í Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="95e25-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]