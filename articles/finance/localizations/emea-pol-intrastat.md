---
title: Pólskt Intrastat
description: Þetta efni inniheldur upplýsingar um Intrastat skýrslur í Póllandi.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: fbacc204208e536291035c6f9bb2ef4fa4038f58
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566092"
---
# <a name="polish-intrastat"></a>Pólskt Intrastat

[!include[banner](../includes/banner.md)]

Síðan **Intrastat** er notuð til að útbúa og tilkynna upplýsingar um viðskipti innan landa Evrópusambandsins. Pólska Intrastat yfirlýsingin inniheldur upplýsingar um vöruviðskipti til skýrslugerðar.

Eftirfarandi reitir eru með í pólsku Intrastat yfirlýsingunni. Allir reitirnir eru innifaldir við komur og sendingar nema kl **RodzajTransportu** (flutningsmátinn) og **KrajPochodzenia** (upprunalandið eða -svæðið) sem eru ekki innifalin í sendingum, og **IdKontrahenta** (erlent virðisaukaskattsnúmer viðskiptavinarins) sem er ekki innifalið við komu.

| Heiti svæðis | Lýsing |
|-------------------------|-------------------------|
| Deklaracja Data | Dagsetningin þegar skjalið er búið til. |
| Miesiac | Viðmiðunarmánuður yfirlýsingarinnar. |
| Rok | Viðmiðunarár yfirlýsingarinnar. |
| Númer | Framtalsnúmerið á viðmiðunartímabilinu. |
| Wersja | Útgáfunúmer yfirlýsingarinnar. |
| NrWlasny | Auðkenni yfirlýsingarinnar. Gildið er sjálfkrafa myndað. |
| Týp | Skýrslustefnan.</br><li>Fyrir komu er „P“ prentað.</li><li>Fyrir sendingar er „W“ prentað.</li> |
| Rodzaj | Tegund yfirlýsingarinnar. Gildið gefur til kynna hvort skýrslan er upprunalega yfirlýsingin eða leiðréttingaryfirlýsing. |
| UC | Einingakóði sem Intrastat yfirlýsingin er stíluð á. Gildið er tilgreint í **Skattfrjálst númer** sviði í **Söluskattur** kafla um **Umboðsmaður** flipi á **Staðlar utanríkisviðskipta** síðu. |
| Nazwa | Nafn félagsins. |
| Miejscowosc, UlicaNumer, KodPocztowy | Fullt heimilisfang lögaðilans. |
| Nip | Pólska skattaauðkennisnúmerið (virðisaukaskattsnúmer [VSK]). |
| Regon | Pólska tölfræðilega auðkennisnúmerið (fyrirtækjanúmer). |
| LacznaWartoscFaktur | Summa reikningsgilda. |
| LacznaWartoscStatystyczna | Summa tölfræðilegra gilda. |
| LacznaLiczbaPozycji | Heildarfjöldi vöruliða. |
| PozId | Samfellt númer tiltekins vöruhluts. |
| UmsögnTowaru | Vöruheiti vörunnar. |
| KrajPochodzeniaWysylki | Alþjóðlega staðlastofnunin (ISO) kóða fyrir land eða svæði mótaðilans. |
| WarunkiDostawy | Intrastat kóðann fyrir afhendingarskilmálana. |
| RodzajTransakcji | Kóðinn sem gefur til kynna eðli viðskiptanna. Pólsk fyrirtæki nota tveggja stafa viðskiptakóða. |
| KodTowarowy | Átta stafa vörukóði samkvæmt sameinuðu flokkunarkerfi. |
| RodzajTransportu | Intrastat kóðann fyrir flutningsmátann. |
| KrajPochodzenia | ISO kóða fyrir landið eða svæðið þar sem vörurnar voru framleiddar eða framleiddar. |
| MasaNetto | Nettómassi í heilum kílóum. |
| IloscUzupelniajacaJm | Magnið í viðbótarmælieiningunni, í heilum tölum. |
| WartoscFaktury | Reikningsvirði allra viðskipta sem falla undir einn lið. |
| WartoscStatystyczna | Tölfræðilegt gildi. |
| Notkun: NazwiskoImie, Sími, Faks, Netfang | Fornafn og eftirnafn, símanúmer, faxnúmer og netfang þess sem leggur fram yfirlýsinguna. |
| IdKontrahenta | Erlend virðisaukaskattsnúmer viðskiptavinar í ESB-ríki. |


## <a name="set-up-intrastat"></a>Setja upp Intrastat

Flyttu inn nýjustu útgáfuna af eftirfarandi rafrænum skýrslugerðum (ER) úr alþjóðlegu geymslunni:

   - Intrastat-líkan
   - Intrastat-skýrsla
   - Intrastat (PL)

Frekari upplýsingar er að finna í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Settu upp VSK-auðkenni og fyrirtækisnúmer fyrir fyrirtækið þitt

### <a name="create-registration-types-for-company-codes"></a>Búðu til skráningargerðir fyrir fyrirtækjakóða

Þú verður að búa til tvær skráningargerðir fyrir fyrirtækjakóða: eina fyrir VSK ID (NIP code) og eina fyrir fyrirtækisnúmerið (Regon code).

1. Fara til **Stjórn stofnunarinnar** > **Heimilisfangabók** > **Skráningargerðir** > **Skráningargerðir**.
2. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til skráningartegund fyrir virðisaukaskattsnúmerið.
3. Í **Sláðu inn upplýsingar um skráningartegund** valmynd, í **Nafn** reit, sláðu inn nafn fyrir nýju skráningargerðina. Til dæmis, slá inn **NIP**.
4. Í reitnum **Land/svæði** skal velja **POL**.
5. Velja **Stofna**.
6. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til skráningartegund fyrir fyrirtækisnúmerið.
7. Í **Sláðu inn upplýsingar um skráningartegund** valmynd, í **Nafn** reit, sláðu inn nafn fyrir nýju skráningargerðina. Til dæmis, slá inn **Regon**.
8. Í reitnum **Land/svæði** skal velja **POL**.
9. Velja **Stofna**.

### <a name="match-the-registration-types-with-registration-categories"></a>Passaðu skráningartegundirnar við skráningarflokka

1. Fara til **Stjórn stofnunarinnar** > **Heimilisfangabók** > **Skráningargerðir** > **Skráningarflokkar**.
2. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til tengil á milli hverrar skráningartegundar sem þú bjóst til og skráningarflokks.

    - Fyrir skráningartegund fyrir VSK ID (NIP-númer), veldu **VSK auðkenni** skráningarflokk.
    - Fyrir skráningargerð fyrir fyrirtækisnúmerið (Regon kóða), veldu **Enterprise ID (COID)** skráningarflokk.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Settu upp VSK-auðkenni og fyrirtækisnúmer fyrir fyrirtækið þitt

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu fyrirtæki þitt í ristinni.
3. Á aðgerðarrúðunni velurðu **Skráningarauðkenni**.
4. Á **Skráningarauðkenni** Flýtiflipi, veldu **Bæta við**.
5. Í **Skráningartegund** reit, veldu eina af skráningartegundunum sem þú bjóst til áður.
6. Sláðu inn virðisaukaskattsnúmer fyrirtækis þíns (NIP kóða) eða fyrirtækisnúmer (Regon kóða), allt eftir skráningargerðinni sem þú valdir í fyrra skrefi.
7. Endurtaktu skref 4 til 6 fyrir hina skráningargerðina sem þú bjóst til áðan.

## <a name="set-up-a-company-address"></a>Settu upp heimilisfang fyrirtækis

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Veldu fyrirtæki þitt í ristinni.
3. Á **Heimilisföng** flipa, veldu **Breyta**.
4. Í **Breyta heimilisfangi** valmynd, í **Póstnúmer** reit skaltu velja póstnúmer fyrirtækis þíns.
5. Í **Götu** reit, sláðu inn heimilisfangið þitt.
6. Í **Borg** reit, veldu borgina þína.

## <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Fara til **Skattur** > **Uppsetning** > **Staðlar utanríkisviðskipta**.
2. Á **Intrastat** flipa, á **Rafræn skýrslugerð** flýtiflipann, í **Kortlagning skráarsniðs** reit, veldu **Intrastat (PL)**.
3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
4. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.
5. Í reitnum **Færslukóði** skal velja færslukóðann fyrir flutning á eignum. Þú notar þennan kóða fyrir færslur sem búa til raunverulegar eða áætlaðar færslur á eignum gegn greiðslu (fjárhagslegri eða annars konar greiðslu). Þú getur líka notað það til leiðréttinga. Fyrirtæki í Póllandi nota tveggja stafa viðskiptakóða.
6. Í reitnum **Kreditnóta** skal velja færslukóðann fyrir vöruskil.
7. Í flipanum **Eiginleikar lands/svæðis**, í reitnum **Land/svæði**, skal gefa upp öll lönd eða svæði sem fyrirtækið þitt á í viðskiptum við. Veldu fyrir hvert land sem er hluti af ESB **ESB** í **Tegund lands/svæðis** reitinn, þannig að landið birtist á Intrastat skýrslunni þinni. Fyrir Pólland, veldu **Innlent** í **Tegund lands/svæðis** sviði.
8. Á **Umboðsmaður** flipa, á **Umboðsmaður** flýtiflipann, í **Söluskattur** kafla, í **Skattfrjálst númer** reit, slá inn **420000** til að tilgreina einingakóðann sem Intrastat yfirlýsingin er stíluð á.
9. Á **Hafðu samband** flipa, sláðu inn nafn, símanúmer, faxnúmer og netfang þess sem er að leggja fram yfirlýsinguna.
10. Á **Númeraraðir** flipa, í **Númeraraðarkóði** sviði fyrir **XML skráarnúmer** tilvísun, tilgreinið ósamfellda talnaröð sem hefur að hámarki níu stafi. Þessi reitur er notaður til að búa til sjálfkrafa gildi fyrir **Auðkenni yfirlýsingar** reitinn á Intrastat skýrslunni.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Settu upp vörufæribreytur fyrir Intrastat yfirlýsinguna

1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
2. Í hnitanetinu skal velja afurð.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja vörukóðann. Nafn vörunnar verður prentað í **Lýsing á vörum** reitinn á Intrastat skýrslunni.
4. Í **Uppruni** kafla, í **Land/svæði** reit, veldu land eða upprunasvæði vörunnar.
5. Í flýtiflipanum **Stjórna birgðum**, í reitnum **Nettóþyngd**, skal færa inn þyngd afurðar í kílógrömmum.

## <a name="set-up-compression-of-intrastat"></a>Uppsetning Intrastat-þjöppunar

-   Farðu í **Skattur**  >  **Uppsetning**  >  **Erlend viðskipti**  >  **Intrastat-þjöppun** og veldu reitina sem á að bera saman þegar Intrastat-upplýsingar eru teknar saman. Fyrir pólska Intrastat skaltu velja eftirfarandi reiti:

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

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Settu upp flutningsaðferð og afhendingarskilmála

1.  Settu upp flutningskóða.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Flutningsmáti**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í **Flutningur** reit, sláðu inn einstakan kóða. Pólsk fyrirtæki nota eins tölustafa flutningskóða.

2.  Settu upp afhendingarmáta Intrastat kóða.

    1. Fara til **Innkaup og innkaup** > **Uppsetning** > **Dreifing** > **Skilmálar afhendingar**.
    2. Veldu sett af afhendingarskilmálum í hnitanetinu.
    3. Á **Almennt** flýtiflipann, í **Intrastat kóða** reit, sláðu inn einstaka kóðann.

## <a name="intrastat-transfer"></a>Intrastat-flutningur

Á síðunni **Intrastat** á aðgerðasvæðinu er hægt að velja **Flutningur** til að flytja sjálfkrafa upplýsingarnar um viðskipti innan samfélags úr sölupöntunum, textum með frjálsum texta, innkaupapöntunum, lánardrottnareikningum, innhreyfingarskjölum afurða lánardrottins, verkreikningum og flutningspöntunum. Aðeins skjöl sem hafa ESB-land sem viðtökuland eða -svæði eða sending verða flutt.

Þú getur líka fært inn færslur handvirkt með því að velja **Nýtt** á aðgerðasvæðinu.

### <a name="generate-an-intrastat-report"></a>Mynda Intrastat-skýrslu

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Úttak** &gt; **Skýrsla**.
3. Í svarglugganum **Intrastat skýrsla** skal stilla eftirfarandi reiti.

    | Svæði | Lýsing |
    |-------------------------|-------------------------|
    | Frá dagsetning | Veldu upphafsdagsetningu fyrir skýrsluna. |
    | Mynda skrá | Stilltu þennan valkost á **Já** til að búa til .xml skrá fyrir Intrastat skýrsluna þína. |
    | Skráarheiti | Sláðu inn nafn .xml skráarinnar. |
    | Búa til skýrslu | Stilltu þennan valkost á **Já** til að búa til .xlsx-skrá fyrir Intrastat-skýrsluna. |
    | Heiti skýrsluskráar | Færðu inn heiti .xlsx-skráar. |
    | Stefna | Veldu **Komur** til að fá skýrslu um komur innan samfélags.</br>Veldu **Sendingar** til að fá skýrslu um sendingar innan samfélags. |
    | Auðkenni yfirlýsingar | Auðkenni skjalsins er sjálfkrafa búið til og hægt að uppfæra það. |
    | Gerð skýrslu | Veldu **Yfirlýsing** fyrir upprunalega yfirlýsingu.</br>Veldu **Leiðrétting framtals – skipti** vegna leiðréttingaryfirlýsingar sem ætlað er að koma að fullu í stað fyrirliggjandi, áður framlagðrar frum- eða leiðréttingaryfirlýsingar. |
    | Borg skjalagerðar | Sláðu inn gildið sem ætti að prenta í **Miejscowosc** reitinn í Intrastat yfirlýsingunni. |
    | Dagsetning skjalagerðar | Sláðu inn gildið sem ætti að prenta í **Deklaracja Data** reitinn í Intrastat yfirlýsingunni. |
    | Númer skjals | Sláðu inn gildið sem ætti að prenta í **Númer** reitinn í Intrastat yfirlýsingunni. |
    | Útgáfa skjals | Sláðu inn gildið sem ætti að prenta í **Wersja** reitinn í Intrastat yfirlýsingunni. |

4. Veldu **Í lagi** og farðu yfir myndaða skýrslu.

## <a name="example"></a>Dæmi

Þetta dæmi sýnir hvernig á að bóka komur og sendingar fyrir Intrastat með því að nota **DEMF** lögaðili.

### <a name="preliminary-setup"></a>Bráðabirgða uppsetning

Flyttu inn nýjustu útgáfu af eftirfarandi skilgreiningum rafrænnar skýrslugerðar:

   - Intrastat-líkan
   - Intrastat-skýrsla
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Settu upp heimilisfang fyrirtækis

1. Farðu í **Fyrirtækisstjórnun** > **Altæk aðsetursbók** > **Aðsetur** > **Uppsetning aðseturs**.
2. Á **Borg** flipa, veldu **Nýtt**.
3. Í reitnum **Land/svæði** skal velja **POL**.
4. Í **Borg** reit, slá inn **Varsjá**.
5. Á **Póstnúmer** flipa, veldu **Nýtt**.
6. Í reitnum **Land/svæði** skal velja **POL**.
7. Í **Borg** reit, veldu **Varsjá**.
8. Í **Póstnúmer** reit, slá inn **00-844**.
9. Farðu í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar** og veldu lögaðilann **DEMF**.
10. Í flýtiflipanum **Aðsetur** skal velja **Breyta**.
11. Í reitnum **Land/svæði** skal velja **POL**.
12. Í **Póstnúmer** reit, veldu **31-111**.
13. Í **Götu** reit, slá inn **Statystyczna 22/1**.
14. Í **Borg** reit, veldu **Varsjá**.
15. Veldu **Í lagi**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Settu upp VSK-auðkenni og fyrirtækjanúmerakóða fyrir fyrirtækið þitt

### <a name="create-registration-types-for-company-codes"></a>Búðu til skráningargerðir fyrir fyrirtækjakóða

1. Fara til **Stjórn stofnunarinnar** > **Heimilisfangabók** > **Skráningargerðir** > **Skráningargerðir**.
2. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til skráningartegund fyrir VSK ID (NIP code).
3. Í **Sláðu inn upplýsingar um skráningartegund** valmynd, í **Nafn** reit, slá inn **NIP**.
4. Í reitnum **Land/svæði** skal velja **POL**.
5. Velja **Stofna**.
6. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til skráningartegund fyrir fyrirtækisnúmerið (Regon kóða).
7. Í **Sláðu inn upplýsingar um skráningartegund** valmynd, í **Nafn** reit, slá inn **Regon**.
8. Í reitnum **Land/svæði** skal velja **POL**.
9. Velja **Stofna**.

### <a name="match-the-registration-types-with-registration-categories"></a>Passaðu skráningartegundirnar við skráningarflokka

1. Fara til **Stjórn stofnunarinnar** > **Heimilisfangabók** > **Skráningargerðir** > **Skráningarflokkar**.
2. Á aðgerðarrúðunni velurðu **Nýtt** til að búa til tengil á milli hverrar skráningartegundar sem þú bjóst til og skráningarflokks.

    - Fyrir **NIP** skráningartegund, veldu **VSK auðkenni** skráningarflokk.
    - Fyrir **Regon** skráningartegund, veldu **Enterprise ID (COID)** skráningarflokk.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Settu upp VSK-auðkenni og fyrirtækisnúmer fyrir fyrirtækið þitt

1. Fara í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**.
2. Í hnitanetinu skal velja **DEMF**.
3. Á aðgerðarrúðunni velurðu **Skráningarauðkenni**.
4. Á **Skráningarauðkenni** Flýtiflipi, veldu **Bæta við**.
5. Í **Skráningartegund** reit, veldu **NIP**.
6. Í **Skráningarnúmer** reit, slá inn **1234567890**.
7. Veljið **Bæta við**.
8. Í **Skráningartegund** reit, veldu **Regon**.
9. Í **Skráningarnúmer** reit, slá inn **12345678901234**.

### <a name="set-up-a-number-sequence-code"></a>Settu upp númerarunarkóða

1. Farðu í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðir**.
2. Á aðgerðarrúðunni, á **Númeraröð** flipa, í **Nýtt** hópur, veldu **Númeraröð**.
3. Á **Auðkenning** flýtiflipann, í **Númeraraðarkóði** reit, slá inn **XML\_ skrá**.
4. Á **Umfangsbreytur** flýtiflipann, í **Umfang** reit, veldu **Fyrirtæki**.
5. Í **Fyrirtæki** reit, veldu **DEMF**.
6. Á **Hluti** flýtiflipann, í **Lengd** sviði fyrir **Alfatölulegt** hluti, slá inn **4**.
7. Á **Almennt** flýtiflipann, í **Uppsetning** kafla, stilltu **Stöðugt** valmöguleika til **Nei**.
8. Í **Númeraúthlutun** kafla, í **Stærsta** reit, slá inn **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Setja upp færibreytur erlendra viðskipta

1. Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta**.
2. Í flýtiflipanum **Intrastat** á **Almennt** flipanum í **Færslukóði** reitknum velurðu **11**.
3. Á **Rafræn skýrslugerð** flýtiflipann, í **Kortlagning skráarsniðs** reit, veldu **Intrastat (PL)**.
4. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
5. Á **Stigveldi vörukóða** Flýtiflipi, staðfestu að **Stigveldi flokka** reiturinn er stilltur á **Intrastat**.
6. Í flipanum **Eiginleikar lands/svæðis** skal velja **Nýtt**.
7. Í reitnum **Land/svæði viðskiptafélaga** skal velja **POL**. Þá, í **Tegund lands/svæðis** reit, veldu **Innlent**.
8. Í reitnum **Land/svæði viðskiptafélaga** skal velja **DEU**. Þá, í **Tegund lands/svæðis** reit, veldu **ESB**.
9. Á **Umboðsmaður** flipa, á **Umboðsmaður** flýtiflipann, í **Söluskattur** kafla, í **Skattfrjálst númer** reit, slá inn **420000**.
10. Á **Hafðu samband** flipa, í **Nafn** reit, slá inn **Manish Chopra**.
11. Í **Sími** reit, slá inn **425-555-5068**.
12. Í **Faxnúmer** reit, slá inn **425-555-5049**.
13. Í **Tölvupóstur** reit, slá inn **manishc@contoso.com**.
14. Á **Númeraraðir** flipa, í **Númeraraðarkóði** sviði fyrir **XML skráarnúmer** tilvísun, veldu **XML\_ skrá**.

### <a name="set-up-product-information"></a>Setja upp afurðarupplýsingar

1. Fara til **Vöruupplýsingastjórnun** > **Vörur** > **Gefin út** **vörur**.
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

### <a name="set-up-a-transport-method"></a>Settu upp flutningsaðferð

1. Búðu til flutningsaðferð.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Flutningsmáti**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í **Flutningur** reit, slá inn **3**.
    4. Í **Lýsing** reit, slá inn **Vegaflutningar**.

2. Úthlutaðu nýja flutningsmáta til afhendingarmáta. Þannig setur þú upp sjálfgefin gildi sem eru notuð fyrir flutningsaðferðina þegar samsvarandi afhendingarmáti er valinn.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Flutningsmátar**.
    2. Í hnitanetinu skal velja **10**.
    3. Í flýtiflipanum **Erlend viðskipti**, í reitnum **Flutningur**, skal velja **3**.

3. Veldu sjálfgefna afhendingarmáta fyrir viðskiptavin.

    1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
    2. Veldu í ristinni **DE-016**.
    3. Á **Reikningur og afhending** flýtiflipann, í **Afhendingarmáti** reit, veldu **10**.

4. Veldu sjálfgefna afhendingarmáta fyrir lánardrottin.

    1. Fara til **Viðskiptaskuldir** > **Söluaðilar** > **Allir söluaðilar**.
    2. Veldu í ristinni **DE-001**.
    3. Á **Reikningur og afhending** flýtiflipann, í **Afhendingarmáti** reit, veldu **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Settu upp kóða fyrir afhendingarskilmála

1. Settu upp Intrastat kóða fyrir afhendingarskilmála.

    1. Fara til **Innkaup og innkaup** > **Uppsetning** > **Dreifing** > **Skilmálar afhendingar**.
    2. Í hnitanetinu skal velja **CIF**.
    3. Á **Almennt** flýtiflipann, í **Intrastat kóða** reit, slá inn **CIF**.

2. Veldu sjálfgefna afhendingarskilmála fyrir viðskiptavin.

    1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
    2. Veldu í ristinni **DE-016**.
    3. Á **Reikningur og afhending** flýtiflipann, í **Afhendingarskilmálar** reit, veldu **CIF**.

3. Veldu sjálfgefna afhendingarskilmála fyrir lánardrottinn.

    1. Fara til **Viðskiptaskuldir** > **Söluaðilar** > **Allir söluaðilar**.
    2. Veldu í ristinni **DE-001**.
    3. Á **Reikningur og afhending** flýtiflipann, í **Afhendingarskilmálar** reit, veldu **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Staðfestu skattfrjálsan númerakóða ESB viðskiptavinar

1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
2. Veldu í ristinni **DE-016**.
3. Á **Reikningur og afhending** flýtiflipann, í **Söluskattur** kafla, staðfestu að **Skattfrjálst númer** reiturinn er stilltur á **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Stofna sölupöntun með viðskiptavin innan ESB

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í flýtiflipanum **Viðskiptavinur**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavinalykill**, skal velja **DE-016**.
4. Í flýtiflipanum **Almennt**, í hlutanum **Geymsluvíddir**, í reitnum **Svæði**, skal velja **1**.
5. Í reitnum **Vöruhús** skal velja **11**.
6. Á **Heimilisfang** flipa, staðfestu að **Heimilisfang** reiturinn er stilltur á **Teichgasse 12, Kiel, 24103, DEU**, vegna þess að viðskiptavinurinn er frá Þýskalandi.
7. Veldu **Í lagi**.
8. Á **Fyrirsögn** flipa, á **Afhending** flýtiflipann, staðfestu að **Afhendingarskilmálar** reiturinn er stilltur á **CIF**, og **Afhendingarmáti** reiturinn er stilltur á **10**.
9. Í flýtiflipanum **Línur**, í flýtiflipanum **Sölupöntun línur**, í reitnum **Vörunúmer**, skal velja **D0001**. Því næst, í reitinn **Magn**, skal færa inn **8**.
10. Á **Upplýsingar um línu** flýtiflipann, á **Utanríkisviðskipti** flipa, staðfestu að **Færslukóði** reiturinn er stilltur á **11**, hinn **Vöruvara** reiturinn er stilltur á **100 200 30**, og **Upprunaland/upprunaland** reiturinn er stilltur á **POL**.
11. Í aðgerðarúðunni skal velja **Vista**.
12. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
13. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
14. Á **Uppsetning** flýtiflipann, í **Söludagur** reit, veldu **18.10.2021** (18. október 2021).
15. Veldu svo **Í lagi** til að bóka reikninginn.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Færðu færsluna í Intrastatbókina og farðu yfir niðurstöðuna

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
4. Velja **Síu**.
5. Í **Intrastat sía** valmynd, á **Svið** flipann, veldu fyrstu línuna og staðfestu að **Field** reiturinn er stilltur á **Dagsetning**.
6. Í reitnum **Skilyrði** skal velja daginn í dag.
7. Veldu **Í lagi** til að loka svarglugganum **Intrastat-sía**.
8. Veldu **Í lagi** til að loka svarglugganum **Intrastat (flutningur)** og farðu yfir niðurstöðuna. Línan táknar sölupöntunina sem þú stofnaðir fyrr.

    ![Lína sem táknar sölupöntunina á Intrastat-síðunni](media/intrastat_pl_1.png)

9. Veldu færslulínuna og veldu síðan flipann **Almennt** til að skoða frekari upplýsingar.

    ![Upplýsingar um sölupöntun á almenna flipa Intrastat-síðunnar](media/intrastat_pl_2.png)

10. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
11. Í **Intrastat skýrsla** valmynd, á **Færibreytur** flýtiflipann, í **Dagsetning** kafla, í **Frá dags** reit, veldu fyrsta dag núverandi mánaðar.
12. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
13. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
14. Í reitnum **Stefna** skal velja **Sendingar**.
15. Í **Kortlagning skráarsniðs** kafla, staðfestu að **Tegund yfirlýsingar** reiturinn er stilltur á **Yfirlýsing**.
16. Í **Borg skjalagerðar** reit, slá inn **Kraká**.
17. Í **Dagsetning skjalagerðar** reit, veldu **19.10.2021** (19. október 2021).
18. Í **Skjal nr** reit, slá inn **11**.
19. Í **Skjalaútgáfa** reit, slá inn **22**.
20. Veldu **Allt í lagi**, og skoðaðu skýrsluna á XML-sniði sem er búið til. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

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
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Borgin þar sem skjalið var búið til.</p>
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
    <p>Heildarfjöldi hluta.</p>
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
    <p>Heildartölfræðileg gildi.</p>
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
    <p>Heildarvirði reiknings.</p>
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
    <p>Einingakóði.</p>
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
    <p>Tegund yfirlýsingarinnar.</p>
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
    <p>Skjalútgáfan.</p>
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
    <p>Skjalnúmerið.</p>
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
    <p>Týp</p>
    </td>
    <td width="330">
    <p>Skýrslustefnan.</p>
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
    <p>Auðkenni yfirlýsingarinnar.</p>
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
    <p>Regon kóða fyrirtækisins.</p>
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
    <p>NIP kóða fyrirtækisins.</p>
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
    <p>Póstnúmer félagsins.</p>
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
    <p>Gatan þar sem fyrirtækið er staðsett.</p>
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
    <p>Nafn félagsins.</p>
    </td>
    <td>
    <p>Contoso skemmtunarkerfi Þýskalandi</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Upplýsingar um hið góða</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilegt gildi.</p>
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
    <p>Reikningsverðmæti.</p>
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
    <p>Vörunúmerið.</p>
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
    <p>Viðskiptakóði.</p>
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
    <p>Afhendingarskilmálar.</p>
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
    <p>Kóðinn fyrir landið eða svæði sendingar/áfangastaðarins.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UmsögnTowaru</p>
    </td>
    <td>
    <p>Lýsing á vörunum.</p>
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
    <p>Faxnúmer sendanda.</p>
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
    <p>Símanúmer innsendanda.</p>
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
    <p>Nafn innsendanda.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastat skýrsla um sendingar](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Viðskiptaskuldir** > **Innkaupapantanir** > **Allar innkaupapantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna innkaupapöntun**, í reitnum **Lánardrottnalykill**, skal velja **DE-001**.
4. Í **Síða** reit velja **1**.
5. Í **Vöruhús** reit velja **11**.
6. Veldu **Í lagi**.
7. Á **Fyrirsögn** flipa, á **Afhending** Flýtiflipi, staðfestu að **Afhendingarmáti** reiturinn er stilltur á **10**, og **Afhendingarskilmálar** reiturinn er stilltur á **CIF**.
8. Í flýtiflipanum **Línur**, í flýtiflipanum **Innkaupapöntunarlínur**, í reitnum **Vörunúmer**, skal velja **D0003**. Því næst, í reitinn **Magn**, skal færa inn **6**.
9. Á **Upplýsingar um línu** flýtiflipann, á **Utanríkisviðskipti** flipa, staðfestu að **Færslukóði** er stillt á **11**, hinn **Flutningur** reiturinn er stilltur á **3**, hinn **Vöruvara** reiturinn er stilltur á **100 200 30**, og **Upprunaland/upprunaland** reiturinn er stilltur á **DEU**.
10. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerðir**, skal velja **Staðfesta**.
11. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
12. Á aðgerðarrúðunni velurðu **Sjálfgefið frá**, og síðan, í **Sjálfgefið magn fyrir línur** reit, veldu **Pantað magn**. Veljið síðan **Í lagi**.
13. Á **Fyrirsögn lánardrottinsreiknings** flýtiflipann, í **Auðkenning reiknings** kafla, í **Númer** reit, slá inn **00010**.
14. Í **Reikningsdagsetningar** kafla, í **Dagsetning reiknings** reit, veldu núverandi dagsetningu. Þessi dagsetning verður notuð fyrir Intrastat flutning.
15. Í **Fá skjal dagsetningu** reit, veldu **18.10.2021** (18. október 2021).
16. Á aðgerðasvæðinu skal velja **Bóka** til að bóka reikninginn.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Búa til Intrastat-skattskýrslu fyrir komur

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Flutningur**.
3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur lánardrottins** á **Já**.
4. Veldu **Í lagi** til að flytja færslurnar og síðan skoða Intrastat-bókina.

    ![Lína sem táknar innkaupapöntunina á Intrastat síðunni](media/intrastat_pl_4.png)

5. Skoðaðu upplýsingarnar á **Almennt** flipa fyrir innkaupapöntunina.

    ![Upplýsingar um innkaupapöntun á Almennt flipanum á Intrastat síðunni](media/intrastat_pl_5.png)

6. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
7. Í **Intrastat skýrsla** valmynd, á **Færibreytur** flýtiflipann, í **Dagsetning** kafla, í **Frá dags** reit, veldu fyrsta dag núverandi mánaðar.
8. Í hlutanum **Valkostir** **útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**. Í reitinn **Skráarheiti** skal síðan færa inn nauðsynlegt heiti.
9. Stilltu valkostinn **Mynda skýrslu** á **Já**. Í reitinn **Heiti skýrsluskráar** skal síðan færa inn nauðsynlegt heiti.
10. Í reitnum **Stefna** skal velja **Komur**.
11. Í **Kortlagning skráarsniðs** kafla, staðfestu að **Tegund yfirlýsingar** reiturinn er stilltur á **Yfirlýsing**.
12. Í **Borg skjalagerðar** reit, slá inn **Kraká**.
13. Í **Dagsetning skjalagerðar** reit, veldu **19.10.2021** (19. október 2021).
14. Í **Skjal nr** reit, slá inn **11**.
15. Í **Skjalaútgáfa** reit, slá inn **22**.
16. Veldu **Allt í lagi**, og skoðaðu skýrsluna á XML-sniði sem er búið til. Eftirfarandi tafla sýnir gildin í skýrsludæminu.

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
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Borgin þar sem skjalið var búið til.</p>
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
    <p>Heildarfjöldi hluta.</p>
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
    <p>Heildartölfræðileg gildi.</p>
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
    <p>Heildarvirði reiknings.</p>
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
    <p>Einingakóði.</p>
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
    <p>Tegund yfirlýsingarinnar.</p>
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
    <p>Skjalútgáfan.</p>
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
    <p>Skjalnúmerið.</p>
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
    <p>Týp</p>
    </td>
    <td width="332">
    <p>Skýrslustefnan.</p>
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
    <p>Auðkenni yfirlýsingarinnar.</p>
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
    <p>Regon kóða fyrirtækisins.</p>
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
    <p>NIP kóða fyrirtækisins.</p>
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
    <p>Póstnúmer félagsins.</p>
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
    <p>Gatan þar sem fyrirtækið er staðsett.</p>
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
    <p>Nafn félagsins.</p>
    </td>
    <td>
    <p>Contoso skemmtunarkerfi Þýskalandi</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Upplýsingar um hið góða</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Tölfræðilegt gildi.</p>
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
    <p>Reikningsverðmæti.</p>
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
    <p>Kóðinn fyrir upprunalandið eða -svæðið.</p>
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
    <p>Kóðinn fyrir flutningsmáta.</p>
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
    <p>Vörunúmerið.</p>
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
    <p>Viðskiptakóði.</p>
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
    <p>Afhendingarskilmálar.</p>
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
    <p>Kóðinn fyrir landið eða svæði sendingar/áfangastaðarins.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UmsögnTowaru</p>
    </td>
    <td>
    <p>Lýsing á vörunum.</p>
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
    <p>Faxnúmer sendanda.</p>
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
    <p>Símanúmer innsendanda.</p>
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
    <p>Nafn innsendanda.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Farðu yfir skýrsluna á Excel-sniði sem er búið til.

    ![Intrastat skýrsla um komur](media/intrastat_pl_6.png)
