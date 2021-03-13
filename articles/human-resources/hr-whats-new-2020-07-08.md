---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (08. júlí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 8. júlí 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14dfd925009cb2a9d40044e27f28521ff4d331b7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130398"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (8. júlí 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3382. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="database-logging"></a>Gagnagrunnsskráning

Gagnagrunnsskráning gerir notendum kleift að ákvarða hvaða töflum og reitum á að fylgjast með. Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu. Notið möguleika gagnagrunnsskráningar til að sjá þessar breytingar yfir tíma. Frekari upplýsingar er að finna í [Skilgreina og stjórna gagnagrunnsskráningu](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Grunnstilla heiti á sjálfsafgreiðslu starfsmanns

Í **færibreytum mannauðs** er nú hægt að breyta heiti vinnusvæði fyrir **Sjálfsafgreiðslu starfsmanns** í **Sjálfsafgreiðsla**. Frekari upplýsingar er að finna á [Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Aðgangur að opinni skráningu fríðindastjórnunar utan tímabils

Þessi útgáfa lagar villu þar sem starfsmenn gátu fengið aðgang að opinni skráningu fríðinda utan skráningartímans eða án fríðindaviðburðar. Þar af leiðandi, ef þú þarft að prufukeyra opna skráningu í sjálfsafgreiðslu starfsmanns, þarftu að breyta dagsetningum opinnar skráningar yfir í daginn í dag (eða fyrr) til að gera hana aðgengilega. Hægt er að breyta þessari stillingu undir **Fríðindastjórnun > Reglur og valkostir tímabila**.

## <a name="email-employee-enrollment-confirmation"></a>Senda starfsmanni staðfestingu á skráningu í tölvupósti

Nú er hægt að senda tölvupóst til starfsmanna eftir að hann lýkur fríðindavali sínu. Annaðhvort er hægt að senda sjálfgefin skilaboð eða nota tölvupóstssniðmát fyrirtækis. Þessar stillingar eru undir **Færibreytur í mannauðsstjórnun > Fríðindastjórnun**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Ógilt leyfi birtist enn í væntanlegu fríi á vinnusvæði starfsfólks (441358)

Afturkallað leyfi birtist ekki lengur sem væntanlegt frí á leyfisspjaldinu á vinnusvæðinu **Starfsfólk**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Ekki er hægt að nota eiginleika deildareiningar í PositionV2-einingunni (456486)

Nú er hægt að bæta deild við án þess að stofna tvítekin tengsl.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity ætti aðeins að nota reiknaðan reit fyrir starfslokaáætlanir (459779)

Þegar einingin **PayrollWorkerEnrolledBenefitDetailEntity** er flutt út, ákvarðar útflutningurinn hvort nota eigi reiknaðan reit samkvæmt gengistöflu eða nota reitinn **ContributionAmountCur** á stuðningstöflunni. Rökin sem gagnaeiningin notar nýtir sér gengistöfluna í kringumstæðum þar sem forritið virkar yfirleitt ekki. Þessi rök valda því að útflutningar gagna skilar núllgildi fyrir þennan dálk, því að engin gengistafla útreiknings er til staðar og afurðin leyfir ekki viðskiptavininum að tilgreina slíka.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Ruglingslegar þýðingar á tékknesku í Starfsmannastjórnun og sjálfsafgreiðslu starfsmanna (400276)

Þessi útgáfa leiðréttir þýðingarnar fyrir **Skráasafn fyrirtækis**, **Næsta skráða námskeið**, **Verk** og **Staða**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Taflan WorkCalendarEmployment er ekki með stofnaða og breytta kerfisreiti virka (460171)

Stofnaðir og breyttir reitir kerfisins eru nú virkir í töflunni **WorkCalendarEmployment** í Mannauð.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Undantekning núlltilvísunar fyrir Ráða og bæta við upplýsingum fyrir framtíðarstarfsmenn (455475)

Þessi útgáfa leiðréttir villu (núlltilvísun) í einfaldaðri starfsmannafærslu þegar starfsmaður er ráðinn með því að nota valmöguleikann **Ráða og bæta við upplýsingum**.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Breytingar sem gerðar eru í Dataverse starfsmannaeiningunni koma ekki fram í Mannauðnum (455652)

Breytingar sem gerðar eru á eftirfarandi reitum í einingunni **Starfsmaður** í Dataverse birtast nú í Mannauð:

- **Vinnur heima**
- **Starfsaldursdagsetning**
- **Árleg dagsetning**
- **Upprunaleg ráðningardagsetning**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Rétt launastig er ekki sjálfgefið samkvæmt starfi sem úthlutað er á stöðuna (394136)

Með þessari breytingu verður rétt launastig sjálfgefið samkvæmt færslunum **Gildisdagur** fyrir **Upplýsingar um stöðu** og **Upphafsdagur** í **Úthlutun launafyrirkomulags**.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="mandatory-fields"></a>Áskildir reitir 

Nú er hægt að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources. Þessi eiginleiki krefst **Vistuð yfirlit**.

## <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.

## <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga 

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina. Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök. Frekari upplýsingar má finna á

- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun

Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru. Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun. Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Bæta viðhengjum við frítímabeiðnir

Möguleikinn á því að bæta viðhengjum við samþykktar leyfisbeiðnir er mikilvægur á þessum COVID 19-tímum. Starfsmenn geta nú bætt við þessum viðhengjum. Þeir hafa einnig meiri innsýn í hvernig uppfærslur á leyfisbeiðnum eru gerðar. Frekari upplýsingar er að finna í [Bæta viðhengi við fyrirliggjandi beiðni](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Bæta ástæðukóða við frestun uppsöfnunar 

Ástæðukóðum hefur verið bætt við uppsöfnun í bið.

## <a name="carry-forward-rules"></a>Yfirfærslureglur 

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir

Hægt er að búa til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi. Ógreit leyfi getur verið gerð, en þarf ekki að vera það. Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-eining er í boði fyrir frestun uppsöfnunar 

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="coming-soon"></a>Væntanlegt

## <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)
