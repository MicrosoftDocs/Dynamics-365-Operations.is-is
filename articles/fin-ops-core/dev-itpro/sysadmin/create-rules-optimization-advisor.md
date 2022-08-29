---
title: Stofna reglur fyrir Fínstillingarráðgjöf
description: Þessi grein fjallar um hvernig á að bæta nýjum reglum við hagræðingarráðgjafa.
author: kamaybac
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: a4addc98e3d5496bc8d2fafb3918931da876739f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273918"
---
# <a name="create-rules-for-optimization-advisor"></a>Stofna reglur fyrir Fínstillingarráðgjöf

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að búa til nýjar reglur fyrir **Hagræðingarráðgjafi**. Til dæmis getur þú búið til nýja reglu sem tilgreinir hvaða tilfelli af tilboðsbeiðnum (RFQ) hafa tóman titil. Með því að nota titla á málum er auðveldlega hægt að greina þau og leita að þeim. Á einfaldan hátt sýnir þetta dæmi hverju hægt er að ná fram með fínstillingarreglum. 

*Regla* er könnun á forritsgögnum. Ef ástandið sem reglan metur sé uppfyllt, eru tækifæri til að fínstilla ferla eða betrumbæta gögn búin til. Hægt er að nýta sér möguleikana og, valkvætt, er hægt að mæla áhrif aðgerðanna. 

Til að búa til nýja reglu fyrir **Fínstillingarráðgjafann** skaltu bæta við nýjum klasa sem nær yfir **SelfHealingRule** abstrakt klasann, útfærir **IDiagnosticsRule** viðmótið og er skreyttur af **DiagnosticRule** eigindinni. Klasinn verður einnig að hafa aðferð skreyttri með **DiagnosticsRuleSubscription** eigindinni. Samkvæmt venju er það gert á **opportunityTitle** aðferðinni, sem verður fjallað um síðar. Hægt er að bæta þessum nýja klasa við sérsniðið líkan sem er háð **SelfHealingRules** líkaninu. Í eftirfarandi dæmi er reglan sem er framkvæmd kölluð **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule** abstrakt klasinn hefur abstrakt aðferðir sem verða að vera framkvæmdar í skyldum klösum. Kjarninn er **meta** aðferðin, sem skilar lista yfir tækifærin sem eru tilgreind í reglunum. Tækifæri geta verið fyrir lögaðila eða geta átt við um allt kerfið.

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

Aðferðin sem sýnd er hér fyrir ofan lykkjast yfir fyrirtæki og velur RFQ tilvik með tómum titlum í **findRFQCasesWithEmptyTitle** aðferðinni. Ef að minnsta kosti eitt slíkt tilvik finnst, þá er sérstakt tækifæri fyrir fyrirtæki búið til með **getOpportunityForCompany** aðferðinni. Takið eftir að svæðið **Gögn** í **SelfHealingOpportunity** töflunni er af gerðinni **Geymnir** og getur því innihaldið öll gögn sem skipta máli fyrir rökfræði sem á sérstaklega við þessa reglu. Að stilla **OpportunityDate** við núverandi tímastimpil skráir tímann á nýjasta matinu á tækifærinu.  

Tækifæri geta einnig farið á milli fyrirtækja. Í þessu tilfelli er lykkjan yfir fyrirtækjum ekki nauðsynleg og tækifærið verður að vera búið til með **getOpportunityCrossCompanies** aðferðinni. 

Eftirfarandi kóði sýnir **findRFQCasesWithEmptyTitle** aðferðina, sem skilar kennimerkjum RFQ tilvika sem hafa tóma titla.

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

Tvær aðrar aðferðir sem þarf að koma til framkvæmda eru **opportunityTitle** og **opportunityDetails**. Sú fyrri skilar stuttum titli fyrir tækifærið, sú seinni skilar nákvæmri lýsingu á tækifærinu, sem einnig getur falið í sér gögn.

Titlinum sem var skilað af **opportunityTitle** birtist undir **Fínstillingartækifæri** dálkinum á vinnusvæði **Fínstillingarráðgjafar**. Hann birtist einnig sem haus á hliðarglugganum sem sýnir fleiri upplýsingar um tækifærið. Samkvæmt venju er þessi aðferð skreytt með **DiagnosticRuleSubscription** eigindinni sem tekur við eftirfarandi frumbreytum: 

* **Greiningarsvæði** - Fasttexti af gerðinni **DiagnosticArea** sem lýsir hvaða svæði forritsins reglan tilheyrir, eins og **DiagnosticArea::SCM**. 

* **Regluheit** - Strengur með regluheitinu. Þetta mun birtast undir dálknum fyrir **Regluheiti** í sniði **Greiningu villuleitarreglu** (**DiagnosticsValidationRuleMaintain**). 

* **Keyrslutíðni** - Fasttexti af gerðinni **DiagnosticRunFrequency** sem lýsir hve oft reglan ætti að keyra, eins og **DiagnosticRunFrequency::Daily**. 

* **Lýsing á reglu** - Strengur með nánari lýsingu á reglunni. Þetta mun birtast í **Lýsing á reglu** dálknum á sniði **Greiningu villuleitarreglu** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> **DiagnosticRuleSubscription** eigindin er nauðsynleg svo reglan virki. Venjulega er hún notuð á **opportunityTitle**, en hún getur skreytt hvaða aðferð sem er í klasanum.

Eftirfarandi er dæmi um framkvæmd. Hrástrengir eru notaðir til einföldunar en rétt framkvæmd krefst merkja. 

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

Lýsingin sem er skilað með **opportunityDetails** birtist í hliðarglugganum sem sýnir frekari upplýsingar um tækifærið. Þetta tekur **SelfHealingOpportunity** frumbreytuna, sem er **Gagna** reitur sem hægt er að nota til að veita frekari upplýsingar um tækifærið. Í dæminu skilar aðferðin auðkenni RFQ tilvikanna með tómum titli. 

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

Abstrakt aðferðirnar tvær sem á eftir að framkvæma eru **provideHealingAction** og **securityMenuItem**. 

**provideHealingAction** skilar rétt ef græðandi aðgerð er útveguð, annars skilar það rangt. Ef skilað er rétt, þá verður að framkvæma aðferðina **performAction** eða villa mun koma upp. **PerformAction** aðferðin tekur **SelfHealingOpportunity** frumbreytu, þar sem hægt er að nota gögnin fyrir aðgerðina. Í dæminu opnast aðgerðin **PurchRFQCaseTableListPage**, fyrir handvirka leiðréttingu. 

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

Það fer eftir reglunum, en það getur verið mögulegt að gera sjálfvirkar ráðstafanir með því að nota tækifærisgögnin. Í þessu dæmi gæti kerfið sjálfkrafa búið til titla fyrir RFQ tilvik. 

**securityMenuItem** skilar heiti aðgerðar íí valmyndaratriði þannig að reglan sé aðeins sýnileg notendum sem geta nálgast aðgerð í valmyndaratriði. Öryggi gæti krafist þess að tilgreindar reglur og tækifæri séu aðeins aðgengilegar samþykktum notendum. Í dæminu geta aðeins notendur með aðgang að **PurchRFQCaseTitleAction** skoðað tækifærið. Taktu eftir því að þessi aðgerð valmyndaratriðis var búin til fyrir þetta dæmi og var bætt við sem aðgangsstaður fyrir **PurchRFQCaseTableMaintain** öryggisréttindi. 

> [!NOTE]
> Valmyndaratriðið verður að vera aðgerð valmyndaratriðis svo öryggi starfi rétt. Aðrar gerðir valmyndaratriða líkt og **Yfirlitsvalmyndaratriði** munu ekki starfa rétt.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Eftir að reglan hefur verið þýdd skaltu keyra eftirfarandi verk til að það birtist í notandaviðmótinu (UI).

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

Reglan birtist á sniði **Greiningar villuleitarreglu**, sem er tiltæk hjá **Kerfisstjórnun** > **Reglubundin verkefni** > **Viðhalda greiningum á villuleitarreglu**. Til að meta það, farðu í **Kerfisstjórnun** > **Reglubundin verkefni** > **Áætlun greiningar á villuleitarreglu**, veldu tíðni reglunnar, eins og **Daglega**. Smellið á **Í lagi**. Farðu í **Kerfisstjórnun** > **Fínstillingarráðgjöf** til að skoða nýja tækifærið. 

Eftirfarandi dæmi er kóðabútur með drög að reglu sem inniheldur allar nauðsynlegar aðferðir og eigindi. Hún auðveldar þér að hefjast handa við að skrifa nýjar reglur. Merkin og aðgerðir valmyndaratriða í þessu dæmi eru eingöngu notuð til útskýringar.

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

Fyrir frekari upplýsingar, horfðu á stutta YouTube myndband: [Hagræðingarráðgjafi í Dynamics 365 Finance](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
