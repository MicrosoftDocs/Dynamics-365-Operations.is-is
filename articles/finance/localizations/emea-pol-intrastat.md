---
title: Pólskt Intrastat
description: Þessi grein inniheldur upplýsingar um Intrastat-skýrslugerð í Póllandi.
author: AdamTrukawka
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 473581fa4f3f1e8cac06d5748f28116e6615215e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281643"
---
# <a name="polish-intrastat"></a>Pólskt Intrastat

[!include[banner](../includes/banner.md)]

Síðan **Intrastat** er notuð til að útbúa og tilkynna upplýsingar um viðskipti innan landa Evrópusambandsins. Pólska Intrastat-skattskýrslan inniheldur upplýsingar um viðskipti með vörur fyrir skýrslugerð.

Eftirfarandi reitir eru innifaldir í pólsku Intrastat-skattskýrslunni: Allir reitirnir eru innifaldir við komur og sendingar nema fyrir **RodzajTransportu** (flutningsmáti) og **KrajPochodzenia** (land eða svæði uppruna) sem eru ekki hluti af sendingum og **IdKontrahenta** (erlent VSK-númer viðskiptavinar) sem er ekki haft með í komum.

| Nafn svæðis | Lýsing |
|-------------------------|-------------------------|
| Deklaracja Data | Dagsetning stofnunar skjalsins. |
| Miesiac | Viðmiðunarmánuður skýrslunnar. |
| Rok | Viðmiðunarár yfirlýsingarinnar. |
| Númer | Yfirlýsingarnúmerið á viðmiðunartímabilinu. |
| Wersja | Útgáfunúmer skýrslunnar. |
| NrWlasny | Kenni skýrslu. Gildinu er sjálfkrafa myndað. |
| Gerð | Stefna skýrslunnar</br><li>Fyrir aðsent er prentað „P“.</li><li>Fyrir sendingar er „W“ prentað.</li> |
| Rodzaj | Gerð skýrslu. Gildi gefur til kynna hvort skýrslan sé upprunaleg skýrsla eða leiðréttingarskýrsla. |
| UC | Einingarkóðinn sem Intrastat-skattskýrslan er send til. Gildið er tilgreint í reitnum **Skattundanþágunúmer** í hlutanum **Virðisaukaskattur** í flipanum **Umboðsaðili** á síðunni **Færibreytur erlendra viðskipta**. |
| Nazwa | Heiti fyrirtækisins. |
| Miejscowosc, UlicaNumer, KodPocztowy | Fullt heimilisfang lögaðilans. |
| Nip | Pólska skattnúmerið (VSK-auðkenni). |
| Regon | Pólska tölfræðinúmerið (fyrirtækjanúmer). |
| LacznaWartoscFaktur | Samtala reikningsgilda. |
| LacznaWartoscStatystyczna | Samtala tölfræðilegra gilda. |
| LacznaLiczbaPozycji | Heildarfjöldi vara. |
| PozId | Númeraröð tiltekinna vara. |
| OpisTowaru | Viðskiptaheiti hrávörunnar. |
| KrajPochodzeniaWysylki | Kóði Alþjóðlegu staðlastofnunarinnar (ISO) fyrir land eða svæði mótaðilans. |
| WarunkiDostawy | Intrastat-kóðinn fyrir afhendingarskilmálana. |
| RodzajTransakcji | Kóðinn sem segir til um eðli færslunnar. Pólsk fyrirtæki nota tveggja stafa færslukóða. |
| KodTowarowy | Átta stafa vörukóði samkvæmt sameinaða nafnakerfinu. |
| RodzajTransportu | Intrastat-kóðinn fyrir flutningsmátann. |
| KrajPochodzenia | ISO-kóðinn fyrir landið eða svæðið þar sem hrávörurnar voru framleiddar. |
| MasaNetto | Nettómassinn er í heilum kílóum. |
| IloscUzupelniajacaJm | Magn í viðbótarmælieiningu, í heilum tölum. |
| WartoscFaktury | Reikningsvirði allra færslna sem falla undir eina vöru. |
| WartoscStatystyczna | Tölfræðilega gildið. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | Fornafn og eftirnafn, símanúmer, faxnúmer og netfang einstaklingsins sem sendir inn skýrsluna. |
| IdKontrahenta | Erlent VSK-númer viðskiptavinar í aðildarríki ESB. |


## <a name="set-up-intrastat"></a>Setja upp Intrastat

Flyttu inn nýjustu útgáfuna af eftirfarandi skilgreiningum fyrir rafræna skýrslugerð úr altæku geymslunni:

   - Intrastat-líkan
   - Intrastat-skýrsla
   - Intrastat (PL)

Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Setja upp VSK-auðkenni og fyrirtækjanúmer eigin fyrirtækis

### <a name="create-registration-types-for-company-codes"></a>Stofna skráningargerðir fyrir fyrirtækjakóða

Þú verður að búa til tvær skráningargerðir fyrir fyrirtækiskóða: eina fyrir VSK-númer (NIP-kóða) og eina fyrir fyrirtækisnúmer (Regon-kóða).

1. Opnið **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Skráningargerðir** > **Skráningargerðir**.
2. Veldu **Nýtt** á aðgerðasvæðinu til að búa til skráningargerð fyrir VSK-númer.
3. Í svarglugganum **Sláðu inn upplýsingar um skráningargerð** í reitnum **Heiti** skal slá inn heiti fyrir nýja skráningargerð. Til dæmis er slegið inn **NIP**.
4. Í reitnum **Land/svæði** skal velja **POL**.
5. Velja **Stofna**.
6. Veldu **Nýtt** á aðgerðasvæðinu til að búa til skráningargerð fyrir fyrirtækisnúmer.
7. Í svarglugganum **Sláðu inn upplýsingar um skráningargerð** í reitnum **Heiti** skal slá inn heiti fyrir nýja skráningargerð. Til dæmis er slegið inn **Svæði**.
8. Í reitnum **Land/svæði** skal velja **POL**.
9. Velja **Stofna**.

### <a name="match-the-registration-types-with-registration-categories"></a>Samsvörun skráningartegunda við skráningarflokka

1. Opnið **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Skráningargerðir** > **Skráningarflokkar**.
2. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til tengil á milli hverrar skráningargerðar sem voru búnar til og skráningarflokks.

    - Fyrir skráningargerðina fyrir VSK-númerið (NIP-kóði) velur þú skráningarflokkinn **VSK-númer**.
    - Fyrir skráningargerð fyrir fyrirtækisnúmerið (Regon-kóða) skal velja skráningarflokkinn **Fyrirtækisnúmer (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Setja upp VSK-auðkenni og fyrirtækjanúmer eigin fyrirtækis

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Í hnitanetinu skal velja fyrirtæki notanda.
3. Í aðgerðarúðunni velurðu **Skráningarkenni**.
4. Á flýtiflipanum **Skráningarkenni** skal velja **Bæta við**.
5. Í svæðinu **Skráningargerð** skal velja eina af skráningargerðunum sem þú bjóst til áður.
6. Sláðu inn VSK-númer (NIP-kóða) fyrirtækisins eða fyrirtækisnúmer (Regon-kóða) eftir því hvaða skráningargerð var valin í fyrra skrefi.
7. Endurtakið skref 4 til 6 fyrir hina skráningargerðina sem búið var að búa til.

## <a name="set-up-a-company-address"></a>Setja upp aðsetur fyrirtækis

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Í hnitanetinu skal velja fyrirtæki notanda.
3. Í flipanum **Aðsetur** skal velja **Breyta**.
4. Í svarglugganum **Breyta aðsetri**, í reitnum **Póstnúmer** skal velja póstnúmer fyrirtækisins.
5. Í reitinn **Gata** er slegið inn heimilisfang notanda.
6. Í reitnum **Borg** skal velja viðeigandi borg.

## <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Opnið **Skattur** > **Uppsetning** > **Færibreytur erlendra viðskipta**.
2. Í flipanum **Intrasta**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat (PL)**.
3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
4. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.
5. Í reitnum **Færslukóði** skal velja færslukóðann fyrir flutning á eignum. Þú notar þennan kóða fyrir færslur sem búa til raunverulegar eða áætlaðar færslur á eignum gegn greiðslu (fjárhagslegri eða annars konar greiðslu). Þú getur líka notað það til leiðréttinga. Fyrirtæki í Póllandi nota tveggja tölustafa færslukóða.
6. Í reitnum **Kreditnóta** skal velja færslukóðann fyrir vöruskil.
7. Í flipanum **Eiginleikar lands/svæðis**, í reitnum **Land/svæði**, skal gefa upp öll lönd eða svæði sem fyrirtækið þitt á í viðskiptum við. Fyrir hvert land sem er hluti af ESB skal velja **ESB** í reitnum **Gerð lands/svæðis**, þannig að landið birtist í Intrastat skýrslunni. Í reitnum **Gerð lands/svæðis** skal velja **Innlent** fyrir Pólland.
8. Í flipanum **Umboðsaðili**, í flýtiflipanum **Umboðsaðili**, í hlutanum **Virðisaukaskattur**, á svæðinu **Skattundanþágunúmer**, skal færa inn **420000** til að gefa til kynna einingarkóðann sem Intrastat-skattskýrslan er stíluð á.
9. Í flipanum **Tengiliður** skal færa inn heiti, símanúmer, faxnúmer og netfang einstaklingsins sem sendi inn skýrsluna.
10. Í flipanum **Númeraraðir**, í reitnum **Kóði númeraraðar** fyrir tilvísunina **Númer XML-skráar**, skal tilgreina samfellda númeraröð sem er með hámark níu stafi. Þessi reitur er notaður til að búa sjálfkrafa til gildi fyrir reitinn **Kenni skýrslu** í Intrastat-skýrslunni.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Setja upp færibreytur afurðar fyrir Intrastat-skattskýrsluna

1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
2. Í hnitanetinu skal velja afurð.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja vörukóðann. Heiti vörunnar verður prentað í reitinn **Lýsing á vörum** í Intrastat-skýrslunni.
4. Í hlutanum **Uppruni**, í reitnum **Land/svæði**, skal velja upprunaland eða -svæði afurðarinnar.
5. Í flýtiflipanum **Stjórna birgðum**, í reitnum **Nettóþyngd**, skal færa inn þyngd afurðar í kílógrömmum.

## <a name="set-up-compression-of-intrastat"></a>Uppsetning Intrastat-þjöppunar

-   Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Intrastat-þjöppun**, og veljið reitina sem á að bera saman þegar Intrastat-upplýsingar eru teknar saman. Fyrir Intrastat í Póllandi skal velja eftirfarandi reiti:

    - Vara
    - Færslukóði
    - Upprunaland/-svæði
    - Flutningur
    - Afhendingarskilmálar
    - Land/svæði sendanda
    - Land/svæði
    - Leiðrétting
    - Skattundanþágunúmer
    - Stefna
    - Reikningur

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Setja upp flutningsleið og afhendingarskilmála

1.  Settu upp flutningskóða.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Flutningsmáti**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í svæðinu **Flutningur** er færður inn einkvæmur kóði. Pólsk fyrirtæki nota eins stafs flutningskóða.

2.  Setja upp Intrastat-kóða afhendingarmáta.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Afhendingarskilmálar**.
    2. Í hnitanetinu skal velja afhendingarskilmála.
    3. Í flýtiflipann **Almennt**, í reitinn **Intrastat-kóði**, skal færa inn einkvæman kóða.

## <a name="intrastat-transfer"></a>Intrastat-flutningur

Á síðunni **Intrastat** á aðgerðasvæðinu er hægt að velja **Flutningur** til að flytja sjálfkrafa upplýsingarnar um viðskipti innan samfélags úr sölupöntunum, textum með frjálsum texta, innkaupapöntunum, lánardrottnareikningum, innhreyfingarskjölum afurða lánardrottins, verkreikningum og flutningspöntunum. Aðeins skjöl sem hafa ESB-land sem land eða svæði áfangastaðar eða vörusendingar verða flutt.

Einnig er hægt að færa færslur handvirkt inn með því að velja **Ný** á aðgerðasvæðinu.

### <a name="generate-an-intrastat-report"></a>Mynda Intrastat-skýrslu

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Úttak** &gt; **Skýrsla**.
3. Í svarglugganum **Intrastat skýrsla** skal stilla eftirfarandi reiti.

    | Svæði | Lýsing |
    |-------------------------|-------------------------|
    | Frá dags. | Veldu upphafsdagsetningu fyrir skýrsluna. |
    | Mynda skrá | Stilltu þennan valkost á **Já** til að búa til .xml-skrá fyrir Intrastat-skýrsluna. |
    | Skráarheiti | Færið inn heiti .xml-skráarinnar. |
    | Búa til skýrslu | Stilltu þennan valkost á **Já** til að búa til .xlsx-skrá fyrir Intrastat-skýrsluna. |
    | Heiti skýrsluskráar | Færðu inn heiti .xlsx-skráar. |
    | Stefna | Veldu **Komur** til að fá skýrslu um komur innan samfélags.</br>Veldu **Sendingar** til að fá skýrslu um sendingar innan samfélags. |
    | Lýsing kennimerkis | Auðkenni skjalsins er búið til sjálfkrafa og hægt er að uppfæra það. |
    | Gerð skýrslu | Veldu **Yfirlýsing** fyrir upprunalega yfirlýsingu.</br>Veldu **Skýrsluleiðrétting - skipti** fyrir leiðréttingarskýrslu sem á að koma í staðinn fyrir fyrirliggjandi skýrslu, áður innsendri upprunaskýrslu eða leiðréttingarskýrslu. |
    | Borg skjalastofnunar | Sláið inn gildið sem á að prenta í reitinn **Miejscowosc** í Intrastat-skattskýrslunni. |
    | Dagsetning skjalastofnunar | Færðu inn gildið sem á að prenta í reitinn **Deklaracja Data** í Intrastat-skattskýrslunni. |
    | Númer skjals | Færðu inn gildið sem á að prenta í reitinn **Numer** í Intrastat-skattskýrslunni. |
    | Útgáfa skjals | Sláið inn gildið sem á að prenta í reitinn **Wersja** í Intrastat-skattskýrslunni. |

4. Veldu **Í lagi** og farðu yfir myndaða skýrslu.

## <a name="example"></a>Dæmi

Dæmið sýnir hvernig á að bóka komur og sendingar fyrir Intrastat með lögaðilanum **DEMF**.

### <a name="preliminary-setup"></a>Bráðabirgða uppsetning

Flyttu inn nýjustu útgáfu af eftirfarandi skilgreiningum rafrænnar skýrslugerðar:

   - Intrastat-líkan
   - Intrastat-skýrsla
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Setja upp aðsetur fyrirtækis

1. Farðu í **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Aðsetur** > **Uppsetning aðseturs**.
2. Á flipanum **Borg** velurðu **Ný**.
3. Í reitnum **Land/svæði** skal velja **POL**.
4. Í reitnum **Borg** skal slá inn **Varsjá**.
5. Á flipanum **Póstnúmer** velur þú **Nýtt**.
6. Í reitnum **Land/svæði** skal velja **POL**.
7. Í reitnum **Borg** skal velja **Varsjá**.
8. Í reitnum **Póstnúmer** skal slá inn **00-844**.
9. Farðu í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar** og veldu lögaðilann **DEMF**.
10. Í flýtiflipanum **Aðsetur** skal velja **Breyta**.
11. Í reitnum **Land/svæði** skal velja **POL**.
12. Í reitnum **Póstnúmer** skal velja **31-111**.
13. Í reitinn **Gata** er slegið inn **Statystyczna 22/1**.
14. Í reitnum **Borg** skal velja **Varsjá**.
15. Veldu **Í lagi**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Setja upp VSK-auðkenni og fyrirtækjanúmerakóða eigin fyrirtækis

### <a name="create-registration-types-for-company-codes"></a>Stofna skráningargerðir fyrir fyrirtækjakóða

1. Opnið **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Skráningargerðir** > **Skráningargerðir**.
2. Veldu **Nýtt** á aðgerðasvæðinu til að búa til skráningargerð fyrir VSK-númer (NIP-kóði).
3. Í svarglugganum **Færa inn upplýsingar um skráningargerð**, í reitinn **Heiti**, skal slá inn **NIP**.
4. Í reitnum **Land/svæði** skal velja **POL**.
5. Velja **Stofna**.
6. Veldu **Nýtt** á aðgerðasvæðinu til að búa til skráningargerð fyrir fyrirtækisnúmer (svæðiskóði).
7. Í svarglugganum **Færa inn upplýsingar um skráningargerð**, í reitinn **Heiti**, skal slá inn **Regon**.
8. Í reitnum **Land/svæði** skal velja **POL**.
9. Velja **Stofna**.

### <a name="match-the-registration-types-with-registration-categories"></a>Samsvörun skráningartegunda við skráningarflokka

1. Opnið **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Skráningargerðir** > **Skráningarflokkar**.
2. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til tengil á milli hverrar skráningargerðar sem voru búnar til og skráningarflokks.

    - Fyrir skráningargerðina **NIP** skal velja **VSK-númer** skráningarflokk.
    - Fyrir skráningargerðina **Regon** skal velja skráningarflokkinn **Fyrirtækiskenni (COID)**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Setja upp VSK-auðkenni og fyrirtækjanúmer eigin fyrirtækis

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Í hnitanetinu skal velja **DEMF**.
3. Í aðgerðarúðunni velurðu **Skráningarkenni**.
4. Á flýtiflipanum **Skráningarkenni** skal velja **Bæta við**.
5. Í reitnum **Skráningargerð** skal velja **NIP**.
6. Í reitinn **Skráningarnúmer** skal færa inn **1234567890**.
7. Veljið **Bæta við**.
8. Í reitnum **Skráningargerð** skal velja **Regon**.
9. Í reitinn **Skráningarnúmer** skal færa inn **12345678901234**.

### <a name="set-up-a-number-sequence-code"></a>Setja upp kóða númeraraðar

1. Farðu í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðir**.
2. Á aðgerðasvæðinu, í flipanum **Númeraröð**, í flokknum **Ný**, skal velja **Númeraröð**.
3. Á flýtiflipanum **Auðkenni**, í reitnum **Kóði númeraraðar**, skal færa inn **XML\_skrá**.
4. Á flýtiflipanum **Umfangsbreytur**, í reitnum **Umfang** skal velja **Fyrirtæki**.
5. Í reitnum **Fyrirtæki** er **DEMF** valið.
6. Á flýtiflipanum **Hlutar**, í reitnum **Lengd** fyrir hlutann **Bók- og tölustafir** slærðu inn **4**.
7. Í flýtflipanum **Almennt**, í hlutanum **Uppsetning**, skal stilla valkostinn **Samfellt** á **Nei**.
8. Í hlutanum **Númeraúthlutun** í reitnum **Stærst** skal færa inn **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta**.
2. Í flipanum **Intrastat** á flýtiflipanum **Almennt** í **Færslu** **kóði** reitnum velurðu **11**.
3. Í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat (PL)**.
4. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
5. Í flýtiflipanum **Stigveldi vörukóða** skal staðfesta að svæðið **Tegundastigveldi** sé stillt á **Intrastat**.
6. Í flipanum **Eiginleikar lands/svæðis** skal velja **Nýtt**.
7. Í reitnum **Land/svæði viðskiptafélaga** skal velja **POL**. Í reitnum **Gerð lands/svæðis** skal síðan velja **Innlent**.
8. Í reitnum **Land/svæði viðskiptafélaga** skal velja **DEU**. Í reitnum **Gerð lands/svæðis** skal síðan velja **ESB**.
9. Á flipanum **Fulltrúi**, á flýtiflipanum **Fulltrúi**, í hlutanum **Virðisaukaskattur**, á svæðinu **Skattundanþágunúmer**, skal færa inn **420000**.
10. Á flipanum **Tengiliður**, í reitnum **Nafn**, er slegið inn **Manish Chopra**.
11. Í reitinn **Sími** er fært inn **425-555-5068**.
12. Í reitinn **Faxnúmer** er slegið inn **425-555-5049**.
13. Í reitinn **Netfang** skal færa inn **manishc@contoso.com**.
14. Í flipanum **Númeraraðir**, í reitnum **Kóði númeraraðar** fyrir tilvísunina **Númer XML-skráar** skal velja **XML\_skrá**.

### <a name="set-up-product-information"></a>Setja upp afurðarupplýsingar

1. Farið í **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar** **afurðir**.
2. Í hnitanetinu skal velja **D0001**.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **100 200 30**.
4. Í flýtiflipanum **Stjórna birgðum**, í hlutanum **Þyngdarmælingar**, í reitinn **Nettóþyngd**, skal færa inn **2**.
5. Í aðgerðarúðunni skal velja **Vista**.
6. Í hnitanetinu skal velja **D0003**.
7. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **100 200 30**.
8. Í hlutanum **Uppruni**, í reitnum **Land/svæði**, skal velja **DEU**.
9. Í flýtiflipanum **Stjórna birgðum**, í hlutanum **Þyngdarmælingar**, í reitinn **Nettóþyngd**, skal færa inn **5**.
10. Í aðgerðarúðunni skal velja **Vista**.

### <a name="change-the-site-address"></a>Breyta aðsetri svæðis

1. Farðu í **Warehouse management** > **Setja upp** > **Vöruhús** > **Svæði**.
2. Í hnitanetinu skal velja **1**.
3. Í flýtiflipanum **Aðsetur** skal velja **Breyta**.
4. Í svarglugganum **Breyta aðsetri**, í reitnum **Land/svæði**, skal velja **POL**.
5. Veldu **Í lagi**.

### <a name="set-up-a-transport-method"></a>Setja upp flutningsaðferð

1. Stofna flutningsaðferð.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Flutningsmáti**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í reitinn **Flutningur** er **3** fært inn.
    4. Í reitinn **Lýsing** skal færa inn **Flutningur á vegum**.

2. Setja nýja flutningsmátann í afhendingarmáta. Á þennan hátt setur þú upp sjálfgefin gildi sem eru notuð fyrir flutningsmátann þegar samsvarandi afhendingarmáti er valinn.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Flutningsmátar**.
    2. Í hnitanetinu skal velja **10**.
    3. Í flýtiflipanum **Erlend viðskipti**, í reitnum **Flutningur**, skal velja **3**.

3. Veljið sjálfgefinn afhendingarmáta viðskiptavinar.

    1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
    2. Í hnitanetinu skal velja **DE-016**.
    3. Í flýtiflipanum **Reikningur og afhending**, í reitnum **Afhendingarmáti**, skal velja **10**.

4. Veljið sjálfgefinn afhendingarmáta fyrir lánardrottinn.

    1. Farið í **Viðskiptaskuldir**  >  **Lánardrottnar**  >  **Allir lánardrottnar**.
    2. Í hnitanetinu skal velja **DE-001**.
    3. Í flýtiflipanum **Reikningur og afhending**, í reitnum **Afhendingarmáti**, skal velja **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Setja upp kóða fyrir afhendingarskilmála.

1. Setja upp Intrastat-kóða fyrir afhendingarskilmálana.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Afhendingarskilmálar**.
    2. Í hnitanetinu skal velja **CIF**.
    3. Í flýtiflipann **Almennt**, í reitinn **Intrastat-kóði**, skal færa inn **CIF**.

2. Veljið sjálfgefna afhendingarskilmála fyrir viðskiptavin.

    1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
    2. Í hnitanetinu skal velja **DE-016**.
    3. Á flýtiflipanum **Reikningur og afhending**, í reitnum **Afhendingarskilmálar**, skal velja **CIF**.

3. Veljið sjálfgefna afhendingarskilmála fyrir lánardrottinn.

    1. Farið í **Viðskiptaskuldir**  >  **Lánardrottnar**  >  **Allir lánardrottnar**.
    2. Í hnitanetinu skal velja **DE-001**.
    3. Á flýtiflipanum **Reikningur og afhending**, í reitnum **Afhendingarskilmálar**, skal velja **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Staðfestið skattundanþágunúmerskóða ESB-viðskiptavinar

1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
2. Í hnitanetinu skal velja **DE-016**.
3. Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Söluskattur**, skal staðfesta að reiturinn **Skattundanþágunúmer** sé stilltur á **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Stofna sölupöntun með viðskiptavin innan ESB

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-016**.
4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
5. Í reitnum **Vöruhús** skal velja **11**.
6. Í flipanum **Aðsetur** skal staðfesta að reiturinn **Aðsetur** sé stilltur á **Teichgasse 12, Kiel, 24103, DEU** því að viðskiptavinurinn er frá Þýskalandi.
7. Veldu **Í lagi**.
8. Í flipanum **Haus**, í flýtiflipanum **Afhending**, skal staðfesta að reiturinn **Afhendingarskilmálar** sé stilltur á **CIF** og reiturinn **Afhendingarmáti** sé stilltur á **10**.
9. Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **8**.
10. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, skal staðfesta að reiturinn **Færslukóði** sé stilltur á **11**, reiturinn **Vara** sé stilltur á **100 200 30** og reiturinn **Upprunaland/-svæði** sé stilltur á **POL**.
11. Í aðgerðarúðunni skal velja **Vista**.
12. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
13. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
14. Í flýtiflipanum **Uppsetning**, í reitnum **Söludagsetning** skal velja **18.10.2021**.
15. Veldu svo **Í lagi** til að bóka reikninginn.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna

1. Farðu í **Skattur** > **Skattskýrslur** > **Erlend viðskipti** > **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
4. Velja **Síu**.
5. Í svarglugganum **Intrastat-sía**, í flipanum **Svið**, skal velja fyrstu línuna og ganga úr skugga um reiturinn **Reitur** er stilltur á **Dagsetning**.
6. Í reitnum **Skilyrði** skal velja daginn í dag.
7. Veldu **Í lagi** til að loka svarglugganum **Intrastat-sía**.
8. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Línan táknar sölupöntunina sem þú stofnaðir fyrr.

    ![Lína sem táknar sölupöntunina á Intrastat-síðunni](media/intrastat_pl_1.png)

9. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um sölupöntun á almenna flipa Intrastat-síðunnar](media/intrastat_pl_2.png)

10. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
11. Í svarglugganum **Intrastat-skýrsla**, á flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, í reitnum **Frá dagsetningu**, skal velja fyrsta dag yfirstandandi mánaðar.
12. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
13. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
14. Í reitnum **Stefna** skal velja **Sendingar**.
15. Í hlutanum **Vörpun skráarsniðs** skal staðfesta að reiturinn **Gerð skýrslu** sé stilltur á **Skýrsla**.
16. Í reitnum **Borg skjalastofnunar** skal færa inn í **Kraká**.
17. Veldu **19.10.2021** (19. október 2021) í reitnum **Dagsetning skjalastofnunar**.
18. Fært er inn **11** í reitinn **Númer fylgiskjals**.
19. Í reitinn **Fylgiskjalsútgáfa** skala færa inn **22**.
20. Veldu **Í lagi** og farðu yfir skýrsluna á XML-sniði sem er búið til. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Nafn svæðis</strong></p>
    </td>
    <td>
    <p><strong>Lýsing svæðis</strong></p>
    </td>
    <td>
    <p><strong>Virði</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Upplýsingar um skjalið</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Dagsetningu stofnunar skjalsins.</p>
    </td>
    <td>
    <p>19-10-2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Borgin þar sem skjalið var stofnað.</p>
    </td>
    <td>
    <p>Kraká</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Heildarfjöldi vara.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilega heildargildið.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Heildarvirði reikningsins.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Einingakóðinn.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Gerð skýrslu.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Útgáfa skjalsins.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Númer</p>
    </td>
    <td>
    <p>Skjalanúmerið.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Viðmiðunarmánuðurinn.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Viðmiðunarárið.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Gerð</p>
    </td>
    <td width="330">
    <p>Stefna skýrslunnar</p>
    </td>
    <td>
    <p>M</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Kenni skýrslu.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Upplýsingar um fyrirtækið</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Borgin þar sem fyrirtækið er staðsett.</p>
    </td>
    <td>
    <p>Varsjá</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Svæðiskóði fyrirtækisins.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>NIP-kóði fyrirtækisins.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Póstnúmer fyrirtækisins.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Gatan sem fyrirtækið er staðsett við.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Heiti fyrirtækisins.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Upplýsingar um vöruna</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilega gildið.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Reikningsvirðið.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettómassi.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>VSK-númer viðskiptavinar.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Vörukóðinn.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Færslukóðinn.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Afhendingarskilmálarnir.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Kóði lands eða -svæðis sendingar/móttöku.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Lýsing á hrávörunum.</p>
    </td>
    <td>
    <p>Vélbúnaður</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Vörunúmerið.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Tengslaupplýsingar</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tölvupóstur</p>
    </td>
    <td>
    <p>Netfang sendanda.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Faxnúmer sendandans.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Sími</p>
    </td>
    <td>
    <p>Símanúmer sendandans.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Heiti sendandans.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastatskýrsla á sendingum](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Viðskiptaskuldir** > **Innkaupapantanir** > **Allar innkaupapantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna innkaupapöntun**, í reitnum **Lánardrottnalykill**, skal velja **DE-001**.
4. Í reitnum **Svæði** skal velja **1**.
5. Í reitnum **Vöruhús** skal velja **11**.
6. Veldu **Í lagi**.
7. Í flipanum **Haus**, í flýtiflipanum **Afhending**, skal staðfesta að reiturinn **Afhendingarmáti** sé stilltur á **10** og reiturinn **Afhendingarskilmálar** sé stilltur á **CIF**.
8. Í flýtiflipanum **Línur**, í flýtiflipanum **Innkaupapöntunarlínur**, í reitnum **Vörunúmer**, skal velja **D0003**. Því næst, í reitinn **Magn**, skal færa inn **6**.
9. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Erlend viðskipti**, skal staðfesta að reiturinn **Færslukóði** sé stilltur á **11**, reiturinn **Flutningur** sé stilltur á **3**, reiturinn **Vara** sé stilltur á **100 200 30** og reiturinn **Upprunaland/-svæði** sé stilltur á **DEU**.
10. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerðir**, skal velja **Staðfesta**.
11. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
12. Á aðgerðarúðunni skal velja **Sjálfgefið frá** og svo í reitnum **Sjálfgefið magn fyrir línur** skal velja **Pantað magn**. Veljið síðan **Í lagi**.
13. Í flýtiflipanum **Reikningshaus lánardrottins**, í hlutann **Auðkenning reiknings**, í reitinn **Númer**, skal færa inn **00010**.
14. Í hlutanum **Reikningsdagsetningar**, í reitnum **Reikningsdagsetning**, skal velja núverandi dagsetningu. Þessi dagsetning verður notuð fyrir Intrastat-flutning.
15. Í reitnum **Móttökudagsetning skjals** skal velja **18.10.2021** (18. október 2021).
16. Á aðgerðasvæðinu skal velja **Bóka** til að bóka reikninginn.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Búa til Intrastat-skattskýrslu fyrir komur

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur lánardrottins** á **Já**.
4. Veldu **Í lagi** til að flytja færslurnar og síðan skoða Intrastat-bókina.

    ![Lína sem táknar innkaupapöntunina á Intrastat-síðunni](media/intrastat_pl_4.png)

5. Farðu yfir upplýsingarnar á flipanum **Almennt** fyrir innkaupapöntunina.

    ![Upplýsingar um innkaupapöntun á almenna flipa Intrastat-síðunnar](media/intrastat_pl_5.png)

6. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
7. Í svarglugganum **Intrastat-skýrsla**, á flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, í reitnum **Frá dagsetningu**, skal velja fyrsta dag yfirstandandi mánaðar.
8. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
9. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
10. Í reitnum **Stefna** skal velja **Komur**.
11. Í hlutanum **Vörpun skráarsniðs** skal staðfesta að reiturinn **Gerð skýrslu** sé stilltur á **Skýrsla**.
12. Í reitnum **Borg skjalastofnunar** skal færa inn í **Kraká**.
13. Veldu **19.10.2021** (19. október 2021) í reitnum **Dagsetning skjalastofnunar**.
14. Fært er inn **11** í reitinn **Númer fylgiskjals**.
15. Í reitinn **Fylgiskjalsútgáfa** skala færa inn **22**.
16. Veldu **Í lagi** og farðu yfir skýrsluna á XML-sniði sem er búið til. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Nafn svæðis</strong></p>
    </td>
    <td>
    <p><strong>Lýsing svæðis</strong></p>
    </td>
    <td>
    <p><strong>Virði</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Upplýsingar um skjalið</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Dagsetningu stofnunar skjalsins.</p>
    </td>
    <td>
    <p>19-10-2021</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Borgin þar sem skjalið var stofnað.</p>
    </td>
    <td>
    <p>Kraká</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Heildarfjöldi vara.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilega heildargildið.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Heildarvirði reikningsins.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Einingakóðinn.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Gerð skýrslu.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Útgáfa skjalsins.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Númer</p>
    </td>
    <td>
    <p>Skjalanúmerið.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Viðmiðunarmánuðurinn.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Viðmiðunarárið.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Gerð</p>
    </td>
    <td width="332">
    <p>Stefna skýrslunnar</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Kenni skýrslu.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Upplýsingar um fyrirtækið</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Borgin þar sem fyrirtækið er staðsett.</p>
    </td>
    <td>
    <p>Varsjá</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Svæðiskóði fyrirtækisins.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>NIP-kóði fyrirtækisins.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Póstnúmer fyrirtækisins.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Gatan sem fyrirtækið er staðsett við.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Heiti fyrirtækisins.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Upplýsingar um vöruna</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilega gildið.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Reikningsvirðið.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Nettómassi.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Kóði upprunalands eða -svæðis afurðarinnar.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Flutningsmátakóðinn.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Vörukóðinn.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Færslukóðinn.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Afhendingarskilmálarnir.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Kóði lands eða -svæðis sendingar/móttöku.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Lýsing á hrávörunum.</p>
    </td>
    <td>
    <p>Vélbúnaður</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Vörunúmerið.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Tengslaupplýsingar</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tölvupóstur</p>
    </td>
    <td>
    <p>Netfang sendanda.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Faxnúmer sendandans.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Sími</p>
    </td>
    <td>
    <p>Símanúmer sendandans.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Heiti sendandans.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastat-skýrsla á aðsent](media/intrastat_pl_6.png)
