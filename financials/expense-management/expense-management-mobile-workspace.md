---
title: "Kostnaðarstýring fartækja vinnusvæði"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Kostnaðarstýring. Þessi vinnusvæði gerir notendum kleift að ná í kvittun, sem hægt er að tengja við kostnaðarskýrslu síðar. Notendur geta einnig með skjótum hætti búið til kostnaðarlínu með því að nota viðhengda kvittun, og búa til og hafa umsjón með kostnaðarskýrslum þeirra."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: 2dd3db95eb741c37dd8a50c397cb4c9494599250
ms.openlocfilehash: 993586b1fb46c21d2b68a6060ab897c8ccc76a6c
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="expense-management-mobile-workspace"></a>Fartækjavinnusvæði útgjaldastýringar

[!include[banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Kostnaðarstýring**. Þessi vinnusvæði gerir notendum kleift að ná í kvittun, sem hægt er að tengja við kostnaðarskýrslu síðar. Notendur geta einnig með skjótum hætti búið til kostnaðarlínu með því að nota viðhengda kvittun, og búa til og hafa umsjón með kostnaðarskýrslum þeirra. Þar að auki geta samþykkjendur notað fartækjavinnusvæðið **Kostnaðarstýring** til að skoða kostnaðarskýrslur sem þeim er úthlutað, og annaðhvort samþykkt eða hafnað þeim.


Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations.


## <a name="overview"></a>Yfirlit

Mörg fyrirtæki þurfa afrit af kvittun í viðhengi, sem sýnir útgjöld í ferðalög eða viðskipti sem tengjast kostnaðarskýrsluna sem starfsmaður sendi til að fá endurgreiðslu. **Útgjaldastjórnun** fartækjasvæðið gerir notendum kleift að stofna nýja færslulínur í fartæki að hans vali með því að nota í viðhengi mynd af kvittun. Einnig geta notendur safna myndum af kvittun og síðan tengið hana kostnaðarskýrslu síðar. Starfsmenn geta einnig stofna og haft umsjón með sínum kostnaðarskýrslum, og sent þær svo til samþykkis og endurgreiðslu með því að nota fartækið sitt.


Nánar tiltekið gerir fartækjavinnusvæðið **Kostnaðarstýring** notendum kleift að vinna þessi verk:

- Taka mynd af kvittun og hlaða inn á Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu. Þú getur svo tengt myndina við kostnaðarskýrslu seinna.
- Senda inn skrá sem fönguð kvittun. Þú getur svo tengt skrána við kostnaðarskýrslu seinna.
- Stofna nýja línu í kostnaðarskýrslu með því að nota viðhengda kvittun. Þú getur svo bætt línuatriði við kostnaðarskýrslu síðar og sent hana til samþykktar og endurgreiðslu.

Ef þú ert að nota Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu með uppfærslu frá júlí 2017, geturðu einnig notað þessa eiginleika:

- Stofna nýja kostnaðarskýrslu.
- Tengja kreditkortafærslur og annan kostnað sem var áður stofnaður við kostnaðarskýrslu.
- Stofna nýjan kostnað fyrir kostnaðarskýrslu.
- Tengja kvittun við hvaða kostnað sem er fyrir kostnaðarskýrslu, annaðhvort með því að taka mynd af kvittuninni eða með því að hlaða upp skrá sem sótta kvittun.
- Bæta gestalista við kostnað ef kostnaðarreglur fyrirtækisins leyfa það.
- Sundurliða kostnað ef kostnaðarreglur fyrirtækisins leyfa það.
- Senda inn kostnaðarskýrslu til samþykkis og endurgreiðslu.
- Samþykkja eða hafna kostnaðarskýrslum sem þú ert úthlutaður samþykkjandi fyrir.

## <a name="prerequisites"></a>Frumskilyrði
Forkröfur eru mismunandi eftir þeirri útgáfu Microsoft Dynamics 365 sem hefur verið innleidd í fyrirtækinu.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Forkröfur ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfa, uppfærsla í júlí 2017 
Hafi Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfa með uppfærslu frá júlí 2017 verið innleidd í fyrirtækinu verður kerfisstjóri að gefa út fartækjavinnusvæðið **Kostnaðarstýring**. Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forkröfur ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar
Ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar í fyrirtækinu, verður kerfisstjóri að uppfylla eftirfarandi forkröfur. 

<table>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Hlutverk</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innleiða KB 4019015.</td>
<td>Kerfisstjóri</td>
<td>KB 4019015 er X++ uppfærsla eða bráðabót lýsingagna sem inniheldur fartækjavinnusvæði <strong>Kostnaðarstýring</strong>. Til að setja upp KB 4019015 verður kerfisstjóri að fylgja eftirfarandi skrefum.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Sæktu lýsigagnabráðabótina á Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Setja upp bráðabót lýsigagna</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Stofna virkjanlegan pakka</a> sem inniheldur <strong>ApplicationSuite</strong> og <strong>ExpenseMobile</strong> virðislíkön og hlaða svo upp virkjanlegum pakka í LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Notaðu virkjanlega pakkann</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Birta fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>.</td>
<td>Kerfisstjóri</td>
<td>Sjáið <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Sæktu og settu upp Dynamics 365 fyrir Operations farsímaforrit
Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:

- [Fyrir Android síma](https://go.microsoft.com/fwlink/?linkid=850662)
- [Fyrir iPhone síma](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Innskráning í fartækjaforritið
1. Ræstu forritið í fartækinu þínu.
2. Færðu inn vefslóð þína fyrir Dynamics 365.
4. Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt. Færðu inn skilríki
5. Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið. Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.


[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Fangaðu kvittun á fartækjavinnusvæðinu með Útgjaldastjórnun

1. Í fartækinu opnarðu vinnusvæðið **Kostnaðarstýring**.
2. Velja **Föngun kvittunar**.
3. Veljið **Taka mynd** eða **Velja mynd**.
4. Fylgið einu af eftirfarandi skrefum:

    - Ef valið er **Taka mynd**, skal fylgja þessum skrefum:

        1. Þú færist yfir á myndavél á fartækinu þínu, svo þú getir tekið mynd af kvittuninni. Þegar búið er að taka mynd velurðu **í lagi** til að samþykkja myndina.
        2. Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

    - Ef þú valdir **Velja mynd** skal fylgja þessum skrefum:

        1. Í listanum skal velja mynd.
        2. Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

5. Velja **Ekkert**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Færðu inn kostnað með skjótum hætti með því að fartækjavinnusvæðið Kostnaðarstýring
1. Í fartækinu opnarðu vinnusvæðið **Kostnaðarstýring**.
2. Veljið **Útgjöld snögg færsla**.
3. Velja tegund fyrir útgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef flokkurinn þinn er ekki á listanum. Leita eftir flokki útgjalda eða skipta til að leita eftir tegund útgjalda.
4. Færa inn dagsetningu færslu útgjaldanna.
5. Valfrjálst: Færið inn söluaðila kostnaðar.
6. Færið inn útgjaldaupphæð.
7. Veljið gjaldmiðilskóðann fyrir úgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. Sjálfgefið er að 400 gjaldmiðlar séu hlaðnir en þeirri tölu má breyta af forritara. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef gjaldmiðillinn þinn er ekki á listanum. Leita eftir gjaldmiðli eða skipta til að leita eftir nafni.
8. Veljið **Taka mynd** eða **Velja mynd**.
9. Fylgið einu af eftirfarandi skrefum:

    - Ef þú valdir **Taka mynd**, ertu færður yfir á myndavél fartækisins, svo þú getir myndað kvittunina. Þegar búið er að taka mynd velurðu **í lagi** til að samþykkja myndina.
    - Veldu mynd á listanum ef þú valdir **Velja mynd**.

10. Velja **Ekkert**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Samþykkja kostnaðarskýrslu með því að nota fartækjavinnusvæðið Kostnaðarstýring (ef þú notar uppfærsluna frá júlí 2017)
1. Í fartækinu opnarðu vinnusvæðið **Kostnaðarstýring**.
2. **Kostnaðarsamþykki** sýnir fjölda kostnaðarskýrsla sem hafa verið úthlutaðar þér til samþykkis. Fjöldinn uppfærist á um 30 mínútna fresti. Veldu **Kostnaðarsamþykki**.

    Listi kostnaðarskýrslna sem hafa verið úthlutaðar þér til samþykkis er sýndur.
    
3. Veldu kostnaðarskýrslu til að skoða kostnaðarupplýsingar hennar.
4. Veldu kostnað til að skoða upplýsingar um hann. Upplýsingarnar sem eru sýndar fyrir kostnað felur í sér allar upplýsingar um kvittanir, gesti og sundurliðanir.
5. Veldu að samþykkja eða hafna kostnaðarskýrslunni á síðunni **Kostnaðarskýrsla**.
6. Færðu inn athugasemdir fyrir samþykkisaðgerðina.
7. Velja **Ekkert**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Búðu til nýja kostnaðarskýrslu og sendu hana inn til samþykkis með því að nota fartækjavinnusvæðið Kostnaðarstýring (ef þú notar uppfærsluna frá júlí 2017)
1. Í fartækinu opnarðu vinnusvæðið **Kostnaðarstýring**.
2. Veldu **Kostnaðarfærslu**.
3. Veldu **Ný skýrsla**, eða veldu fyrirliggjandi kostnaðarskýrslu af listanum.
4. Færðu inn tilgang og allar viðbótarupplýsingar sem eru tiltækar fyrir nýjar kostnaðarskýrslur. Þessar upplýsingar er mismunandi, eftir því hvernig kostnaðarstýring er skilgreind fyrir fyrirtækið þitt.
5. Velja **Ekkert**.
6. Veldu **Tengja** til að bæta við fyrirliggjandi kostnaði, eins og kreditkortafærslum, við kostnaðarskýrslu.
7. Veldu einn eða fleiri kostnaðarliði í listanum.
8. Velja **Ekkert**.
9. Veldu **Nýr kostnaður** til að bæta nýjum kostnaði við kostnaðarskýrsluna.
10. Velja tegund fyrir útgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef flokkurinn þinn er ekki á listanum. Leita eftir flokki útgjalda eða skipta til að leita eftir tegund útgjalda.
11. Valfrjálst: Færið inn söluaðila kostnaðar.
12. Færa inn dagsetningu færslu útgjaldanna.
13. Færið inn útgjaldaupphæð.
14. Veljið gjaldmiðilskóðann fyrir úgjöldin. Þá sérðu lista yfir vörur sem er hlaðið upp í forritið til notkunar utan nets. Sjálfgefið er að 400 gjaldmiðlar séu hlaðnir en þeirri tölu má breyta af forritara. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef gjaldmiðillinn þinn er ekki á listanum. Leita eftir gjaldmiðli eða skipta til að leita eftir nafni.
15. Velja **Ekkert**.
16. Veldu **Bæta við meiri upplýsingum** til að bæta meiri upplýsingum við kostnaðinn. Reitirnir sem eru tiltækir fara eftir því hvernig kostnaðarstýring er skilgreind fyrir þitt fyrirtæki.
17. Veldu **Kvittanir** ef reglur fyrirtækisins gera kröfu um kvittun fyrir kostnaðinum, og fylgdu svo eftirfarandi skrefum:

    1. Veljdu **Fanga kvittun** eða **Tengja kvittun**.
    2. Fylgið einu af eftirfarandi skrefum:

        - Ef þú valdir **Fanga kvittun** skal fylgja þessum skrefum:

            1. Veljið **Taka mynd** eða **Velja mynd**.
            2. Fylgið einu af eftirfarandi skrefum:

                - Ef valið er **Taka mynd**, skal fylgja þessum skrefum:

                    1. Þú færist yfir á myndavél á fartækinu þínu, svo þú getir tekið mynd af kvittuninni. Þegar búið er að taka mynd velurðu **í lagi** til að samþykkja myndina.
                    2. Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

                - Ef þú valdir **Velja mynd** skal fylgja þessum skrefum:

                    1. Í listanum skal velja mynd.
                    2. Valfrjálst: Sláðu inn nafn myndarinnar og færðu inn þær athugasemdir sem þarf.

            3.  Velja **Ekkert**.

        - Ef þú valdir **Tengja kvittun** skal fylgja þessum skrefum:

            1.  Veldu eina eða fleiri myndir í listanum.
            2.  Velja **Ekkert**.

    3. Veldu hnappinn **Til baka** til að fara aftur í kostnaðarupplýsingarnar.

18. Veldu **Gestir** ef reglur fyrirtækisins gera kröfu um gesti fyrir kostnaðinum, og fylgdu svo eftirfarandi skrefum:

    1. Veldu **Gestur**, **Fyrri gestir** eða **Samstarfsmenn**.
    2. Fylgið einu af eftirfarandi skrefum:

        - Ef valið er **Gestur** skal fylgja þessum skrefum:

            1. Færðu inn heiti gestsins.
            2. Valfrjáls: Færðu inn fyrirtæki og/eða land gestsins.
            3. Valfrjálst: Færðu inn starfstitil gestarins.
            4. Velja **Ekkert**.

        - Ef þú valdir **Fyrri gestir** skal fylgja þessum skrefum:

            1. Veldu einn eða fleiri fyrri gesta í listanum. Þú sérð lista af fyrri gestum sem þú hefur bætt við fyrri kostnaðarskýrslur sem er hlaðið inn í forritið þitt til að nota án nettengingar. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef fyrri gesturinn þinn er ekki á listanum. Leitaðu eftir nafni eða skiptu yfir í leit til að leita eftir fyrirtæki, landi eða starfstitli.
            2. Velja **Ekkert**.

        - Ef valdir eru **Samstarfsmenn** skal fylgja þessum skrefum:

            1. Veldu einn eða fleiri samstarfsmenn í listanum. Þá sérðu lista yfir samstarfsmenn sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef samstarfsmaðurinn þinn er ekki á listanum. Leitaðu eftir nafni eða skiptu yfir í leit til að leita eftir fyrirtæki eða starfstitli.
            2. Velja **Ekkert**.

    3. Veldu hnappinn **Til baka** til að fara aftur í kostnaðarupplýsingarnar.

19. Veldu **Sundurliða** ef reglur fyrirtækisins gera kröfu um að kostnaður sé sundurliðaður, og fylgdu svo eftirfarandi skrefum:

    1. Veldu fyrstu dagsetningu til að sundurliða.
    2. Veldu **Bæta við sundurliðun**.
    3. Veldu undirflokk fyrir sundurliðun kostnaðarins. Þá sérðu lista yfir undirflokka kostnaðar sem er hlaðið upp í forritið til notkunar utan nets. 50 atriðum er hlaðið sjálfgefið en þeirri tölu má breyta. Til að fá frekari upplýsingar ættu þróunaraðilar að skoða [Fartækjaverkvangur](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Veldu **Leit** til að leita á netinu ef undirflokkurinn þinn er ekki á listanum. Leita eftir heiti undirflokks kostnaðar.
    4. Færðu inn færsluupphæðina fyrir sundurliðunina.
    5. Breyttu dagsetningu færslunnar ef þess er krafist.
    6. Velja **Ekkert**.
    7. Endurtaktu skrefin á undan þar til þú hefur bætt við allri sundurliðun fyrir valda dagsetningu.
    8. Fyrir fleiri daga geturðu valið **Afrita á næsta dag** til að afrita sundurliðunina á næsta dag. Einnig geturðu valið dagsetningu til að sundurliða og svo bætt við sundurliðunum eins og fyrir fyrstu dagsetninguna.
    9. Veldu hnappinn **Til baka** þegar þú hefur lokið við að sundurliða kostnaðinn til að fara aftur í kostnaðarupplýsingarnar.

20. Veldu hnappinn **Til baka** til að fara aftur á síðuna **Kostnaðarskýrsla**.
21. Endurtaktu þrepin á undan þar til þú hefur bætt við öllum kostnaði.
22. Veldu **Senda**.
23. Færðu inn athugasemdir fyrir samþykkjandann.
24. Velja **Ekkert**.

