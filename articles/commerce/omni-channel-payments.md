---
title: Greiðsluyfirlit omni-rásar
description: Þetta efnisatriði veitir yfirlit yfir greiðslur omni-rásar í Dynamics 365 Commerce.
author: rubendel
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 7b99b5f7b5b972d41e0831995bde69e9041369b9
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028012"
---
# <a name="omni-channel-payments-overview"></a>Greiðsluyfirlit Omni-rásar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir greiðslur omni-rásar í Dynamics 365 Commerce. Það inniheldur ítarlegan lista yfir studdar aðstæður, upplýsingar um virkni, uppsetningu og úrræðaleit, og lýsingar á dæmigerðum vandamálum.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Tákn | Strengur af gögnum sem greiðsluvinnsla býður upp á sem tilvísun. Tákn geta staðið fyrir greiðslukortanúmer, greiðsluheimildir og fyrri greiðslutökur. Tákn eru mikilvæg vegna þess að þau hjálpa til við að halda viðkvæmum gögnum fyrir utan sölustaðarkerfi. Stundum er einnig vísað í þau sem *tilvísanir*. |
| Kortatákn | Tákn sem greiðsluvinnsla býður upp á fyrir geymslu í sölustaðarkerfi. Eingöngu söluaðili sem tekur á móti kortatákni getur notað það. Stundum er einnig vísað í kortatákn sem *kortatilvísanir*. |
| Heimildartákn | Einkvæmt auðkenni sem greiðsluvinnsla veitir sem hluta svars sem hún sendir til sölustaðarkerfis eftir að sölustaðarkerfið sendir heimildarbeiðni. Heimildartákn er hægt að nota síðar ef kallað er eftir vinnslunni til að framkvæma aðgerðir á borð við bakfærslu eða ógildingu heimildar. Hins vegar er það oftast notað til að ná í reiðufé þegar pöntun er uppfyllt eða færsla er kláruð. Stundum er einnig vísað í heimildartákn sem *heimildartilvísanir*. |
| Greiðslutökutákn | Tilvísun sem greiðsluvinnsla veitir sölustaðarkerfi þegar greiðsla er kláruð eða sótt. Þá er hægt að nota greiðslutökutáknið til að vísa í greiðslutökuna fyrir næstu aðgerðir á borð við endurgreiðslubeiðni. | 
| Kort ekki til staðar | Hugtak sem vísar til greiðslufærslna þar sem sjálft kortið er ekki við höndina. Til dæmis geta þessar færslur átt sér stað í aðstæðum rafrænna viðskipta eða símavers. Fyrir þessar færslur eru greiðslutengdar upplýsingar færðar handvirkt inn á vefsvæði rafrænna viðskipta, í símaverssamskiptum eða á sölustað eða posa. |
| Kort til staðar | Hugtak sem vísar til greiðslufærslna þar sem sjálft kortið er við höndina og er notað í posa sem er tengdur við sölustaðarkerfi Microsoft Dynamics 365. |

## <a name="overview"></a>Yfirlit

Almennt séð lýsir hugtakið *greiðslur omni-rásar* möguleikanum á því að búa til pöntun í einni rás og uppfylla hana í annarri rás. Lykillinn að notendaþjónustu vegna greiðslu omni-rásar er að halda utan um greiðsluupplýsingar ásamt öðrum upplýsingum um pöntunina og síðan nota þessar greiðsluupplýsingar þegar kallað er aftur á pöntunina eða unnið úr henni í annarri rás. Gott dæmi er atburðarásin „Kaupa á netinu, sækja í verslun“. Í þessari atburðarás er greiðsluupplýsingum bætt við þegar pöntun er búin til á netinu. Síðan er kallað aftur á þær á sölustað til að innheimta greiðslukort viðskiptavinar þegar sótt er. 

Hægt er að innleiða allar atburðarásir sem lýst er í þessu efnisatriði með því að nota staðlað þróunartól greiðsluhugbúnaðar (SDK) sem Commerce býður upp á. [Dynamics 365-greiðslutengill fyrir Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) býður upp á tilbúna innleiðingu á öllum atburðarásum sem lýst er hér. 

### <a name="prerequisites"></a>Forkröfur

Sérhverri atburðarás sem lýst er í þessu efnisatriði þarf á greiðslutengli að halda sem styður greiðslur omni-rásar. Tilbúinn Ayden-tengil er einnig hægt að nota vegna þess að hann styður atburðarásirnar sem eru tiltækar í gegnum Payments SDK. Frekari upplýsingar um hvernig á að innleiða greiðslutengla og almennt um Retail SDK er að finna á [Heimasíða Retail fyrir fagfólk í upplýsingatækni og þróunaraðila](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Studdar útgáfur

Greiðslumöguleikar omni-rásar sem er lýst í þessu efnisatriði voru gefnar út sem hluti af Microsoft Dynamics 365 for Retail, útgáfu 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Tenglar fyrir „Kort til staðar“ og „Kort ekki til staðar“

Payments SDK reiðir sig á tvö sett af forritunarviðmótum fyrir greiðslur. Fyrra sett af forritunarviðmóti kallast **iPaymentProcessor**. Það er notað til að innleiða greiðslutengla fyrir „kort ekki til staðar“ sem hægt er að nota í símaveri og með verkvangi Microsoft Dynamics rafrænna viðskipta. Frekari upplýsingar um viðmótið **iPaymentProcessor** er að finna í hvítbókinni [Innleiða greiðslutengil og greiðslutæki](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf), sem sér um greiðslur. 

Seinna sett af forritunarviðmóti kallast **iNamedRequestHandler**. Það styður innleiðingu á greiðslusamþættingum „kort til staðar“ sem nota posa. Frekari upplýsingar um viðmótið **iNamedRequestHandler** er að finna í [Stofna greiðslusamþættingu fyrir greiðslustöð](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Eftirfarandi hlutar og uppsetningarskref eru nauðsynleg:

- **Samþætting rafrænna viðskipta:** Samþætting við Commerce er nauðsynleg til að styðja atburðarásir þar sem pöntunin á upptök sín í netverslun. Nánari upplýsingar um SDK-rafræn viðskipti í Retail skal sjá [Þróunartól hugbúnaðar (SDK) fyrir verkvang rafrænna viðskipta](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Í sýniútgáfuumhverfi styður tilvísun netverslunar atburðarásir fyrir greiðslu omni-rásar. 
- **Skilgreining netgreiðslna:** Uppsetning á netrás verður að innihalda tengil sem hefur verið uppfærður til að styðja greiðslur omni-rásar. Að öðrum kosti er hægt að nota tilbúinn greiðslutengil. Frekari upplýsingar um hvernig á að skilgreina Adyen-greiðslutengil fyrir netverslanir er að finna í [Adyen-greiðslutengill](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Til viðbótar við uppsetningarskref rafrænna viðskipta sem er lýst í þessu efnisatriði verður færibreytan **Leyfa að vista greiðsluupplýsingar í rafrænum viðskiptum** að vera stillt á **Rétt** í stillingum fyrir Adyen-tengil. 
- **Skilgreining á greiðslum omni-rásar:** í bakvinnslunni skal opna **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar færibreytur Commerce**. Síðan, í flipanum **Greiðslur á omni-rás**, skal stilla valkostinn **Nota greiðslur á omni-rás** á **Já**. Í Commerce, útgáfum 10.0.12 og nýrri, er þessi stilling á vinnusvæðinu **Eiginleikastjórnun**. Veljið eiginleikann **Greiðslur á Omni-rás** og smellið á **Virkja núna**. 
- **Greiðsluþjónustur:** Símaverið notar sjálfgefinn greiðslutengil á síðunni **Greiðsluþjónustur** til að vinna úr greiðslum. Til að styðja við atburðarásir á borð við „Kaupa í símaveri, sækja í verslun“ verður þessi sjálfgefni greiðslutengill að vera Adyen-greiðslutengill eða greiðslutengill sem uppfyllir kröfur innleiðingar fyrir greiðslur á omni-rás.
- **EFT-þjónusta:** Greiðslur í gegnum posa verða að vera settar upp í flýtiflipanum **EFT-þjónusta** fyrir vélbúnaðarsniðið. Adyen-tengillinn styður tilbúnar atburðarásir fyrir greiðslur á omni-rás. Aðra greiðslutengla sem styðja viðmótið **iNamedRequestHandler** er einnig hægt að nota ef þeir styðja greiðslur omni-rásar.
- **Tiltækileiki greiðslutengils:** Þegar pöntun er endurkölluð innihalda línur greiðslumáta sem eru endurkallaðar, ásamt pöntuninni, heiti greiðslutengils sem var notaður til að búa til heimildirnar sem tengjast þeirri pöntun. Þegar pöntunin er uppfyllt reynir Payments SDK að nota sama tengil og var notaður til að búa til upprunalegu heimildina. Þess vegna þarf greiðslutengill sem er með sömu eiginleika söluaðila að vera tiltækur svo hægt sé að ná í hann. 
- **Kortategundir:** Til þess að atburðarásir omni-rásar geti virkað almennilega þarf hver rás að vera með sömu uppsetningu fyrir greiðslumáta sem hægt er að nota fyrir omni-rás. Þessi uppsetning felur í sér auðkenni greiðslumáta og auðkenni kortategundar. Ef greiðslumátinn **Kort** er til dæmis með auðkennið **2** í uppsetningu netverslunar, ætti hann að vera með sama auðkennið í uppsetningu smásöluverslunar. Sama krafa á við um auðkenni korta. Ef kortanúmer **12** er stillt á **VISA** í netverslun, ætti að setja upp sama auðkennið fyrir smásöluverslunina. 
- Retail Modern POS fyrir Windows eða Android með innbyggðri vélbúnaðarstöð -eða-
- Modern POS fyrir iOS eða sölukerfi í skýinu með tengdri samnýttri vélbúnaðarstöð. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Grundvallarregla sem styður greiðslur á omni-rás

Greiðslutenglar og greiðsluvinnslur nota tákn eða tilvísanir til að vísa í samskipti sem tengjast kortagreiðslum. Þegar til dæmis óskað er eftir greiðsluheimild er tilvísun í þessa heimild útveguð. Þess vegna er hægt að vísa í heimildina síðar þegar fjármagn er sótt við uppfyllingu. Þessi heimild er einkvæm fyrir söluaðila, greiðslutengil og vinnslu. 

Ef sækja á pöntun verslun sem var búin til á netinu verður að kalla aftur á sömu greiðsluupplýsingarnar og nota þær. Þegar upprunalegar upplýsingar eru veittar sem hluti af beiðninni um að sækja greiðslu gagnvart upprunalegu heimildinni, getur greiðsluvinnslan meðhöndlað beiðnina og sótt greiðsluna. 

Til að vísa rétt í netpöntun verður greiðslutengillinn „kort ekki til staðar“ sem styður sömu vinnsluna einnig að vera tiltækur. Með þessum hætti getur sölustaðarkerfið verið með eina vinnslu fyrir greiðsluna „kort til staðar“, en það getur einnig haft aðgang að öðrum greiðslutenglum svo hann geti uppfyllt pantanir sem eru búnar til í öðrum rásum með því að nota mismunandi greiðsluvinnslur. 

## <a name="supported-scenarios"></a>Studdar aðstæður

Eftirfarandi atburðarásir fyrir greiðslu á omni-rás eru studdar:

- Kaupa á netinu, sækja í verslun
- Kaupa í símaveri, sækja í verslun
- Kaupa í verslun A, sækja í verslun B
- Kaupa í verslun A, senda til viðskiptavinar

    > [!NOTE]
    > Greiðslur sem gerðar eru í símaveri sem varpast í „Venjulegar“ greiðsluaðgerð verða að vera merktar sem **Fyrirframgreiða** = **Já** til að endurspeglast í upphæð til greiðslu þegar pöntunin er endurmerkt á sölustað. Greiðslur án forgreiðslna af gerðinni „Venjulegt“ eru ekki þekktar þegar pöntunin er afturkölluð á sölustað. 

Afbrigði þessara atburðarása eru einnig studdar. Til dæmis getur netpöntun innihaldið bæði línur sem verða sendar til viðskiptavinar og línur sem verða sóttar í verslun. Allir valmöguleikar á uppfyllingu pöntunar eru studdir í gegnum greiðslur á omni-rás. 

Eftirfarandi kaflar lýsa skrefunum fyrir hverja atburðarás og sýna hvernig á að keyra atburðarásina með því að nota sýnigögn. 

### <a name="buy-online-pick-up-in-store"></a>Kaupa á netinu, sækja í verslun

Áður en hafist er handa skal ganga úr skugga um að eftirfarandi skilyrði séu uppfyllt:

- Þú ert með tilvísun í netverslun þar sem Adyen-tengill er skilgreindur.
- Valkosturinn **Greiðslur á Omni-rás** á síðunni **Samnýttar færibreytur Commerce** er stilltur á **Satt**. Í síðari útgáfum er þessi stilling flutt yfir á vinnusvæðið **Eiginleikastjórnun** þar sem hægt er að velja eiginleikann **Greiðslur á Omni-rás** og smella á **Virkja núna**. 
- Adyen-greiðslutengill er skilgreindur fyrir Houston-afgreiðslukassann.
- Retail Modern POS fyrir Windows eða Android með innbyggðri vélbúnaðarstöð -eða-
- Modern POS fyrir iOS eða sölukerfi í skýinu með tengdri samnýttri vélbúnaðarstöð. 

Fylgdu þessum skrefum til að keyra atburðarásirnar.

1. Í tilvísun netverslunar skal stofna pöntun sem er sótt í verslun. Vertu viss um að velja verslunina **Houston**. 
2. Farðu í gegnum skrefin sem ljúka kaupum og greiddu með því að nota prufunúmer fyrir kreditkort. Þú getur fundið prufunúmer fyrir kreditkort á [Síða fyrir prufukortanúmer Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. Í Commerce skal nota runuvinnsluna **Samstilla pantanir** og dreifingaráætlunina **P-001** til að stofna pöntun í bakvinnslunni.
4. Á sölustað, á upphafsíðunni, skal velja aðgerðina **Pantanir til að sækja** til að sjá pantanir sem verða sóttar í verslun. 
5. Veldu eina eða fleiri línur úr pöntuninni sem var stofnuð í netverslun sem vísað er í og veldu síðan **Sækja**.

    Röðin er sótt úr bakvinnslunni. 

6. Þegar upplýsingar um pöntunarlínuna eru sóttar úr bakvinnslunni, og kennsl er borin á kortagreiðslu sem hægt er nota fyrir omni-rás, færðu upplýsingar um greiðslumáti er tiltækur.
7. Veldu **Nota tiltækan greiðslumáta** til að ljúka millifærslunni með því að nota kortaupplýsingarnar sem voru færðar inn í netverslun sem vísar er í.

    Pöntunarlínurnar eru hlaðnar á færslusíðunni og gjaldfallin staða er 0 (núll). 

8. Veldu flipann **Greiðslur** til að skoða línu greiðslumáta sem var sótt úr netpöntuninni. 
9. Veldu hvaða greiðslumáta sem er til að ljúka millifærslunni. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Kaupa í símaveri, sækja í verslun

1. Í Commerce, á síðunni **Notendaþjónusta**, skal færa **Karen Berg** inn í leitarstikuna og síðan velja **Leita**. 
3. Veldu **Karen Berg** í leitarniðurstöðunum.
4. Eftir að Karen hefur verið hlaðin inn á síðuna **Notendaþjónusta** skal velja **Ný sölupöntun**.
5. Á síðu nýrrar sölupöntunar skal velja **Haus** til að skoða pöntunarhaus. 
6. Á síðunni **Pöntunarhaus** skal stilla svæðið á **Miðlægt** og vöruhúsið á **Houston**.
7. Í flipanum **Afhenda** skal stilla reitinn **Flutningsmáti** á **60** fyrir sótt af viðskiptavini.
8. Veljið **Línur** og bætið síðan einni eða fleiri línum við pöntunina. 
9. Veljið **Ljúka** til að færa inn flæði pöntunarloka.
10. Flettið niður á greiðsluhlutann, veljið **Bæta við** og veljið síðan línu þar sem gerð greiðslumáta er stillt á **Kort**. 
11. Veljið plúsmerkið (**+**) til að bæta við kortagreiðslu. 
12. Færið inn upplýsingarnar fyrir prufunúmer kreditkorts sem fannst á [Síða fyrir prufukortanúmer Adyen](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) og veljið síðan **Í lagi**.

    > [!NOTE]
    > Ef kortategundin fyrir kortanúmerið sem var slegið inn er ólík þeirri tegund sem var valin þegar greiðslan var sett af stað, mun greiðslan samt fara í gegn. Hins vegar verður hún bókuð í lyklana sem er varpað í kortategundina sem var valin í skrefi 10.

12. Veljið aftur **Í lagi** til að loka svarglugganum **Greiðslur við lok pöntunar**.
13. Á síðunni **Samantekt sölupöntunar** skal velja **Senda inn**.
14. Á sölustað, á upphafsíðunni, skal velja aðgerðina **Pantanir til að sækja** til að sjá pantanir sem verða sóttar í verslun. 
15. Veldu eina eða fleiri línur úr pöntuninni sem var stofnuð í netverslun sem vísað er í og veldu síðan **Sækja**.

    Röðin er sótt úr bakvinnslunni. 

16. Þegar upplýsingar um pöntunarlínuna eru sóttar úr bakvinnslunni, og kennsl er borin á kortagreiðslu sem hægt er nota fyrir omni-rás, færðu upplýsingar um greiðslumáti er tiltækur.
17. Veldu **Nota tiltækan greiðslumáta** til að ljúka millifærslunni með því að nota kortaupplýsingarnar sem voru færðar inn í netverslun sem vísar er í.

    Pöntunarlínurnar eru hlaðnar á færslusíðunni og gjaldfallin staða er 0 (núll).

18. Veldu flipann **Greiðslur** til að skoða línu greiðslumáta sem var sótt úr netpöntuninni. 
19. Veldu hvaða greiðslumáta sem er til að ljúka millifærslunni. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Kaupa í verslun A, sækja í verslun B

1. Ræsið sölustað fyrir Houston-verslun.
2. Á síðunni **Færsla** skal bæta Karen Berg við færsluna með því að nota talnaborðið til slá inn **2001**.
3. Bætið einni eða fleiri línum við færsluna.
4. Veljið **Pantanir** til að sjá valmöguleika pöntunar.
5. Veljið **Sækja allt** og síðan, þegar beðið er um það, skal velja **Pöntun viðskiptavinar**.
6. Í leitarstikunni skal slá inn **Seattle** og síðan velja verslunina **Seattle** til að sækja. 
7. Veljið **Í lagi** til að samþykkja núverandi dagsetningu sem daginn sem pöntun verður sótt.
9. Veljið **Greitt með korti** til að hefja greiðsu.
10. Leggið fram greiðslu með korti fyrir upphæðinni sem þarf að inna af hendi fyrir innborguninni. 
11. Ljúkið greiðslu innborgunar í posanum. 
12. Eftir að greiðslan hefur verið greidd skal velja möguleikann á því að nota sama kortið til uppfyllingar og bíða eftir því að pöntunin klárist. 
13. Ræsið sölustað fyrir Seattle-verslun.
14. Á sölustað, á upphafsíðunni, skal velja aðgerðina **Pantanir til að sækja** til að sjá pantanir sem verða sóttar í verslun. 
15. Veldu eina eða fleiri línur úr pöntuninni sem var stofnuð í netverslun sem vísað er í og veldu síðan **Sækja**.

    Röðin er sótt úr bakvinnslunni. 

16. Þegar upplýsingar um pöntunarlínuna eru sóttar úr bakvinnslunni, og kennsl er borin á kortagreiðslu sem hægt er nota fyrir omni-rás, færðu upplýsingar um greiðslumáti er tiltækur.
17. Veldu **Nota tiltækan greiðslumáta** til að ljúka millifærslunni með því að nota kortaupplýsingarnar sem voru færðar inn í netverslun sem vísar er í.

    Pöntunarlínurnar eru hlaðnar á færslusíðunni og gjaldfallin staða er 0 (núll).

18. Veldu flipann **Greiðslur** til að skoða línu greiðslumáta sem var sótt úr netpöntuninni. 
19. Veldu hvaða greiðslumáta sem er til að ljúka millifærslunni. 

### <a name="buy-in-store-a-ship-to-customer"></a>Kaupa í verslun A, senda til viðskiptavinar

1. Ræsið sölustað fyrir Houston-verslun.
2. Á síðunni **Færsla** skal bæta Karen Berg við færsluna með því að nota talnaborðið til slá inn **2001**.
3. Bætið einni eða fleiri línum við færsluna.
4. Veljið **Pantanir** til að sjá valmöguleika pöntunar.
5. Veljið **Senda allt** og síðan, þegar beðið er um það, skal velja **Pöntun viðskiptavinar**.
6. Á síðu sendingaraðferðar skal velja **Venjulegt yfir nótt** og velja svo **Í lagi** til að samþykkja daginn í dag sem sendingardag. 
7. Veljið **Í lagi** til að samþykkja núverandi dagsetningu sem daginn sem pöntun verður sótt.
8. Veljið **Greitt með korti** til að hefja greiðsu.
9. Leggið fram greiðslu með korti fyrir upphæðinni sem þarf að inna af hendi fyrir innborguninni. 
10. Ljúkið greiðslu innborgunar í posanum. 
11. Eftir að greiðslan hefur verið greidd skal velja möguleikann á því að nota sama kortið til uppfyllingar og bíða eftir því að pöntunin klárist.

Þegar pöntun er sótt, pökkuð og reikningsfærð í bakvinnslu verða greiðsluupplýsingarnar sem eru veittar á sölustaðnum notaðar til að sækja fjármagnið fyrir vörunum sem verða sendar til viðskiptavinar. 

## <a name="scenario-details"></a>Upplýsingar um dæmi

Ásamt grunnatburðarásunum sem var verið að lýsa, hafa verið gerðar nokkrar endurbætur á Payments SDK til að styðja við greiðslur á omni-rás. 

### <a name="pos"></a>Sölustaður

#### <a name="single-swipedip-for-customer-orders"></a>Greiðslukortalestur fyrir pantanir viðskiptavinar

Áður en eiginleikinn fyrir greiðslur á omni-rás voru innleiddar, þegar pantanir viðskiptavina sem fólu í sér innborganir sem voru búnar til á sölustað, þurftu viðskiptavinir að renna/stinga inn greiðslukortinu tvisvar sinnum til að greiða innborgunina og einu sinni til að tákngera kortið fyrir næstu uppfyllingu á pöntun. Þegar kveikt er á eiginleika tákngervingar fyrir omni-rás verða viðskiptavinir að renna kortinu sínu einungis einu sinni til þess að bæði greiða innborgun og gefa heimild fyrir upphæðinni sem verður greidd þegar vörurnar verða uppfylltar síðar meir. Við uppfyllingu er heimilaða fjármagnið sótt. Áður en eiginleiki tákngervingar fyrir omni-rás var innleiddur var einungis endurtekið kortatákn stofnað fyrir næstu uppfyllingu pöntunar. Þess vegna var fjármagnið fyrir uppfyllingu í biðstöðu ekki heimilað, og vegna þess að þetta fjármagn var ekki haldið eftir fyrir þessi tilteknu innkaup voru minni líkur á því að hægt væri að sækja það síðar meira.

> [!NOTE]
> Stakur kortalestur er ekki studdur í Retail útgáfu 8.1.3. Pantanir viðskiptavinar í útgáfu 8.1.3 nota sama flæðið sem var notað áður en eiginleiki tákngervingar fyrir omni-rás var innleiddur. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kort sem geta ekki gefið út endurtekin kortatákn

Ekki er hægt að nota sum kort fyrir greiðslur á omni-rás vegna þess að þau styðja ekki útgáfu á endurteknum kortatáknum. Þegar pöntun er stofnuð á sölustað, ef innborgun er greidd með korti sem styður ekki endurtekin kortatákn, er fyrra flæði fyrir tákngervingu korts notað. Viðskiptavinur sem vill nota greiðslu sem verður notuð fyrir næstu uppfyllingu á pöntun verður þar af leiðandi að framvísa öðru korti. Ef annað kortið styður ekki endurtekin kortatákn verður aðgerð tákngervingar hafnað og gjaldkeri verður beðinn um að biðja um að viðskiptavinur framvísi öðru korti. 

### <a name="using-a-different-card"></a>Notkun á öðru korti

Viðskiptavinur sem kemur í verslun til að sækja pöntun hefur möguleikann á því að nota annað kort. Þegar gjaldkeri fær kvaðninguna **Nota tiltækan greiðslumáta** þegar pöntun er sótt, getur hann spurt hvort viðskiptavinur vilji nota sama kortið. Ef viðskiptavinur hefur glatað kortinu sem var notað til að búa til pöntunina og vill greiða hana með öðru korti getur gjaldkerinn valið **Nota annan greiðslumáta**. Ef viðskiptavinur kemur aftur síðar til að sækja fleiri vörur fyrir sömu pöntunina, ef upprunaleg kortaheimild er enn í gildi, getur gjaldkerinn spurt hvort viðskiptavinurinn vilji nota þetta kort.

### <a name="invalid-authorizations"></a>Ógildar heimildir

Ef kortið sem var notað til að búa til pöntun er ekki lengur í gildi, þegar valið er að sækja vörur, mun beiðni um greiðslutöku mistakast. Greiðslutengill sölustaðar reynir þá að búa til nýja heimild og sækja greiðslu með því að nota sömu kortaupplýsingar. Ef nýja heimildin eða greiðslutakan mistekst verður gjaldkeri látinn vita að ekki var hægt að vinna úr greiðslunni. Gjaldkerinn verður þá að fá nýja greiðslu frá viðskiptavini. 

### <a name="multiple-available-payments"></a>Margar tiltækar greiðslur

Þegar pöntun er sótt, sem er með marga greiðslumáta og margar línur, fær gjaldkerinn fyrst kvaðninguna **Nota tiltækan greiðslumáta**. Ef til eru mörg kort, þegar gjaldkerinn velur **Nota tiltækan greiðslumáta**, verða núverandi línur greiðslumáta sóttar þar til staðan jafnast út fyrir vörurnar sem er verið að sækja. Gjaldkerinn hefur ekki möguleikann á því að velja kortið sem á að nota fyrir vörurnar sem verið er að sækja. 

## <a name="related-topics"></a>Tengd efnisatriði

- [Algengar spurningar um greiðslur](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365-greiðslutengill fyrir Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](./cpe-bopis.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]