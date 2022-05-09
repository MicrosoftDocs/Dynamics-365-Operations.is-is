---
title: Færibreytur fyrir endurteknar samningsgreiðslur
description: Þetta efnisatriði útskýrir hvernig á að setja upp sjálfgefin gildi fyrir innheimtuáætlanir sem eru búnar til í Endurteknum samningsreikningum. Það útskýrir einnig hvernig stofna innheimtuáætlunarhópa.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4c52095aa49962cbfc577faf71ab0d71929a386b
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629705"
---
# <a name="recurring-contract-billing-parameters"></a>Færibreytur fyrir endurteknar samningsgreiðslur

Nota **Endurteknar innheimtufæribreytur samnings** síðu til að setja upp sjálfgefin gildi fyrir innheimtuáætlanir sem eru búnar til í Endurteknum samningsreikningum. Allar innheimtuáætlanir sem þú býrð til munu upphaflega nota þessi sjálfgefna gildi. Hins vegar geturðu breytt gildunum fyrir hverja innheimtuáætlun eftir þörfum.

## <a name="general-tab"></a>Almennt

1. Á **Endurteknar innheimtufæribreytur samnings** síðu, á **Almennt** flipa, í **Innheimtuáætlunarhópur** reit, veldu innheimtuáætlunarhóp. Fyrir upplýsingar um hvernig á að setja upp innheimtuáætlunarhópa, sjá [Innheimtuáætlunarhópar](#set-up-billing-schedule-groups) kafla síðar í þessu efni.
2. Í **Uppsagnartegund** reit, veldu hvernig endanlegur reikningur er reiknaður út þegar innheimtuáætlun er hætt:

    - **Stilla áætlun** – Slepptu innheimtuáætluninni á uppsagnardegi, breyttu stöðu áætlunarinnar í **Síðasta innheimta**, og stilla tilheyrandi frestunaráætlun með því að bakfæra upphæðina sem ekki þarf lengur að viðurkenna. Ef upphafsdagur innheimtu er eftir uppsagnardaginn eru reikningstímabilin sem eftir eru fjarlægð.
    - **Reikningur eftir** – Bættu öllum upphæðum sem eftir eru í innheimtuáætluninni við uppsagnartímabilið, breyttu stöðu áætlunarinnar í **Síðasta innheimta**, og uppfærðu frestunaráætlunina. Ef upphafsdagur innheimtu er eftir uppsagnardagsetningu er heildarupphæð allra eftirstandandi innheimtutímabila bætt við innheimtutímabilið og eftirstandandi innheimtutímabil eru fjarlægð.
    - **Engin aðlögun** – Slepptu innheimtuáætluninni á uppsagnardegi. Engar breytingar eru gerðar á innheimtuáætlun.

3. Í **Einstök áætlunargerð** reit, veldu **Enginn** að tilgreina að viðskiptavinir séu takmarkaðir við eina greiðsluáætlun. Veldu **Á hvern viðskiptavin** eða **Á hvern endanotanda** að tilgreina að viðskiptavinir séu takmarkaðir við einstaka tímaáætlun.
4. Stilltu **Samræma við mánuði** valmöguleika til **Já** til að samræma línur innheimtuáætlunar við lok mánaðar þegar innheimtuáætlun er búin til eða uppfærð. Stilltu það á **Nei** að nota stigvaxandi dagsetningar.
5. Stilltu **Hlutfallslega hlutatímabil** valmöguleika til **Já** að úthluta innheimtufjárhæðum miðað við fjölda daga á tímabilinu. Stilltu það á **Nei** að hafa jafna upphæð á hverju reikningstímabili, óháð fjölda daga.
6. Ef þú stillir **Hlutfallslega hlutatímabil** valmöguleika til **Já**, stilltu **Hlutfallsaðferð** sviði til **Daglega** að dreifa upphæðum eftir fjölda daga á tímabilinu. Stilltu það á **Mánaðarlega** að hafa jafna upphæð í hverjum mánuði.
7. Tilgreindu hvort nýstofnaðar innheimtuáætlanir séu sjálfgefið í bið.

    > [!NOTE]
    > Til að fjarlægja bið á innheimtuáætlun verður notandinn að vera hluti af notendahópi. Veldu **Fjarlægja hnekkingu bið notendahóps** að setja upp notendahóp þar sem **Leyfa fjarlægja bið** valmöguleikinn er virkur.

8. Í **Tegund reikningsfærslu** reit, veldu sjálfgefna reikningsfærslugerð fyrir nýjar innheimtuáætlanir.
9. Stilltu **Samræma frestun við innheimtu** valmöguleika til **Já** að samræma samsvarandi frestunaráætlun þannig að hún noti sömu dagsetningar og innheimtuáætlun. Stilltu það á **Nei** að hafa mismunandi dagsetningar.
10. Ef þú ert að nota tekjuskiptingaraðgerðina skaltu stilla **Búðu til tekjuskiptingu sjálfkrafa** valmöguleika til **Já** þegar hlutum er bætt við innheimtuáætlun. The **Tekjuskipting** gátreiturinn verður sjálfkrafa valinn á innheimtuáætlunarlínunni ef hluturinn er settur upp sem tekjuskiptur liður. Stilltu valkostinn á **Nei** ef þú vilt velja handvirkt **Tekjuskipting** gátreit.
11. Stilltu reiti til að búa til sölupöntun:

    - Reikningar geta verið sameinaðir eftir tímabilum, viðskiptavinum eða hlutum. Hvaða samsetning af **Já** og **Nei** hægt er að stilla gildi. Einnig er hægt að skipta reikningum eftir vöruflokkum.
    - Eftirfarandi bókunarvalkostir eru í boði fyrir reikninga:

        - **Stofna sölupöntun** – Stofna aðeins sölupöntunina.
        - **Sýna bókunarreikning** – Reiknaðu sölupöntunina og opnaðu síðu þar sem þú getur bókað reikninginn handvirkt.
        - **Búðu til gjaldtextareikning** – Veldu þennan valkost ef þú ert að nota reikninga með frjálsum texta.
        - **Bókaðu reikning sjálfkrafa** – Reiknaðu sölupöntunina og bókaðu hana sjálfkrafa.

    - Stilltu **Bættu innheimtudagsetningum við vörulýsingu** valmöguleika til **Já** til að bæta við lýsingu sem inniheldur upphafsdag og lokadag innheimtu.
    - Stilltu **Útiloka núllneyslu** valmöguleika til **Já** að útiloka innheimtuáætlunarlínur sem hafa enga notkun. Stilltu það á **Nei** að hafa þessar línur með í sölupöntuninni.
    - Stilltu **Ekki prenta barnavörur** valmöguleika til **Já** ef þú vilt ekki prenta undirliði tekjuskiptingar á sölupöntun. Aðeins yfirliðurinn mun birtast á reikningnum. Ef nettóupphæð (falinna) undirliða er summa sem ekki er núll, sýnir nettóupphæð móðurlínunnar samantekt yfir undirlínurnar. Stilltu valkostinn á **Nei** að prenta allar undirvörur fyrir neðan móðurvöruna á sölureikningnum.

12. Stilltu reiti fyrir stuðning og endurnýjun:

    - Stilltu **Sjálfvirk stuðningur og endurnýjun** valmöguleika til **Já** til að nota sjálfkrafa stuðnings- og endurnýjunareiginleikann í sölupöntun.
    - Í **Stuðnings- og endurnýjunarstig** reit, veldu sjálfgefið stuðnings- og endurnýjunarstig.
    - Í **Stuðnings- og endurnýjunarmagn** reit, tilgreinið stuðnings- og endurnýjunarmagn.
    - Í **Sjálfgefin upphafsdagur stuðnings og endurnýjunar** reit, tilgreindu dagsetninguna sem á að nota sem sjálfgefna upphafsdagsetningu fyrir stuðning og endurnýjun:

        - **Dagsetning viðskipta** – Notaðu viðskiptadagsetninguna sem upphafsdagsetningu.
        - **Upphaf yfirstandandi mánaðar** – Notaðu þann fyrsta í núverandi mánuði sem upphafsdagsetningu.
        - **Upphaf næsta mánaðar** – Notaðu fyrsta næsta mánaðar sem upphafsdag. Ef viðskiptadagur er sá fyrsti er sá fyrsti í núverandi mánuði notaður.
        - **Regla 15** – Notaðu fyrsta dag þessa mánaðar sem upphafsdag ef viðskiptadagsetning er á milli fyrsta og fimmtánda mánaðar. Ef viðskiptadagsetningin er sextándi eða síðar, skal nota fyrsta næsta mánaðar sem upphafsdag.

    - Stilltu **Taka afslátt með í útreikningi** valmöguleika til **Já** að taka afsláttarupphæðina inn í styrktar- eða endurnýjunarupphæðina. Stilltu það á **Nei** að undanskilja afsláttarupphæðina.
    - Í **Stuðningstíðni** og **Endurnýjunartíðni** reiti, veldu þá tíðni sem á að nota þegar stuðnings- og endurnýjunaratriðum er bætt við innheimtuáætlun: **Daglega**, **·**, **·**, **·**, eða **Árlega**.
    - Stilltu **Samræma eftir vöruflokki** valmöguleika til **Já** til að samræma upphafs- og lokadagsetningar nýrra vara við núverandi vörur, byggt á vöruflokknum.
    - Stilltu **Samræma við næsta óinnheimta tímabil** valmöguleika til **Já** til að ákvarða jöfnunardagsetningu fyrir endurnýjunarvöru miðað við dagsetningu næsta óinnheimtu tímabils eftir að endurnýjun hefst.
    - Stilltu **Afritaðu raðnúmer** valmöguleika til **Já** til að afrita raðnúmer vöru frá upphaflegu sölupöntunarlínunni yfir í samsvarandi innheimtuáætlunarlínu.

13. Ef þú ert að nota stigmögnun á innheimtuáætluninni skaltu velja aðferðina sem er notuð við útreikning vísitölu neysluverðs.
14. Stilltu **Fylgstu með verðbreytingum** valmöguleika til **Já** ef þú vilt skrá yfir verðbreytingar á innheimtuáætlunarlínum. Ef innheimtuáætlunarlínu er breytt handvirkt úr staðlaðri í íbúð og nýtt verð fært inn, eru endurskoðunarupplýsingar raktar á innheimtuáætlunarlínunni. Stilltu valkostinn á **Nei** ef þú vilt ekki fylgjast með þessum breytingum.
15. Tilgreindu hvort færslur séu síaðar eftir upphafsdegi eða lokadagsetningu sjálfgefið á **Búðu til reikning** síðu.
16. Ef þú notar **Óinnheimtar tekjur** eiginleiki, tilgreindu valkostina sem eru notaðir:

    - Stilltu **Bókaðu almenna dagbók sjálfkrafa** valmöguleika til **Já** ef þú vilt að almenna dagbókin verði búin til og bókuð á sama tíma. Stilltu það á **Nei** ef þú vilt búa til almenna dagbók og bóka hana síðan handvirkt.
    - Í **Sjálfgefið dagbókarheiti** reit, veldu sjálfgefið dagbókarheiti sem á að nota þegar almenna dagbókin er búin til.
    - Í **Skammtíma óinnheimt aðferð** reit, veldu skammtíma óinnheimta aðferð, ef þú ert að nota slíka. Ef þú velur **Enginn**, skammtímavirknin verður ekki notuð með óinnheimtuðum tekjum. Veldu **Rúllutímabil** að nota alltaf 12 mánuði eða **Fast ártal** að nota það sem eftir er af reikningsárinu.

17. Tilgreindu valkostina sem eru notaðir þegar innheimtuáætlun og línum hennar er hætt:

    - **Gefðu út lánsfé** – Búðu til kreditnótu þegar innheimtuáætlun eða innheimtuáætlunarlínu er hætt.
    - **Leiðrétting lána** – Búðu til inneignarleiðréttingu fyrir innheimtuáætlun þegar línu er hætt. Lánsfjárleiðréttingin birtist á framtíðarreikningstímabili fyrir innheimtuáætlunina. Lánsfjárleiðréttingin mun uppfæra reikningsupphæðina fyrir næsta reikningstímabil þar til inneign hefur lokið við að setja innheimtuáætlunina.
    - **Engin inneign** – Ekki búa til kreditleiðréttingu eða inneignarnótu þegar innheimtuáætlun eða innheimtuáætlunarlínu er hætt. Þessi valkostur er aðeins í boði þegar **Engin aðlögun** valkostur er notaður til að slíta innheimtuáætlun.

## <a name="sequence-number-tab"></a>Flipinn röð númera

Nota **Raðnúmer** flipann á **Endurteknar innheimtufæribreytur samnings** síðu til að stilla sjálfgefið gildi fyrir innheimtuáætlunarnúmer. Sjálfgefin gildi eru sett upp á **Númeraraðir** síða (**Stjórn stofnunarinnar \> Númeraraðir \> Númeraraðir**).

## <a name="set-up-billing-schedule-groups"></a>Settu upp greiðsluáætlunarhópa

Nota **Innheimtuáætlunarhópur** síðu til að búa til innheimtuáætlunarhóp fyrir endurtekna samningsreikninga. Þegar ný innheimtuáætlun er búin til og innheimtuáætlunarhópur er notaður á hana, verða gildin sem eru skilgreind á **Innheimtuáætlunarhópur** síðu eru færð inn sem sjálfgefin gildi fyrir innheimtuáætlunina. Þú getur breytt hvaða sjálfgefna gildum sem er fyrir tiltekna innheimtuáætlun sem þú býrð til. Þú getur sett upp marga innheimtuáætlunarhópa og síðan úthlutað einum þeirra sem sjálfgefinn innheimtuáætlunarhóp á **Endurteknar innheimtufæribreytur samnings** síðu.

Til að stofna innheimtuáætlunarhóp fyrir endurtekna samningsreikninga skal fylgja þessum skrefum.

1. Á **Innheimtuáætlunarhópur** síðu, veldu **Nýtt** til að búa til greiðsluáætlunarhóp.
2. Í **Innheimtuáætlunarhópur** reit, sláðu inn einstakt auðkenni.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í **Innheimtutíðni** reit, tilgreinið hversu oft innheimtuáætlun er innheimt á viðskiptavin: **Einu sinni**, **·**, **·**, **·**, **·**, eða **Árlega**.
5. Í **Innheimtubil** reit, sláðu inn greiðslubil. Til dæmis, stilltu **Innheimtutíðni** sviði til **Mánaðarlega** og **Innheimtubil** sviði til **2** að innheimta annan hvern mánuð.
6. Í **Verðlagningaraðferð** reit, veldu sjálfgefna verðlagningaraðferð fyrir vörur á innheimtuáætlun:

    - **Standard** – Reiknaðu einingarverð út frá heildarmagninu sem er slegið inn og notaðu staðlaða verðlagningu frá **Útgefnar vörur** síðu í Vöruupplýsingastjórnun.
    - **Flat** – Notaðu fast verð sem er fært inn á innheimtuáætlunarlínuna.
    - **Tier** – Reiknaðu einingarverð með því að nota fast magn á mismunandi verðflokkum. Fylla þarf út hvert þrep áður en farið er yfir í næsta verðflokk.
    - **Flat Tier** – Reiknaðu einingarverð með því að nota fast magn og lengri verðupphæðir fyrir mismunandi verðflokka. Verðið sem er innheimt á innheimtutímabili notar framlengda verðið sem samsvarar þrepinu þar sem innheimtumagnið er til.

7. Í **Tegund vöru** reit, veldu tegund vöru fyrir innheimtuhópinn:

    - **Standard** – Veldu þetta gildi ef magnið er óstöðugt.
    - **Notkun** – Veldu þetta gildi fyrir mælda hluti eða neysluvörur. Ef þú velur þetta gildi skaltu stilla **Notkunarmöguleiki fyrir lestur** sviði til **Lestur** til að slá inn gildi (lestur) fyrir reikningstímabil á mæli eða tæki. Notað verðmæti verður reiknað út frá fyrra reikningstímabili og núverandi lestri sem þú slærð inn.
    - **Áfangi** – Veldu þetta gildi til að nota innheimtuaðgerðina Milestone. Ef þú velur þetta gildi, í **Áfangasniðmát** reit, veldu áfangasniðmátið ef þú ert að nota það.
    - **Neysla** – Veldu þetta gildi til að slá inn gildið sem er notað fyrir greiðslutímabil.

8. Stilltu **Reikningur sérstaklega** valmöguleika til **Já** að búa til blöndu af samstæðureikningum og aðskildum reikningum fyrir sama viðskiptavin. Til dæmis hefur viðskiptavinur fimm innheimtuáætlanir. Þrír þeirra verða settir saman á einn reikning, en hver hinna tveggja þarf sérstakan reikning. Stilltu valkostinn á **Nei** að búa aðeins til einn samstæðureikning fyrir viðskiptavininn.
9. Stilltu **Endurnýja sjálfkrafa** valmöguleika til **Já** til að endurnýja sjálfkrafa endurtekna innheimtuáætlun fyrir næsta innheimtutímabil þegar reikningurinn er búinn til. Stilltu það á **Nei** til að endurnýja innheimtuáætlun handvirkt. Í **Línur til að bæta við fyrir hverja endurnýjun** reit, tilgreinið hversu mörgum línum á að bæta við fyrir hverja endurnýjun.
10. Stilltu **Stækkun** valmöguleika til **Já** að sækja um *stigmögnun* (verðhækkanir) við innheimtuáætlanir sem tengjast þessum innheimtuáætlunarhópi.
