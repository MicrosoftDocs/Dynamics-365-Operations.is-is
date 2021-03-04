---
title: Grunnstilla gerðir viðburða
description: Microsoft Dynamics 365 Human Resources notar tegundir atburða í lífinu til að skilgreina atburði þar sem það gildir að uppfæra skráningu starfsmannabóta.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419010"
---
# <a name="configure-life-event-types"></a>Grunnstilla gerðir viðburða

Microsoft Dynamics 365 Human Resources notar gerðir viðburða til að skilgreina tilvik þar sem það gildir að uppfæra skráningu starfsmannabóta. Til dæmis að giftast eða eignast barn. Auðkenni hvers lífsviðburðar má aðeins tengjast einni tegund atburðar. Til dæmis, ef þú býrð til lífsviðburðarauðkenni sem heitir Heimilisbreyting sem er tengd lífbreytingartegundinni Breyting á heimilisfangi starfsmanna, geturðu ekki búið til annað kennimerki sem er merkt heimilisfang breytinga á starfsmanni og tengt það við atburðinn fyrir lífsviðgerð Breyting á heimilisfangi starfsmanna. 

Eftir að þú hefur búið til tegundir af atburðum í lífinu þarftu að tengja þær við áætlunartegundir. Nánari upplýsingar sjá [Stofna áætlunargerðir](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Þegar þú hefur búið til viðburð þarftu að tengja hann við áætlunargerð. Nánari upplýsingar sjá [Stofna áætlunargerðir](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>Búðu til viðburðagerð

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Gerðir viðburða**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Auðkenni gerðar viðburðar** | Einkvæmt auðkenni viðburðargerðar. |
   | **Lýsing** | Lýsing á gerð viðburðar. |
   | **Gerð viðburðar** | Hvati til að uppfæra skráningu starfsmanna á fríðindum. Sjá lista yfir atburði í lífinu [Viðburðir](hr-benefits-setup-payment-frequencies.md?life-events) hér að neðan. |

4. Veljið **Vista**.

## <a name="view-attached-plans"></a>Skoða viðhengdar áætlanir

Þú getur séð lista yfir áætlanir sem eru tengdar völdum tegund atburðar. Viðburðir eru tengdir áætlunartegundum og áætlunartegundir tengjast áætlun. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Gerðir viðburða**.

2. Velja **Aðgerðir**.

3. Veldu **Meðfylgjandi áætlanir**.

## <a name="life-events"></a>Viðburðir

Þú getur valið úr eftirfarandi lífsviðburðum þegar þú býrð til gerð atburðar í lífinu:

| Viðburður | Staðsetning | Kveikja |
| --- | --- | --- |
| **Breyting á hjúskaparstöðu** | Verkamaður > Snið > Persónulegar upplýsingar > Hjúskaparstaða| Breyting á hjúskaparstöðu |
| **Breyting á atvinnustöðu** | <ul><li>Starfskraftur > Starf</li><li>Síðan Starfssaga</li></ul> | Breyting á starfsstöðu |
| **Breyting á heimilisfangi starfsmanns** | <ul><li>Verkamaður > Forstilling > Heimilisföng </li><li>Verkamaður > Persónulegar upplýsingar > Persónulegir tengiliðir > Heimilisfang</li></ul> Bætt við, breytt eða eytt heimilisfangi |
| **Breyting á skjólstæðingi** | <ul><li>Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > Bæta við eða eyða háðum</li><li>Sjálfsafgreiðsla starfsmanns</li></ul> | Bætt við eða eytt háð. Persónuleg tengsl verða að vera barn, maki, sambýlismaður/-kona eða fyrrverandi maki. Uppfærsla á **Gildir frá** dagsetningu kveikir viðburð. Ef þú uppfærir ekki þessa dagsetningu mun enginn viðburður kvikna. |
| **Fæðing eða ættleiðing (skjólstæðingur)** | <ul><li>Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing</li><li>Sjálfsafgreiðsla starfsmanns</li></ul> | **Samþykktardagsetning** reiturinn útfylltur. Fæðingardagsetning barns er krafist. |
| **Missir tryggingar (maki/sambúðaraðili)** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Missir tryggingar | **Missir tryggingar** valinn fyrir persónulegan tengilið ásamt **Gildistökudagur** |
| Breytingar á atvinnu sambúðaraðila | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Ráðin/n. | <ul><li>Upplýsingaskrá um skjólstæðing stofnuð og **Persónulegur tengiliður ráðinn** kassi = Já</li><li>**Persónulegur tengiliður ráðinn** reitnum breytt (já eða nei)</li></ul> |
| **Fjarvistarleyfi (maki/sambúðaraðili)** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Fjarvistarleyfi | <ul><li>Upplýsingaskrá um skjólstæðing stofnuð og **EhrLOAEffectiveDate** fyllt út</li><li>**personPrivateDetails.EhrIsLOA** er breytt (já eða nei)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** er breytt</li></ul> |
| **Breyting á tryggingu (stöðu)** | <ul><li>Starfskraftur > Stöðuúthlutun > Stöðuúthlutanir starfskrafta</li><li>Stöður > Stöður</li></ul> | <ul><li>Skiptu um stöðu í verkefnaupplýsingaskrá starfsmanna</li><li>Breyting á úthlutun starfskrafts í stöðuna</li></ul> |
| **Medicare (starfsmaður/skjólstæðingur)** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Gildisdagsetning Medicare | Ekki hrundið af stað sjálfkrafa þegar persónulegur tengiliður tekur gildi gildandi dagsetningu. |
| **Stuðningur samkvæmt dómsúrskurði** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > Ósjálfstætt > Dómstóll skipaði stuðning (QMSCO / QDRO og gildistökudagar) | Kemur ekki fram neinum sjálfvirkum uppfærslum. Það hefur ekki áhrif á hæfi; það skráir atburði í lífinu. |
| **Látin(n)** | Verkamaður > Snið > Persónulegar upplýsingar > Dagsetning andláts | Dagsetning andláts er færð inn |
| **Sönnun fyrir tryggingu** | <ul><li>Verkamaður > Verkamaður > Útgáfur > Atvinnusaga > Dagsetningastjóri > Upplýsingar um bætur</li><li> Verkamaður > Atvinna > Upplýsingar um bætur > Staðfestingardag</li></ul> | <ul><li>Starfsmaður fer inn á staðfestingardag</li><li>Starfsmaður setur EvidenceOfInsurability sviðið á **Já**</li></ul> |
| **Rétthafi** | Verkamaður > Forstilling > Persónulegar upplýsingar > Persónulegir tengiliðir | Persónulegum samskiptum er bætt við og **Rétthafi** kassi og **Gildistökudagur** eru byggðar. Persónuleg tengsl verða að vera af gerðinni **Child**, **Spouse**, **DomesticPartner**, **Sibling**, **FamilyContact**, **OtherContact**, **Parent**, **BeneficiaryEstate**, **BeneficiaryOrg** eða **BeneficiaryTrust**. |
| **Medicare starfsmanns** | Verkamaður > Verkamaður > Útgáfur > Atvinnusaga > Dagsetningastjóri > Upplýsingar um bætur | <ul><li>**EhrMedicareEligibilityDate** er breytt</li><li>**MedicareEligibile** er stillt á **Já**</li></ul> |
| **Fæðingardagur** | Verkamaður > Prófíll > Persónulegar upplýsingar > Persónulegir tengiliðir > upplýsingar um skjólstæðing > Afmælisdagur. | Fæðingardagur er bætt við eða uppfærður (ekki eftir að lífsviðburðarbreyting hefur verið afgreidd). Dæmi: Ef **Hæfiskostir persónulegs tengliðar** fyrir barn er stillt á Aldur: 26 í Uppsetning > Bætur > Hæfiskostir persónulegs tengliðar, og ef starfsmenn HR reka vinnslu á atburði í lífsháttum einhvern dag eftir að hinn ávani verður 26 ára, birtast skilaboð þar sem þeim er tilkynnt að hinn háði sé ekki lengur gjaldgengur. |
| **Breytingar á hæfi starfsmanna (ekki sérstakar í Bandaríkjunum)** | <ul><li>Starfskraftur > Starf</li><li>Verkamaður > Verkamaður > Útgáfa > Atvinnusaga</li></ul> | <ul><li>Gerð starfsmanna, atvinnu flokkur eða fimm hæfnisviðin notandi breytast</li><li>**HcmEmploymentDetail.EhrEmploymentType** breytingar (aðeins unnar fyrir *breyttar* atvinnuupplýsingar, ekki unnar fyrir *nýjar* atvinnuskrár, eins og endurráðningu og uppsögn)</li></ul> |
| **Nýr hnekki á hæfi (ekki sérstakur í Bandaríkjunum)** | Human resources háþróaður > Fríðindi > Áætlanir > Fríðindi > Hæfisregla hnekkt | Notkun lífsviðburða | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Breyting á hnekkingu hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | Human resources háþróaður > Fríðindi > Áætlanir > Fríðindi > Hæfisregla hnekkt | Nota viðburðavinnslu (afla aðeins breytingar á **Gildir frá** og **Gildir til** reitir á hæfisreglu hnekkja) |
| **Gildislok á hnekkingu hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | Human resources háþróaður > Fríðindi > Áætlanir > Fríðindi > Hæfisregla hnekkt | Breytingavinnsla á Notkun lífsviðburða. Til dæmis, ef þú breytir hæfisreglu áætlunarinnar hnekki gildistíma til að vera í dag kl. 17:00, hvenær sem er eftir kl. 17:00 eða næstu daga á eftir og keyra síðan vinnslu á atburði á Lífsviðburði, birtast skilaboð sem segja að hæfisreglan hnekkt er útrunnið. |
| **Ný bótakerfi (ekki sérstök í Bandaríkjunum)** | Human resources háþróaður > Fríðindi > Áætlanir > Nýtt | <ul><li>Gildisvalkostir bætast við núverandi áætlun</li><li>Ný áætlun með hæfileikum meðfylgjandi er bætt við</li></ul></br></br>Starfsmenn HR ættu að stjórna hæfileikaframkvæmdum í Lífsmóti í þessu tilfelli. |
| **Breyting á hæfisreglu (ekki sértækt fyrir Bandaríkjunum)** | Human resources háþróaður > Fríðindi > Reglur/valkostir > Hæfisreglur | Hæfisvinnsla á Notkun lífsviðburða. Skráð hvenær **EhrBenefitEligibilityRule** skrár hafa eftirfarandi gildum breytt: **UseEmplCategory**, **UseEmplStatus** eða **UseEmplType**. Aðeins uppfærir viðskipti með lífatburði sem þegar eru til vegna breyttrar reglu eða hæfisskilyrða. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]