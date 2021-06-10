---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (16. september 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 16. september 2020.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057165"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (16. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3557. Tölurnar í sviga við hliðina á sumum eiginleikum vísa í stuðningsnúmer Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Innifalið í þessari útgáfu

-  [Vistuð yfirlit - almennt framboð](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Frekari upplýsingar er að finna í [Vistuð yfirlit](../fin-ops-core/fin-ops/get-started/saved-views.md). 

- Skjámyndin **Stöðuaðgerðir** er með uppfært hnitanet vídda og nýjan svarglugga (469495).

- Ef **Takmarka aðgang að upplýsingum starfsmanna** er stillt á „já“ í **Ítarlegri aðgangur** í **Færibreytur Human Resources** sýnir skjámynd fríðinda núna eingöngu viðeigandi starfsmenn (393384).

- Nýr valmöguleiki fyrir myndun dagatals í einingunni **WorkCalendar** (477055):<br>- Sjálfgefinn lokatími<br>- Sjálfgefinn upphafstími<br>- Er föstudagur vinnudagur<br>- Er mánudagur vinnudagur<br>- Er laugardagur vinnudagur<br>- Er sunnudagur vinnudagur<br>- Er fimmtudagur vinnudagur<br>- Er þriðjudagur vinnudagur<br>- Er miðvikudagur vinnudagur<br>- Auðkenni á frídegi vinnudagatals

- Einingin **LeaveBankTransactionV1** inniheldur núna ástæðukóðann (477823).

- Nú er hægt að vista verkskráningar (492923).

- Gögn er nú birt úr **HCMWorkerContactEntity** (427620).

- Flýtiflipinn **Laun** sýnir nú fyrir starfsmannagerðina verktaki í skjámyndinni **Aðgerðir starfskrafts** (482494).

- Reitirnir **Stig** og **Áætlun** eru nú áskildir ef stillt er á **Föst laun**. Villuboð birtast ef þessir reitir eru skildir eftir auðir (482497).

- Reiturinn **Gerð áætlunar** í **Fríðindi** er nú fellilisti (488768).

- Kerfisstjórar fá nú senda tilkynningu ef sérstilltum reit er eytt úr Human Resources (481408).

- Meðan á uppsagnarferli starfsmanns stendur hagar Human Resources á eðlilegan hátt og breytir ekki völdu fyrirtæki eftir að það virðist læsast (479877). 

- Stjórnendur geta ekki lengur bætt við númeradálki með sérstillingu (485317).

- Stjórnendur geta ekki lengur fjarlægt síu gagnabils úr auðkennisnúmerum sem eru að renna út (485321).

- Þegar reiturinn **Skýrslur til** er auður, birtast upplýsingar um staðsetningu enn þegar músinni er haldið yfir staðsetningunni (433328).

- Starfsmenn geta nú skoðað upplýsingar um fríðindaáætlun í sjálfsafgreiðslu starfsmanna (481676).

- Starfsmenn geta nú séð öll skráð námskeið (429048).

- Nú er hægt að takmarka skoðunarmöguleika fyrir síðuna **Fagvottanir**. Hægt er að takmarka skoðunarmöguleika á núverandi lögaðila eftir stöðu og gerð starfsmanns (451501). 


## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="human-resources-app-in-teams"></a>Forritið „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar má finna á

- [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 1
- [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md) í Human Resources fylgiskjölum

### <a name="human-resources-app-in-teams-preview-features"></a>Forritið Human Resources í forskoðunareiginleikum Teams
 
-  **Tilkynningar**: Sendendur og samþykktaraðilar frítímabeiðni verða látnir vita í forriti Human Resources í Teams. Samþykktaraðilar geta samþykkt eða hafnað beiðnum um frí. Sendendur verða látnir vita hvort beiðnin hafi verið samþykkt eða henni hafnað. Frekari upplýsingar má finna á
   - [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2
   - [Virkja tilkynningar fyrir forritið Human Resources í Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) í Human Resources fylgiskjölum
   - [Kveikja eða slökkva á Teams tilkynningum fyrir einstaka notendur](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) í Human Resources fylgiskjölum
   - [Teams-tilkynningarnar](./hr-teams-leave-app.md#respond-to-teams-notifications) í Human Resources fylgiskjölum
   - [Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources
 
- **Frítímadagatal stjórnanda**: Stjórnendur geta séð samþykkt frí og frí sem bíður ákvörðunar fyrir beina undirmenn í dagatalsyfirliti. Þetta yfirlit veitir auðveldan skilning á því hvenær teymismeðlimir þeirra eru fjarri vinnu. Frekari upplýsingar má finna á
   - [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2
   - [Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig (477004)

Nýr valkostur er nú tiltækur til að staðsetja **Vinnuliðum sem úthlutað er á mig** lista í hægri dálknum á stjórnborðinu. Með þessari breytingu eru allir vinnuliðir og verkefnalistar birtir á sama svæði. Virkjaðu þessa virkni með því að kveikja á **(Forskoðun) Endurbætur á upplifun verkflæðis** í eiginleikastjórnun. Frekari upplýsingar um að kveikja á forútgáfueiginleikum er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

Þessi eiginleiki er einnig fyrir verkflæðisvalkosti sem birtast í skjámyndunum starfsmannaaðgerðir. Verkflæðisvalkostur birtist einnig fyrir ofan flýtiflipa aðgerðarinnar fyrir flýtiaðgang. Frekari upplýsingar má finna á 

- [Endurbætur á upplifun verkflæðis fyrir fyrirtæki og starfsfólk](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) í Dynamics 365 2020 útgáfutímabilsáætlun 2

![Vinnuliðir sem úthlutað er á mig](./media/hr-workflow-work-items-assigned-to-me.png)

![Flýtiaðgangur að verkflæðisatriðum](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Leyfis- og fjarvistadagatal

Í þessari útgáfu eru fleiri dagatalsmöguleikar fyrir frítíma- og fjarvistadagatöl. Fyrir frekari upplýsingar, sjá [Skoða dagatöl hópa og fyrirtækja](./hr-employee-self-service-calendar.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

### <a name="benefits-management-reason-codes"></a>Ástæðukóðar fyrir fríðindastjórnun

Ástæðukóðar fyrir fríðindastjórnun verða brátt sameinaðir við tiltæka ástæðukóða í Human Resources. Ef ástæðukóðar voru stofnaðir í Fríðindastjórnun sem eru yfir 15 stafir að lengd þarf að breyta heiti ástæðukóðans í Fríðindastjórnun **Ástæðukóðar** skjámyndinni þannig að þeir eru 15 stafir eða minna. Þegar búið er að uppfæra heitið mun ástæðukóðinn birtast undir fyrirliggjandi skjámynd ástæðukóða í starfsmannastjórnun. Þessi breyting verður tiltæk í framtíðinni og mun ekki hafa áhrif á fyrirliggjandi virkni.

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
