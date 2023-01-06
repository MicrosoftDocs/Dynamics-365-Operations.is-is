---
title: Færibreytur fyrir endurteknar samningsgreiðslur
description: Í þessari grein er útskýrt hvernig á að setja upp sjálfgefin gildi fyrir greiðsluáætlanir sem eru búnar til í endurteknum samningsgreiðslum. Þar er einnig útskýrt hvernig greiðsluáætlunarflokkar eru búnir til.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644004"
---
# <a name="recurring-contract-billing-parameters"></a>Færibreytur fyrir endurteknar samningsgreiðslur

Notaðu síðuna **Færibreytur fyrir endurteknar samningsgreiðslur** til að setja upp sjálfgefin gildi fyrir greiðsluáætlanir sem eru búnar til í endurteknum samningsgreiðslum. Allar greiðsluáætlanir sem þú útbýrð munu í upphafi nota þessi sjálfgefnu gildi. Þó er hægt að breyta gildunum fyrir hverja greiðsluáætlun eftir þörfum.

## <a name="general-tab"></a>Almennt

1. Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**, í flipanum **Almennt**, í reitnum **Greiðsluáætlunarflokkur**, skal velja greiðsluáætlunarflokk. Upplýsingar um hvernig á að setja upp greiðsluáætlunarflokka er að finna í hlutanum [Greiðsluáætlunarflokkar](#set-up-billing-schedule-groups) síðar í þessari grein.
2. Í reitnum **Tegund uppsagnar** skal velja hvernig lokareikningur er reiknaður þegar greiðsluáætlun er sagt upp:

    - **Laga áætlun** – Lokaðu á greiðsluáætlunina á uppsagnardeginum, breyttu stöðu áætlunar í **Síðasta reikningsfærsla** og lagaðu tengda frestunaráætlun með því að bakfæra upphæðina sem á ekki lengur að skrá. Ef upphafsdagur reiknings er á eftir lokadegi eru eftirstandandi reikningstímabil fjarlægð.
    - **Reikningur eftir** – Bættu eftirstandandi upphæðum í greiðsluáætlunina við uppsagnartímann, breyttu stöðu áætlunarinnar í **Síðasta reikningsfærsla** og uppfærðu frestunaráætlunina. Ef upphafsdagur reiknings er eftir lokadaginn er heildarupphæð allra eftirstandandi reikningstímabila bætt við reikningstímabilið og eftirstandandi reikningstímabil fjarlægð.
    - **Engin leiðrétting** – Segðu upp greiðsluáætluninni á uppsagnardeginum. Engar leiðréttingar eru gerðar á greiðsluáætluninni.

3. Í reitnum **Gerð einkvæmrar áætlunar** skal velja **Engin** til að tilgreina að viðskiptavinir takmarkist við eina greiðsluáætlun. Veldu **Á viðskiptavin** eða **Á endanotanda** til að tilgreina að viðskiptavinir takmarkist við einkvæma áætlun.
4. Stilltu valkostinn **Samræma við mánuð** á **Já** til að samræma upplýsingalínur greiðsluáætlunar við lok mánaðar þegar greiðsluáætlun er stofnuð eða uppfærð. Stilltu hann á **Nei** til að nota dagsetningar sem bætt er við.
5. Stilltu valkostinn **Hlutfallsskipta hluta úr tímabilum** á **Já** til að úthluta greiðsluupphæðum út frá fjölda daga á tímabilinu. Stilltu á **Nei** til að vera með jafna upphæð á hverju reikningsfærðu tímabili burtséð frá fjölda daga.
6. Ef valkosturinn **Hlutfallsskipta hluta úr tímabilum** er stilltur á **Já** skal stilla reitinn **Aðferð hlutfallsskiptingar** á **Daglega** til að dreifa upphæðum út frá fjölda daga á tímabilinu. Stilltu hann á **Mánaðarlega** til að vera með jafna upphæð í hverjum mánuði.
7. Tilgreindu hvort nýlega gerðar greiðsluáætlanir séu í bið sjálfgefið.

    > [!NOTE]
    > Til að fjarlægja bið á greiðsluáætlun verður notandi að vera hluti af notendaflokki. Veldu **Hnekkja notendaflokki fyrir fjarlægingu biðstöðu** til að setja upp notendaflokk þar sem valkosturinn **Leyfa að fjarlægja biðstöðu** er virkur.

8. Í reitnum **Gerð reikningsfærslu** skal velja sjálfgefna gerð reikningsfærslu fyrir nýjar greiðsluáætlanir.
9. Stilltu valkostinn **Samræma frestun við greiðslu** á **Já** til að samræma samsvarandi frestunaráætlun þannig að hún noti sömu dagsetningar og greiðsluáætlunin. Stillið á **Nei** til að hafa aðra daga.
10. Ef þú notar eiginleika tekjuskiptingar skal stilla valkostinn **Stofna tekjuskiptingu sjálfkrafa** á **Já** þegar vörum er bætt við greiðsluáætlun. Gátreiturinn **Tekjuskipting** verður sjálfkrafa valinn í greiðsluáætlunarlínunni ef varan er sett upp sem vara tekjuskiptingar. Veldu valkostinn **Nei** ef á að velja á gátreitinn **Tekjuskipting** handvirkt.
11. Stilltu valkostinn **Skipting viðskiptavinar** á **Já** til að leyfa greiðsluáætlun sé reikningsfærð á aðra viðskiptavini. Þegar hann er stilltur á **Já** er valkosturinn **Skipting viðskiptavinar** í boði í haus og línu greiðsluáætlunar. 
12. Stilla reitina fyrir stofnun sölupantana:

    - Hægt er að sameina reikninga eftir tímabili, viðskiptavini eða vöru. Hægt er að velja hvaða samsetningu sem er af **Já** og **Nei**. Einnig er hægt að skipta reikningum eftir vöruflokkum.
    - Eftirtaldir bókunarvalkostir eru í boði fyrir reikninga:

        - **Stofna sölupöntun** – Stofna aðeins sölupöntunina.
        - **Sýna bókun reiknings** – Reikningsfærðu sölupöntunina og opnaðu síðu þar sem hægt er að bóka reikninginn handvirkt.
        - **Stofna textareikning með gjaldi** – Veldu þennan valkost ef reikningar með frjálsum texta eru notaðir.
        - **Bóka reikning sjálfvirkt** – Reikningsfærðu sölupöntunina og bókaðu hana sjálfkrafa.

    - Veldu valkostinn **Bæta greiðsludögum við vörulýsingu** á **Já** til að bæta við lýsingu sem inniheldur upphafs- og lokadagsetningu reikningsfærslunnar.
    - Stilltu valkostinn **Útiloka núll notkun** á **Já** til að útiloka greiðsluáætlunarlínur sem eru ekki með neina notkun. Stilltu hann á **Nei** til að hafa þessar línur í sölupöntuninni.
    - Stilltu valkostinn **Ekki prenta undirvörur** á **Já** ef ekki á að prenta undirvörur tekjuskiptingar í sölupöntuninni. Aðeins yfirvaran mun birtast á reikningnum. Ef nettóupphæð (földu) undirvörunnar er ekki summa sem ekki er núll sýnir nettóupphæð yfirlínunnar samantekt á undirlínunum. Stilltu valkostinn á **Nei** til að prenta undirvöru fyrir neðan yfirvöruna á sölureikninginn.

12. Stilla reitina fyrir stuðning og endurnýjun:

    - Stilltu valkostinn **Virkja þjónustu og endurnýjun sjálfkrafa** á **Já** til að nota eiginleika þjónustu og endurnýjunar sjálfkrafa í sölupöntun.
    - Í reitnum **Þjónustu- og endurnýjunarstig** skal velja sjálfgefið þjónustu- og endurnýjunarstigið.
    - Í reitnum **Þjónust- og endurnýjunarmagn** skal tilgreina þjónustu- og endurnýjunarmagn.
    - Í reitnum **Sjálfgefin upphafsdagsetning þjónustu og endurnýjunar** skal tilgreina dagsetninguna sem á að nota sem sjálfgefna upphafsdagsetningu fyrir þjónustu og endurnýjun:

        - **Færsludagsetning** – Notaðu færsludagsetninguna sem upphafsdagsetningu.
        - **Upphaf yfirstandandi mánaðar** – Notaðu fyrsta dag yfirstandandi mánaðar sem upphafsdagsetningu.
        - **Byrjun næsta mánaðar** – Notaðu fyrsta dag næsta mánaðar sem upphafsdagsetningu. Ef færsludagsetningin er þann fyrst þá er fyrst núverandi mánaðar notaður.
        - **Regla um 15** – Notaðu fyrsta núverandi mánaðar sem upphafsdagsetningu ef færsludagsetningin er milli fyrsta og fimmtánda í mánuðinum. Ef færsludagsetningin er sextándi eða síðar skal nota fyrsta næsta mánaðar sem upphafsdagsetningu.

    - Stilltu valkostinn **Taka afslátt með í útreikning** á **Já** til að taka afsláttarupphæð með í upphæð þjónustu eða endurnýjunar. Stilltu það á **Nei** til að taka ekki með afsláttarupphæðina.
    - Í reitunum **Þjónustutíðni** og **Endurnýjunartíðni** skal velja tíðnina fyrir notkun þegar þjónustu- og endurnýjunaratriðum er bætt við greiðsluáætlun: **Daglega**, **Mánaðarlega**, **Ársfjórðungslega**, **Annað hvert ár** eða **Árlega**.
    - Stilltu valkostinn **Samræma eftir vöruflokki** á **Já** til að samræma upphafs- og lokadagsetningu nýrra vara við fyrirliggjandi vörur, samkvæmt vöruflokknum.
    - Stilltu valkostinn **Samræma við næsta ógreidda tímabil** á **Já** til að ákvarða samræmingardagsetningu fyrir endurnýjunaratriði út frá dagsetningunni á næsta ógreidda tímabil eftir að endurnýjun hefst.
    - Stilltu valkostinn **Afrita raðnúmer** á **Já** til að afrita raðnúmer vörunnar úr upphaflegri sölupöntunarlínu í samsvarandi greiðsluáætlunarlínu.

13. Ef þú notar hækkun í greiðsluáætluninni skal velja aðferðina sem er notuð fyrir útreikning á vísitölu neysluverðs.
14. Stilltu valkostinn **Rekja verðbreytingu** á **Já** ef þú vilt fá færslu yfir verðbreytingar á greiðsluáætlunarlínum. Ef greiðsluáætlunarlína er breytt handvirkt úr hefðbundinni í flata og nýtt verð slegið inn eru upplýsingar eftirlits raktar í greiðsluáætlunarlínunni. Stilltu valkostinn á **Nei** ef ekki á að rekja þessar breytingar.
15. Tilgreindu hvort færslur eru síaðar eftir upphafsdagsetningu eða lokadagsetningu sjálfgefið á síðunni **Búa til reikning**.
16. Ef eiginleikinn **Óreikningsfærðar tekjur** er notaður skal tilgreina valkostina sem eru notaðir:

    - Stilltu valkostinn **Bóka færslubók sjálfvirkt** á **Já** ef á að stofna og bóka færslubókina á sama tíma. Stilltu hann á **Nei** ef á að stofna færslubókina og síðan bóka hana handvirkt.
    - Í reitnum **Sjálfgefið heiti færslubókar** skal velja sjálfgefið heiti færslubókar til að nota þegar færslubókin er stofnuð.
    - Í reitnum **Aðferð fyrir óreikningsfært til skamms tíma** skal velja aðferð óreikningsfært til skamms tíma ef þú ert að nota slíkt. Ef þú velur **Ekkert** verður skammtímavirknin ekki notuð með óreikningsfærðum tekjum. Veldu **Hlaupandi tímabil** til að nota alltaf 12 mánuði eða **Fast ár** til að nota það sem eftir er af fjárhagsárinu.

17. Tilgreindu valkostina sem eru notaður þegar greiðsluáætlun og línum hennar er sagt upp:

    - **Gefa út kreditfærslu** – Stofna kreditnótu þegar greiðsluáætlun eða greiðsluáætlunarlínu er sagt upp.
    - **Kreditleiðréttingar** – Búðu til kreditleiðréttingu fyrir greiðsluáætlun þegar línu er sagt upp. Kreditleiðréttingin birtist á reikningstímabilum í framtíðinni fyrir greiðsluáætlunina. Kreditleiðréttingin mun uppfæra reikningsupphæðina fyrir næsta greiðslutímabil þar til búið er að nota inneignina á greiðsluáætlunina.
    - **Engin inneign** – Ekki stofna kreditleiðréttingu eða kreditnótu þegar greiðsluáætlun eða greiðsluáætlunarlínu er sagt upp. Þessi valkostur er aðeins í boði þegar valkosturinn **Engin leiðrétting** er notaður til að segja upp greiðsluáætlun.
18. Þegar valkosturinn **Í eitt skipti er hægt að segja upp með endurgreiðslu** er stilltur á **Nei** og greiðsluáætlun með greiðslutíðni upp á **Eitt skipti** breytist staða greiðsluáætlunarlínunnar í **Sagt upp** þegar greiðsluáætlunin er reikningsfærð. Ekki er hægt að segja upp þessari greiðsluáætlun og engin inneign er gefin út. Þegar **Í eitt skipti er hægt að segja upp með endurgreiðslu** er stilltur á **Já** verður greiðsluáætlunarlína með greiðslutíðni upp á **Eitt skipti** með stöðuna **Virk** eftir að greiðsluáætlun er reikningsfærð. Hægt er að segja upp greiðsluáætlunarlínunni og vinna úr endurgreiðslu. 
19. Valkosturinn **Hlutfallsskipta daglega** sem er stilltur í færibreytum fer sjálfgefið á síðu fjöldauppsagnar og uppsagnarglugga greiðsluáætlunarhauss og línu. Hægt er að breyta honum í uppsagnarferlinu. Þegar hann er stilltur á **Já** verða allar endurgreiðslupphæðir reiknaðar með daglegum daglegri tíðni. Þegar stillt er á **Nei** verður kreditfærsla samkvæmt uppsagnardagsetningu og greiðslutíðni. Ef til dæmis er notuð mánaðarleg tíðni og greiðsluupphæðin var $100 á mánuði er upphæð inneignar í $100 áföngum. Ef greiðslutíðnin er einskiptis er upphæð inneignar $0,00. Stilla verður daglega hlutfallsskiptingu á „Já“ til að fá endurgreiðslu fyrir einskiptis greiðslutíðni. 
20. Stilltu valkostinn **Búa til frestun fyrir inneign** á **Já** til að stofna nýja frestunaráætlun ef kreditfæra á fyrirliggjandi frestunaráætlun. Skildu valkostinn eftir á **Nei** til að stofna kreditfærsluna á fyrirliggjandi frestunaráætlun.

## <a name="sequence-number-tab"></a>Raðnúmersflipi

Notaðu flipann **Raðnúmer** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** til að stilla sjálfgefið gildi fyrir númer greiðsluáætlunar. Sjálfgefin gildi eru sett upp á síðunni **Númeraraðir** (**Fyrirtækisstjórnun \> Númeraraðir \> Númeraraðir**).

## <a name="set-up-billing-schedule-groups"></a>Setja upp greiðsluáætlunarflokka

Notaðu síðuna **Greiðsluáætlunarflokkur** til að stofna greiðsluáætlunarflokk fyrir endurtekna samningsgreiðslu. Þegar ný greiðsluáætlun er búin til og greiðsluáætlunarflokkur er settur á hana eru gildin sem skilgreind eru á síðunni **Greiðsluáætlunarflokkur** slegin inn sem sjálfgefin gildi fyrir greiðsluáætlunina. Hægt er að breyta hvaða sjálfgefna gildi sem er fyrir tiltekna greiðsluáætlun sem er búin til. Hægt er að setja upp marga greiðsluáætlunarflokka og úthluta svo einum þeirra sem sjálfgefnum greiðsluáætlunarflokki á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

Til að búa til greiðsluáætlunarflokk fyrir endurtekna samningsgreiðslu skal fylgja þessum skrefum.

1. Á síðunni **Greiðsluáætlunarflokkur** skal velja **Nýr** til að búa til nýjan greiðsluáætlunarflokk.
2. Í reitinn **Greiðsluáætlunarflokkur** skal færa inn einkvæmt kennimerki.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Í reitnum **Greiðslutíðni** skal tilgreina hversu oft greiðsluáætlunin er send til innheimtu á viðskiptavin: **Eitt skipt**, **Daglega**, **Mánaðarlega**, **Ársfjórðungslega**, **Hálfs árs fresti** eða **Árlega**.
5. Í reitinn **Greiðslutímabil** skal færa inn greiðslutímabil. Stilltu til dæmis reitinn **Greiðslutíðni** á **Mánaðarlega** og reitinn **Greiðslutímabil** á **2** til að innheimta annan hvern mánuð.
6. Í reitnum **Verðlagningaraðferð** skal velja sjálfgefna verðlagningaraðferð fyrir vörur í greiðsluáætluninni:

    - **Staðlað** – Reiknaðu einingarverðið út frá heildarmagni sem fært er inn og notaðu staðlaða verðlagningu á síðunni **Útgefnar afurðir** í afurðaupplýsingastjórnun.
    - **Fast** – Notaðu fast verð sem er slegið inn í greiðsluáætlunarlínuna.
    - **Lag** – Reiknaðu einingarverðið með því að nota fast magn í mismunandi verðþrepum. Fylla verður út hvert lag áður en farið er í næsta verðþrep.
    - **Fast lag** – Reiknaðu út einingarverðið með því að nota fast magn og upphæðir reiknaðs verðs fyrir mismunandi verðþrep. Verðið sem er innheimt á greiðslutímabili notar reiknað verð sem samsvarar þrepinu þar sem greiðslumagnið er til staðar.

7. Í reitnum **Vörutegund** skal velja tegund vöru fyrir greiðsluflokkinn:

    - **Staðlað** – Veldu þetta gildi ef magn er fast.
    - **Notkun** – Veldu þetta gildi fyrir mældar vörur eða neysluvörur. Ef þetta gildi er valið skal stilla reitinn **Lestrarvalkostur notkunar** á **Lestur** til að slá inn gildið (lestur) fyrir greiðslutímabil á mæli eða tæki. Notað gildi verður reiknað út frá fyrra greiðslutímabili og núverandi lestri sem færður er inn.
    - **Áfangi** – Veldu þetta gildi til að nota virkni greiðsluáfanga. Ef þetta gildi er valið í reitnum **Sniðmát áfanga** skal velja áfangasniðmátið ef slíkt er notað.
    - **Notkun** – Veldu þetta gildi til að slá inn gildið sem er notað fyrir greiðslutímabil.

8. Stilltu valkostinn **Reikningsfæra sérstaklega** á **Já** til að búa til samsetningu af samstæðureikningum og aðskildum reikningum fyrir sama viðskiptavininn. Til dæmis er viðskiptavinur með fimm greiðsluáætlanir. Þrjár þeirra verða sameinaðar í einn reikning, en hinar tvær þurfa aðskilda reikninga. Stilltu valkostinn á **Nei** til að búa til aðeins einn samstæðureikning fyrir viðskiptavininn.
9. Stilltu valkostinn **Endurnýja sjálfkrafa** á **Já** til að endurnýja endurtekna greiðsluáætlun sjálfkrafa fyrir næsta greiðslutímabil þegar reikningurinn er búinn til. Stilltu hann á **Nei** til að endurnýja greiðsluáætlunina handvirkt. Í reitnum **Línur til að bæta við fyrir hverja endurnýjun** skal tilgreina hversu mörgum línum á að bæta við fyrir hverja endurnýjun.
10. Stilltu valkostinn **Stighækkun** á **Já** til að nota *stighækkanir* (verðaukningu) á greiðsluáætlanir sem tengjast þessum greiðsluáætlunarflokki.
