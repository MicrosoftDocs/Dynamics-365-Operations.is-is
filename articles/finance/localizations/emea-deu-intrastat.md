---
title: German Intrastat
description: Þetta efnisatriði inniheldur upplýsingar um Intrastat-skattskýrslu í Þýskalandi.
author: anasyash
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 50c412fdfd7118843d285cbb70e8e44847c9d4a5
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487926"
---
# <a name="german-intrastat"></a>German Intrastat

[!include [banner](../includes/banner.md)]

Síðan **Intrastat** er notuð til að útbúa og tilkynna upplýsingar um viðskipti innan landa Evrópusambandsins. Þýska Intrastat-skattskýrslan inniheldur upplýsingar um viðskipti með vörur fyrir skýrslugerð. Skýrslan er sniðin samkvæmt leiðbeiningum þýskra yfirvalda sem koma fram á síðunni [6.2 Skrár á INSTAT/XML sniði](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html).

Eftirfarandi tafla sýnir reitina sem eru innifaldir í þýsku Intrastat-skattskýrslunni.

| Svæði | Sendingar | Móttökur |
|-------------------------|-------------------------|-------------------------|
| Tímabil tilvísunar | X | X |
| Stefnukóði | X | X |
| Gjaldmiðill Intrastat-skattskýrslunnar</br>**Athugaðu:** Þessi gjaldmiðill er <em>bókhaldsgjaldmiðillinn</em>. | X | X |
| Grunnvörukóði | X | X |
| Vöruheiti | X | X |
| Kóði viðbótareiningar | X | X |
| Aðildarríki vörusendingar/áfangastaðar | X | X |
| Nettómassi | X | X |
| Magn í viðbótareiningum | X | X |
| Upprunaland |  | X |
| Upphæð reiknings | X |  |
| Tölfræðilegt gildi  | X | X |
| Eðli færslna | X | X |
| Flutningsmáti | X | X |
| Svæðiskóði</br>**Athugasemd:**</br><ul></br><li>Ef upprunaland eða landsvæði er Þýskaland og reikningurinn er fyrir sendingar er sýndur Intrastat-kóði fyrir upprunaríkið.</li></br><li>Ef upprunalandið eða landsvæðið er ekki Þýskaland og reikningurinn er fyrir sendingar er sýndur kóðinn **99**.</li></br><li>Ef reikningurinn er fyrir komur er sýndur Intrastat-kóði fyrir ríkið.</li></br></ul> | X | X |
| Höfn/Flugvöllur/Innanlandshafnarnúmer | X | X |
| Afhendingarskilmálar | X | X |


## <a name="set-up-intrastat"></a>Setja upp Intrastat

1. Settu upp kóða fyrirtækisins.

    1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
    2. Í flýtiflipanum **Erlend viðskipti og vörustjórnun**, í hlutanum **Auðkenning**, í reitinn **DVR**, skal færa inn auðkenni viðskiptasamningsins. Þetta auðkenni verður tekið með í skýrslunni.
    3. Í reitinn **VSK-undanþágunúmer útflutnings** skal færa inn virðisaukaskattsnúmer (VSK-númer) fyrirtækisins fyrir útflutning.
    4. Í reitinn **VSK-undanþágunúmer innflutnings** skal færa inn VSK-númer fyrirtækisins fyrir innflutning.
    5. Í reitinn **Intrastat-kóði** skal færa inn Intrastat-kóðann sem lögaðilanum er úthlutað.
    6. Í flýtiflipanum **Skattskráning**, í reitnum **Skattskráningarnúmer**, skal tilgreina skattskráningarnúmer fyrirtækisins.

    > [!NOTE]
    > Ef þú býrð til Intrastat-skýrslu fyrir samstarfsaðila skaltu færa inn í reitinn **Skattskráningarnúmer** skattskráningarnúmer móðurfyrirtækisins.

2. Í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), í sameiginlega eignasafninu, skaltu sækja nýjustu útgáfur af eftirfarandi stillingum fyrir rafræna skýrslugerð fyrir Intrastat-skattskýrsluna:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - INSTAT XML
    - INSTAT XML (DE)

3. Setja upp færibreytur erlendra viðskipta:

    1. Í Dynamics 365 Finance skal fara í **Skattur** > **Uppsetning** > **Færibreytur erlendra viðskipta**.
    2. Í flipanum **Intrasta**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat XML (DE)**.
    3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
    4. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.
    5. Í reitnum **Færslukóði** skal velja færslukóðann fyrir flutning á eignum. Þú notar þennan kóða fyrir færslur sem skapa raunverulegar eða áætlaðar færslur á eignum gegn greiðslu (fjárhagslegri eða annars konar greiðslu). Þú getur líka notað það til leiðréttinga.
    6. Í reitnum **Kreditnóta** skal velja færslukóðann fyrir vöruskil.
    7. Í reitnum **Starfskraftur** skal velja tengiliðinn fyrir Intrastat skýrslu. Einnig er hægt í flipanum **Tengiliður** að færa inn eða velja gildi í reitunum **Heiti**, **Símanúmer**, **Fax**, **Tölvupóstur** og **Veffang**. Þessir reitir eru hafðir með í skýrslunni.
    8. Í reitnum **Yfirvald** skal velja Intrastat-yfirvald.
    9. Farðu í **Skattur** > **Óbeinir skattar** > **Söluskattur** > **Yfirvöld söluskatts** og færðu inn upplýsingar fyrir Intrastat-yfirvöldin sem þú valdir í skrefinu á undan:

       - Kenni yfirvalda
       - Aðsetur
       - Tengslaupplýsingar

    10. Í flipanum **Eiginleikar lands/svæðis**, í reitnum **Land/svæði**, skal gefa upp öll lönd eða svæði sem fyrirtækið þitt á í viðskiptum við. Fyrir hvert land eða svæði, í reitnum **Gerð lands/svæðis**, velja **ESB** þannig að landið eða svæðið birtist í Intrastat skýrslunni.

4. Setja upp svæðiskóða.

    1. Farðu í **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Aðsetur** > **Uppsetning aðseturs**.
    2. Í flipanum **Ríki/hérað**, í reitnum **Land/svæði** skal velja **DEU** og síðan velja **Nota síu**.
    3. Í hnitanetinu skal velja ríkið. Því næst skal færa einkvæman Intrastat-kóða inn í reitinn **Intrastat-kóði**.

5. Settu upp upprunanetfang fyrir vöru.

    1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
    2. Í hnitanetinu skal velja afurðina.
    3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Upprunaland**, skal velja viðeigandi **DEU**.

6. Farðu í **Skattur**  >  **Uppsetning**  >  **Erlend viðskipti**  >  **Intrastat-þjöppun** og veldu reitina sem á að bera saman þegar Intrastat-upplýsingar eru teknar saman. Fyrir Intrastat í Þýskalandi skal velja eftirfarandi reiti:

    - Vara
    - Land/svæði
    - Leiðrétting
    - Stefna
    - Afhendingarskilmálar
    - Reikningur
    - Upprunaland/-svæði
    - Afh.staður
    - Land/svæði sendanda
    - Staða sendanda
    - Vinnsla talnagagna
    - Færslukóði
    - Flutningur
    - Skattundanþágunúmer

### <a name="intrastat-transfer"></a>Intrastat-flutningur

Á síðunni **Intrastat** á aðgerðasvæðinu er hægt að velja **Flutningur** til að flytja sjálfkrafa upplýsingarnar um viðskipti innan samfélags úr sölupöntunum, textum með frjálsum texta, innkaupapöntunum, lánardrottnareikningum **,** innhreyfingarskjölum afurða lánardrottins, verkreikningum og flutningspöntunum. Aðeins skjöl sem hafa ESB-land sem land eða svæði áfangastaðar (fyrir sendingar) eða vörusendingu (fyrir komur) verða flutt.

Einnig er hægt að færa færslur handvirkt inn með því að velja **Ný** á aðgerðasvæðinu.

### <a name="generate-an-intrastat-report"></a>Mynda Intrastat-skýrslu

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
3. Í svarglugganum **Intrastat skýrsla** skal stilla eftirfarandi reiti.

    | Svæði | lýsing |
    |-------------------------|-------------------------|
    | Frá degi | Veldu upphafsdagsetningu fyrir skýrsluna. |
    | Til dags. | Veldu lokadagsetningu fyrir skýrsluna. |
    | Mynda skrá | Stilltu þennan valkost á **Já** til að búa til .xml-skrá. |
    | Skrárnafn | Hafa reitinn auðann. Skráarheitið er búið til sjálfkrafa og samanstendur af gildi XML-merkis **&lt;envelopeId&gt;** ásamt skráarendingunni **.xml**.</br>Gildið **&lt;envelopeId&gt;** er samtenging af eftirfarandi einingum í þessari röð:</br><ol type="1"></br><li>Gildi merksins **&lt;interchangeAgreementId&gt;**</li></br><li>Bandstrik (-)</li></br><li>Gildi merkisins **&lt;referencePeriod í YYYYMM&gt;**</li></br><li>Bandstrik (-)</li></br><li>Gildi **&lt;Envelope/DateTime/date in YYYYMMDD&gt;** merkisins</li></br><li>Bandstrik (-)</li></br><li>Gildi merksins **&lt;Envelope/DateTime/date in hhmm&gt;**</li></br></ol> |
    | Stefna | <ul></br><li>Veldu **Komur** til að tilkynna um komur innan samfélags.</li></br><li>Veldu **Sendingar** til að tilkynna um sendingar innan samfélags.</li></br><li>Veldu **Bæði** til að tilkynna bæði um komur og sendingar.</li></br></ul> |
    | Skattskráningarnúmer | Færðu inn skattskráningarnúmerið sem á að nota til að mynda auðkenniskóða sendanda, ef númerið er frábrugðið skattskráningarnúmeri lögaðilans. |


## <a name="example"></a>Dæmi

Dæmið sýnir hvernig á að bóka komur og sendingar fyrir Intrastat. Það notar **DEMF** lögaðilann.

1. Í [LCS](https://lcs.dynamics.com/Logon/Index), í sameiginlega eignasafninu, skaltu sækja nýjustu útgáfur af eftirfarandi stillingum fyrir rafræna skýrslugerð fyrir Intrastat-skattskýrslusniðið:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - Intrastat XML
    - Intrastat XML (DE)

2. Stofnaðu færslukóða.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færslukóðar**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í reitinn **Færslukóði** skal færa inn **21**.
    4. Í reitinn **Heiti** skal færa inn **Vöruskil**.
    5. Í aðgerðarúðunni skal velja **Vista**.

3. Setja upp auðkennisnúmer yfirvalda.

    1. Farðu í **Skattur** > **Óbeinir skattar** > **Söluskattur** > **Yfirvald söluskatts**.
    2. Á listanum velurðu **TA**.
    3. Í reitinn **Auðkenning yfirvalds** skal færa inn **123**.

4. Setja upp svæðiskóða.

    1. Farðu í **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Aðsetur** > **Uppsetning aðseturs**.
    2. Í flipanum **Ríki/hérað**, í reitnum **Land/svæði** skal velja **DEU** og síðan velja **Nota síu**.
    3. Í hnitanetinu skal velja **BE** og því næst í reitinn **Intrastat-kóði** skal færa inn **11**.
    4. Í aðgerðarúðunni skal velja **Vista**.

5. Setja upp færibreytur erlendra viðskipta.

    1. Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta**.
    2. Í flýtiflipanum **Intrastat**, í flýtiflipanum **Almennt**, í reitnum **Færslukóði**, skal velja **11**.
    3. Í reitnum **Kreditnóta** skal velja **21**.
    4. Í reitnum **Yfirvald** skal velja **TA**.
    5. Í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **INSTAT-XML (DE)**.
    6. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
    7. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, skal ganga úr skugga um að **Intrastat** sé valið.
    8. Í flipanum **Eiginleikar lands/svæðis** skal velja **Nýtt**.
    9. Í reitnum **Land/svæði viðskiptafélaga** skal velja **FRA**.
    10. Í reitnum **Land/svæði** skal velja **ESB**.

6. Úthlutaðu vörukóða á afurð og stilltu uppruna afurðar. Reitirnir **Vörukóði**, **Upprunaland/-svæði** og **Upprunaríki** verða þá sjálfkrafa stilltir á sölupantanir og innkaupapantanir þegar þú velur afurðina.

    1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
    2. Í hnitanetinu skal velja **D0001**.
    3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **920 20 34**.
    4. Í hlutanum **Uppruni**, í reitnum **Land/svæði**, skal velja **DEU**.
    5. Í flýtiflipanum **Stjórna birgðum**, í hlutanum **Þyngdarmælingar**, í reitinn **Nettóþyngd**, skal færa inn **12**.
    6. Í aðgerðarúðunni skal velja **Vista**.

7. Úthlutaðu flutningi á flutningsmáti. Flutningskóðinn verður þá sjálfkrafa stilltur á pöntunum þegar þú velur flutningsmátann.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Flutningsmátar**.
    2. Á listanum velurðu **10**.
    3. Í flýtiflipanum **Erlend viðskipti**, í reitnum **Flutningur**, skal velja **01**.

8. Stofnaðu sölupöntun með viðskiptavin innan ESB.

    1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-012**.
    4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
    5. Í reitnum **Vöruhús** skal velja **11**.
    6. Veldu **Í lagi**.
    7. Í flipanum **Haus**, í flýtiflipanum **Erlend viðskipti**, í reitnum **Gátt**, skal velja **53**.
    8. Í reitnum **Tölfræðilegt ferli** skal velja **31710**.
    9.  Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun** **línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **10**.
    10. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, skal ganga úr skugga um að reitirnir **Færslukóði**, **Flutningur**, **Varningur** og **Upprunaland/-svæði** séu sjálfkrafa stilltir.
    11. Í aðgerðarúðunni skal velja **Vista**.
    12. Á aðgerðasvæðinu, í flipanum **Reikningur**, í hlutanum **Mynda** skal velja á **Reikningur**.
    13. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
    14. Veldu svo **Í lagi** til að bóka reikninginn.

9.  Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Velja **Síu**.
    5. Í svarglugganum **Intrastat-sía**, í flipanum **Svið**, skal velja fyrstu línuna og ganga úr skugga um reiturinn **Reitur** er stilltur á **Dagsetning**.
    6. Í reitnum **Skilyrði** skal velja daginn í dag.
    7. Veldu **Í lagi** til að loka svarglugganum **Intrastat-sía**.
    8. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Línan táknar sölupöntunina sem þú stofnaðir fyrr.

        ![Lína sem táknar sölupöntunina á Intrastat-síðunni](media/intrastat_deu_1.png)

10. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um sölupöntun á almenna flipa Intrastat-síðunnar](media/intrastat_deu_2.png)

11. Stofna kreditnótu með því að nota sölupöntun.

    1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-012**.
    4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
    5. Í reitnum **Vöruhús** skal velja **11**.
    6. Í flipanum **Haus**, í flýtiflipanum **Erlend viðskipti**, í reitnum **Gátt**, skal velja **53**.
    7. Í reitnum **Tölfræðilegt ferli** skal velja **31710**.
    8. Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun** **línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **-2**.
    9. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, í reitnum **Færslukóði**, skal velja **21**.
    10. Gakktu úr skugga um að reitirnir **Flutningur**, **Varningur** og **Upprunaland/-svæði** séu stilltir sjálfkrafa.
    11. Í aðgerðarúðunni skal velja **Vista**.
    12. Á aðgerðasvæðinu, í flipanum **Reikningur**, í hlutanum **Mynda** skal velja á **Reikningur**.
    13. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
    14. Veldu svo **Í lagi** til að bóka reikninginn.

12. Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Nýrri línu þar sem reiturinn **Stefna** er stilltur á **Komur** hefur verið bætt við.            
        Þessi lína stendur fyrir efnisleg skil á vörum.

        ![Lína fyrir efnisleg skil á vörum á Intrastat-síðunni](media/intrastat_deu_3.png)

13. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um efnisleg skil á vörum í flipanum almennt á Intrastat-síðunni](media/intrastat_deu_4.png)

14. Stofnaðu leiðréttingu með því að nota sölupöntun:

    1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-012**.
    4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
    5. Í reitnum **Vöruhús** skal velja **11**.
    6. Í flipanum **Haus**, í flýtiflipanum **Erlend viðskipti**, í reitnum **Gátt**, skal velja **53**.
    7. Í reitnum **Tölfræðilegt ferli** skal velja **31710**.
    8. Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun** **línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **-3**.
    9. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, í reitnum **Færslukóði**, skal velja **11**.
    10. Gakktu úr skugga um að reitirnir **Flutningur**, **Varningur** og **Upprunaland/-svæði** séu stilltir sjálfkrafa.
    11. Í aðgerðarúðunni skal velja **Vista**.
    12. Gakktu úr skugga um að reiturinn **Færslukóði** sé stilltur á 11.
    13. Á aðgerðasvæðinu, í flipanum **Reikningur**, í hlutanum **Mynda** skal velja á **Reikningur**.
    14. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
    15. Veldu svo **Í lagi** til að bóka reikninginn.

15. Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna:

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Nýrri línu þar sem gátmerki birtist í dálknum **Leiðrétting** hefur verið bætt við.

        ![Lína fyrir leiðréttingu á Intrastat síðunni](media/intrastat_deu_5.png)

16. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um leiðréttinguna í flipanum almennt á Intrastat-síðunni](media/intrastat_deu_6.png)

17. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
18. Í svarglugganum **Intrastat skýrsla**, í flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, skal velja mánuð sölupöntunarinnar sem var stofnuð.
19. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**.
20. Í reitinn **Skráarheiti** skal færa inn nauðsynlegt heiti.
21. Veldu **Í lagi** og farðu yfir skýrsluna sem er mynduð. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

    | **Nafn**                  | **Sölureikningur**  |   **Leiðrétting**   | **Kreditnóta** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Hátalari            | Hátalari            | Hátalari         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

