---
title: Yfirlit fríðindastjórnunar
description: Yfirlit yfir eiginleika stjórnunar fríðinda í Dynamics 365 Human Resources. Bjóddu starfsmönnum þínum framlengda valkosti með auðveldri notkun á netinu.
author: andreabichsel
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd3ffa08b7714d1c6019ea5987dc18ad717720a7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558322"
---
# <a name="benefits-management-overview"></a>Yfirlit fríðindastjórnunar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Til að vera samkeppnishæfur verður þú að bjóða upp á mikið af fríðindum til að laða að og halda bestu starfsmönnum þínum. Til viðbótar við venjulegan ávinning eins og læknisfræðilega og tannlæknaþjónustu, gætirðu líka viljað bjóða upp á stækkaða þjónustu eins og ættleiðingaraðstoð, afþreyingarforrit og fatapeninga. Fríðindastjórnun í Microsoft Dynamics 365 Human Resources veitir þér sveigjanlega lausn sem styður fjölbreytt úrval af kostum. Human Resources felur einnig í sér nothæfa reynslu starfsmanna sem sýnir framboð þitt.

- Auknar fríðindaáætlanir gera þér kleift að búa til og hafa umsjón með einstökum fríðindaáætlunum og styðja flóknar töflur um fríðindahlutfall og ívafin stig. Þú getur auðveldlega búið til fríðindaáætlanir, knippi og sjálfvirkar innritunarreglur til að auðvelda starfsmannaupplifun.
- Flex lánstraust forrit gera þér kleift að styðja við starfslok og aðra atburði í lífinu.
- Víðtækar hæfisreglur tryggja að þú gerir rétt fríðindi tiltæk réttum starfsmönnum.
- Netskráning í fríðindi veitir starfsmönnum þínum auðvelda reynslu.
- Hæf vinnsla á atburði í lífinu styður framtíðarviðburði.

Ef þú vilt fá aðgang að kynningargögnum þarftu að dreifa sandkassumhverfinu þínu á nýjan leik.

> [!NOTE]
> Nú er hægt að sérsníða skjámyndir fríðindastjórnunar. Nú er hægt að bæta sérstilltum reitum sem tengjast tryggingarhlutföllum í skjámyndinni **Tryggingarvalkostur** fyrir fríðindaáætlanir. Frekari upplýsingar um hvernig unnið er með sérstillta reiti er að finna í [Sérstilltir reitir](hr-developer-custom-fields.md).
>
> ![Sérstilltir reitir fríðindastjórnunar](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Virkja fríðindastjórnun

Þetta efnisatriði lýsir því hvernig á að kveikja á eiginleikum í Human Resources. Það segir einnig til um hvaða núgildandi eiginleikum í Human Resources er skipt út fyrir Fríðindastjórnun eða hvaða eiginleikar eru gerðir óvirkir eftir að þú kveikir á Fríðindastjórnun.

> [!IMPORTANT]
> ÞEgar þú hefur virkjað fríðindastjórnun í umhverfi **Framleiðslu** er ekki hægt að afvirkja hana. Við mælum með að virkja og prófa ávinning stjórnunar í umhverfinu **Sandkassi** áður en það er gert kleift í umhverfi **Framleiðslu**. Það er verulegur munur á gamall fríðindavirkni og nýrrar virkni stjórnunar fríðinda sem krefst viðbótaruppsetningar og ætti að prófa áður en þeir eru settir í framleiðslu.

Frekari upplýsingar eru í [Stjórna eiginleikum](hr-admin-manage-features.md).

## <a name="process-overview"></a>Yfirlit ferlis

Ferlið til að stilla fríðindi felur í sér eftirfarandi verk:

1.  Setja upp nauðsynlegar upplýsingar um fríðindi.
2.  Setja upp valfrjálsar upplýsingar um fríðindi.
3.  Uppsetning fríðindaáætlana.
4.  Setja upp sveigjanlegar útgjaldaáætlanir (valfrjálst).
5.  Skilgreina nauðsynlegar upplýsingar um starfsmann.
6.  Skilgreina valfrjálsar upplýsingar um starfsmann.
7.  Vinna úr starfsmönnum til að ákvarða hæfi.
8.  Starfsmenn velja áætlanir í gegnum sjálfsafgreiðslu starfsmanna (valfrjálst).
9.  Staðfesta val á áætlun starfsmanns.
10. Úrvinnsla viðburðar (valfrjálst).
11. Uppfærslur einkunnagjafar (valfrjálst).

## <a name="set-up-required-benefit-information"></a>Setja upp nauðsynlegar upplýsingar um fríðindi

Áður en hægt er að skrá starfsmenn í áætlanirnar verður að setja upp marga þætti:

- **Færibreytur fríðindastjórnunar** – Þessum stillingum er deilt milli fyrirtækja. Hægt er að stilla sjálfgefna ástæðukóða, virkja valkostinn **Fríðindi árslauna**, stilla sjálfgefna greiðslutíðni fyrir nýjar ráðningar og virkja viðburði. Frekari upplýsingar er að finna í [Stilla færibreytur fríðindastjórnunar](hr-benefits-setup-parameters.md).
- **Hæfnisvalkostir persónulegs tengiliðar** – Persónulegir tengiliðir eru einstaklingar sem eru annaðhvort tengdir eða rétthafar áætlana sem eru settar upp. Yfirleitt er um að ræða börn, maka eða félagasamtök. Nánari upplýsingar er að finna í [Grunnstilla hæfnisvalkosti persónulegs tengiliðar](hr-benefits-setup-contact-eligibility-options.md).
- **Tryggingarvalkostir** – Settu upp þær tegundir trygginga sem verða í boði fyrir áætlun. Skilgreindu sérstaklega hvern á að tryggja eða hversu mikil trygging er í boði. Frekari upplýsingar er að finna í [Stofna tryggingarvalkosti](hr-benefits-setup-coverage-options.md).
- **Áætlunargerð** – Settu upp gerðir áætlana sem verða í boði þegar þú stofnar fríðindaáætlun. Dæmi um áætlunargerðir eru m.a. **Tannlækningar**, **Augnlækningar** og **Sparnaður**. Nokkrar mikilvægar stillingar á áætlunargerðinni ákvarða stillingarnar sem eru tiltækar í fríðindaáætluninni. Nánari upplýsingar sjá [Stofna áætlunargerðir](hr-benefits-setup-plan-types.md).
- **Hæfnisreglur** – Hæfnisreglur eru notaðar til að ákvarða hvort starfsmaður uppfylli skilyrði áætlunar. Að minnsta kosti ein hæfnisregla verður að vera tengd við fríðindaáætlun. Frekari upplýsingar er að finna í [Grunnstilla hæfnisreglur og valkosti](hr-benefits-setup-eligibility-rules.md).
- **Greiðslutíðni** – Greiðslutíðni er nauðsynleg þegar fríðindahlutfall er skilgreint. Greiðslutíðnin sem er notuð á verð hjálpar til við að finna upphæðina sem starfsmaðurinn og/eða vinnuveitandinn skulda vikulega, mánaðarlega eða árlega. Frekari upplýsingar er að finna í [Setja upp greiðslutíðni](hr-benefits-setup-payment-frequencies.md).
- **Verð** – Verð skilgreina hvað fríðindi munu kosta fyrir annaðhvort starfsmanninn eða vinnuveitandann. Ef peningum er úthlutað aftur til starfsmanns (til dæmis inneign vegna líkamsræktarkorts) er neikvætt verð slegið inn. Frekari upplýsingar er að finna í [Skilgreina verð](hr-benefits-setup-rates.md).
- **Verðþrep** – Verðþrep er notað þegar verð verður að breytast vegna einhverra skilyrða. Algengasta verðþrepið er einfalt þrep sem byggir á aldri. Hins vegar er einnig hægt að setja upp tvöfalt verðþrep þar sem verðið gæti breyst vegna kyns, aldurs eða annarra skilyrða.
- **Frádrættir** – Frádrættirnir eru í grundvallaratriðum upplýsingar/kóðar í hausnum sem verður flutt í launakerfið til að finna út frádráttinn fyrir fríðindin. Setja verður upp þessa frádrætti vegna þess að þeir eru nauðsynlegir í fríðindaáætluninni. Frekari upplýsingar er að finna í [Skilgreina frádrætti](hr-benefits-setup-deductions.md).
- **Fríðindatímabil** – Fríðindatímabil er tímabilið þegar starfsmenn fá fríðindatryggingu. Það kallast einnig áætlunarár. Opnu skráningartímabilin eru einnig sett upp hér.

## <a name="set-up-optional-benefit-information"></a>Setja upp valfrjálsar upplýsingar um fríðindi

Ekki þarf að setja upp eftirfarandi þætti til að stofna fríðindaáætlun:

- **Áætlunarpakkar** – Áætlunarpakki er safn af fríðindum sem sömu hæfnisreglurnar ná yfir. Til dæmis gætu allir í söludeildinni fengið farsíma.
- **Búnt** – Búnt er fríðindahópur þar sem velja þarf eina áætlun áður möguleikinn á að velja viðbótaráætlanir er tiltækur. Til dæmis gæti áætlun um frádráttarbæran sjúkrakostnað verið sameinað við áætlun heilbrigðissparnaðarreiknings (HSA).
- **Gerðir viðburða** – Viðburðir eru atburðir sem gera kleift að breyta tryggingu starfsmanns. Gerðir viðburða eru tengdir við áætlunargerð. Til dæmis gæti gerð sjúkraáætlunar opnað á breytingar áætlana vegna fæðingar eða ættleiðingar, eða vegna breytingar á hjúskaparstöðu. Hinsvegar gæti gerð tryggingaráætlunar hugsanlega ekki leyft neinar breytingar vegna viðburða. Frekari upplýsingar er að finna í [Skilgreina gerðir viðburða](hr-benefits-setup-life-event-types.md).
- **Biðdagar og biðtími** – Hægt er að stilla biðtíma tryggingar fyrir fríðindaáætlun. Til dæmis gæti nýráðinn starfsmaður skráð sig í 401(k) aðeins eftir að hafa starfað í þrjá mánuði. Í þessu tilviki er biðtíminn þrír mánuðir. Biðdagar eru notaðir á biðtímanum ef hægt er að vinna úr nýjum skráningum og senda þær til þjónustuveitanda aðeins á tilteknum degi mánaðarins. Til dæmis, ef aðeins er hægt að vinna úr 401(k) skráningum á fimmtánda degi mánaðarins, eftir þriggja mánaða starf er biðtíminn sem er settur upp er þrír mánuðir og biðdagurinn sá fimmtándi. Frekari upplýsingar er að finna í [Grunnstilla biðdaga](hr-benefits-setup-waiting-days.md) og [Grunnstilla biðtímabil](hr-benefits-setup-waiting-periods.md).
- **Ástæðukóðar** – Ástæðukóðar eru notaðir til að útskýra af hverju fríðindi kunna að breytast fyrir starfsmann. Frekari upplýsingar er að finna í [Setja upp ástæðukóða](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Uppsetning fríðindaáætlana

Þegar þú setur upp fríðindaáætlun þarftu að ljúka eftirfarandi skrefum áður en hægt er að skrá starfsmenn:

- Úthluta fríðindatímabili.
- Hengja við tryggingarvalkosti.
- Stilla gildir-frá og gildir-til dagsetningu í flipanum **Almennt**.
- Úthluta minnst einni hæfnisreglu.
- Stilltu reitinn **Leyfa/halda áfram með skráningu** í flipanum **Uppsetning**.

Frekari upplýsingar um hvernig á að setja upp fríðindaáætlanir er að finna í [Setja upp fríðindaáætlanir](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Setja upp áætlunarpakka sveigjanlegrar inneignar (valfrjálst)

Þú getur notað áætlunarpakka sveigjanlegrar inneignar til að skrá starfsmenn fyrir fríðindum út frá fyrirframskilgreindum fjölda sveigjanlegrar inneignar. Starfsmenn geta valið hvernig sveigjanlegum inneignum er úthlutað. Ef starfsmenn eru til dæmis þegar tryggðir samkvæmt sjúkratryggingaráætlun maka þurfa þeir ekki að nota inneign sína vegna sjúkratryggingar. Því gætu þeir viljað nota hana fyrir önnur fríðindi í staðinn. Frekari upplýsingar um áætlunarpakka sveigjanlegrar inneignar er að finna í [Setja upp áætlunarpakka sveigjanlegrar inneignar](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Skilgreina nauðsynlegar upplýsingar um starfsmann

Áður en hægt er að skrá starfsmenn í fríðindi þarf að leggja fram tilskildar upplýsingar fyrir þá. Allir starfsmenn verða að vera með stöðu. Þú verður að skrá starfsmenn í launafyrirkomulag fastra launa á upphafsdegi þeirra, eða þeir verða að vera með árleg launatengd fríðindi. Auk þess þarf í hlutanum **Atvinnuupplýsingar** á síðunni **Starfskraftur** að velja gildi í reitnum **Greiðslutíðni fríðinda**.

Ef um er að ræða starfsmann sem fær viðbótarlaun líkt og þóknanir er hægt að bæta við **Árleg launatengd fríðindi** upphæð úr starfsmannafærslu. Human Resources notar **Árleg launatengd fríðindi** upphæð við ákvörðun tryggingaupphæðar, í stað árlega upphæð fastra launa. **Árleg launatengd fríðindi** verða að gilda frá upphafsdagsetningu starfsmanns eða frá upphafi fríðindatímabilsins, hvort sem kemur á eftir. Ef bæði föst laun og upphæð árlegra launatengdra fríðinda eru skráð fyrir starfsmann verða árleg launatengd fríðindi notuð við ákvörðun á tryggingaupphæðum.

## <a name="configure-optional-employee-information"></a>Skilgreina valfrjálsar upplýsingar um starfsmann

Þegar þú býrð til bótaáætlun þar sem notast er við tíðni sem byggist á kyni eða aldri, verður þú að færa inn fæðingardag og kyn starfsmanns til að reikna út fríðindakostnaðinn.

## <a name="process-employees-to-determine-eligibility"></a>Vinna úr starfsmönnum til að ákvarða hæfi

Áður en hægt er að skrá starfsmenn í áætlanir er úrvinnsla á hæfi keyrð til að skera úr um hvaða áætlanir eru gjaldgengar fyrir þá. Hægt er að skoða niðurstöður hæfisferlisins í niðurstöðuskoðun vinnslunnar. Frekari upplýsingar er að finna í [Vinna úr fríðindahæfni](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-via-employee-self-service-optional"></a>Starfsmenn velja áætlanir í gegnum sjálfsafgreiðslu starfsmanna (valfrjálst)

Þegar opin skráning á sér stað, starfsmenn eru nýráðnir eða viðburður á sér stað geta starfsmenn valið eða uppfært fríðindin sín í gegnum sjálfsafgreiðslu starfsmanna. Frekari upplýsingar er að finna í [Skilgreina sjálfsafgreiðslu starfsmanna](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Staðfesta val starfsmannaáætlunar

Staðfesta þarf fríðindin sem starfsmenn velja áður en litið er á starfsmenn sem skráða. Einnig er hægt að velja fríðindi fyrir hönd starfsmanns. Til að velja eða staðfesta fríðindi, á síðu **Starfsmanns**, í flipanum **Fríðindi**, skal velja **Fríðindaáætlanir starfsmanna**. Til að velja eða staðfesta fríðindi fyrir marga starfsmenn skaltu nota síðuna **Magnuppfærsla fríðindaáætlana starfskrafts**.

## <a name="life-event-processing-optional"></a>Úrvinnsla viðburðar (valfrjálst)

Á starfstíma starfsmanns getur hver starfsmaður fyrir sig gengið í gegnum ýmsa viðburði eins og giftingu, breytingu á starfi eða breytingar á fjölskylduhögum. Til að nota viðburði verður að virkja þá á síðunni **Samnýttar færibreytur fyrir mannauð**. Setja upp gerðir viðburða og valkosti viðburða fyrir áætlunargerðir.

Áður en hægt er að vinna úr viðburðum þarf að keyra opna skráningu að minnsta kosti einu sinni meðan tímarammi ráðningar stendur yfir. Í Bandaríkjunum gerist opin skráning yfirleitt einu sinni á ári. Utan Bandaríkjanna gæti opin skráning átt sér stað við ráðningu. Úrvinnsla viðburða krefst þess ekki að starfsmenn velji fríðindaáætlun. Starfsmennirnir verða þó að hafa verið hafðir með í opinni skráningarvinnslu. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Vinna úr viðburðum](hr-benefits-process-life-events.md)
- [Vinna úr breytingum á viðburðum](hr-benefits-process-life-event-changes.md)
- [Vinna úr hæfni viðburðar](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Uppfærslur verðs (valfrjálst)

Stundum breytist verð fríðinda á tímabili áætlunar. Til að uppfæra verð hjá starfsmönnum sem eru þegar skráðir í áætlunina verður að vinna úr verðbreytingunum. Frekari upplýsingar er að finna [Vinna úr breytingum á verði](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
