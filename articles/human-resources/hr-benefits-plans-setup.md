---
title: Búa til fríðindaáætlun
description: Uppsetning fríðindaáætlana í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e3822a1071023898e459a82c14ff648d8cdebed
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230109"
---
# <a name="create-a-benefits-plan"></a>Búa til fríðindaáætlun

Þessi grein sýnir þér hvernig á að setja upp fríðindaáætlun í Dynamics 365 Human Resources.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veljið **Nýtt**.

3. Í flipanum **Almennt** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Fyrirkomulag** | Einkvæmt auðkenni fyrir áætlunina. |
   | **Lýsing** | Lýsing á áætluninni. |
   | **Gerð áætlunar** | Þegar þú býrð til nýja áætlun þarftu að tilgreina gerð áætlunarinnar. Áætlun gerð er há stigi flokkun á tilteknum tegundum af fríðindum. Hver áætlunartegund tilgreinir hvort starfsmaður geti skráð sig í margar áætlanir af þeirri gerð, tilgreinir hvort tengiliðir séu styrkþegar eða á framfæri og skilgreini umfjöllunarvalkosti. Þú getur búið til nýjar sérsniðnar áætlunartegundir til að uppfylla þarfir á fríðindatilboðum þínum. Helstu tegundir fríðindaáætlana eru: <ul><li>401K</li><li>ADD</li><li>Tannlæknaþjónusta</li><li>Líkamsrækt</li><li>FSA</li><li>Viðburður</li><li>LTD</li><li>Heilsufar</li><li>PTO</li><li>STD</li><li>Sýn</li></ul> |
   | **Gerð kóða áætlunargerðar** | Kóði áætlunartegundar áætlunartegundarinnar. |
   | **Áætlun** | Tilgreinir forrit til að tengja áætlunina mögulega. |
   | **Búnt** | Tilgreinir búnt til að tengja áætlunina mögulega. |
   | **Næstefsta stig** | Tilgreinir hvort áætlunin sem aðaláætlunin í búntinu sem hún tilheyrir. |
   | **Staða** | Tilgreinir gildandi stöðu á fríðindaáætlunar. Sjálfgildið er Virkt. Ef þú breytir stöðunni í Óvirk er áætlunin ekki tiltæk sem val við innritun. |
   | **Gildir frá dagsetningu og tíma** | Lokadagsetning og tími þegar áætlunin hefst. Sjálfgefið gildi er núverandi kerfisdagsetning. |
   | **Gildir til dagsetningu og tíma** | Dagsetningin og tíminn sem áætluninni lýkur (staðan er stillt á Óvirk). Sjálfgefið gildi er 12/31/2154, sem táknar aldrei. |

4. Á **Stillingar** flipann, tilgreindu gildi fyrir eftirfarandi reiti, allt eftir gerð áætlunarinnar sem þú ert að búa til:

   | Gerð áætlunar | Svæði | Lýsing |
   | --- | --- | --- |
   | Medical (Medical, Dental, Vision, HMO) | COBRA-skráning | Tilgreinir hvort áætlunin sé gjaldgeng COBRA (Consolidated Omnibus Budget Reccilciliation Act). |
   | Medical (Medical, Dental, Vision, HMO) | HIPAA-skráning | Tilgreinir hvort áætlunin sé HIPAA (lögum um umgengni og ábyrgð á heilbrigðistryggingum) hæf. |
   | <ul><li>Medical (Medical, Dental, Vision, HMO)</li><li>Annað (PTO, líkamsrækt)</li><li>Annað</li><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li><li>Sparnaður (til dæmis 401 (k))</li><li>FSA</li></ul> | Hæfni fyrir skatt | Tilgreinir hvort hægt sé að leggja framlög til áætlunarinnar áður en skattar eru lagðir á. |
   | <ul><li>Medical (Medical, Dental, Vision, HMO)</li><li>Annað (PTO, líkamsrækt)</li><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li><li>Sparnaður (til dæmis 401 (k))</li><li>FSA</li></ul> | Hæfni eftir skatt | Tilgreinir hvort hægt sé að leggja framlög til áætlunarinnar eftir að skattar eru lagðir á. |
   | <ul><li>Medical (Medical, Dental, Vision, HMO)</li><li>Annað (PTO, líkamsrækt)</li><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li><li>Sparnaður (til dæmis 401 (k))</li><li>FSA</li></ul> | Framlagsveitandi | Tilgreinir hver leggur sitt af mörkum til áætlunarinnar - starfsmaður, vinnuveitandi eða báðir. |
   | <ul><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li></ul> | Trygging að lágmarki | Lágmarksfjárhæð tryggingar sem krafist er vegna áætlunarinnar. |
   | <ul><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li></ul> | Trygging að hámarki | Hámarksfjárhæð tryggingar sem krafist er vegna áætlunarinnar. |
   | <ul><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li></ul> | Nota stigvaxandi tryggingu | Tilgreinir hvort staðfesta skuli að tryggingarupphæðin passi við gilda hækkandi upphæð. |
   | <ul><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li></ul> | Stigvaxandi upphæð | Hækkandi fjárhæð tryggingar sem krafist er vegna áætlunarinnar. Til dæmis, ef stigaupphæðin er 1.000, starfsmaður getur ekki haft $200.500 af tryggingum, þá þyrftu þeir að ná saman upp að $201.000 eða niður í $200.000. |
   | <ul><li>Örorkubætur til lengri tíma</li><li>Bæta við (grunnlífi, frjálsu lífi)</li></ul> | Stigvaxandi átt | Tilgreinir átt jöfnunar, annað hvort upp eða niður, þegar tryggingarupphæðin fullnægir ekki upphæðargildi hækkunarinnar. |
   | Bæta við (grunnlífi, frjálsu lífi) | Sönnun fyrir tryggingarhæfi | Tilgreinir hvort starfsmaður verði að leggja fram vísbendingar um tryggingarhæfni. |
   | Bæta við (grunnlífi, frjálsu lífi) | Upphæð | Upphæðin í bókhaldsgjaldmiðli. Þetta reitur er aðeins virkur ef gátreiturinn Sannanir á tryggingarhæfni er valinn. |
   | <ul><li>Sparnaður (til dæmis 401 (k))</li><li>FSA</li></ul> | Lágmarksframlag á ári | Lágmarksfjárhæð framlags sem krafist er vegna áætlunarinnar. |
   | <ul><li>Sparnaður (til dæmis 401 (k))</li><li>FSA</li></ul> | Hámarksframlag á ári | Hámarksfjárhæð framlags sem krafist er vegna áætlunarinnar. |
   | Sparnaður (til dæmis 401 (k)) | Hámarksupphæð vinnuveitanda á ári | Hámarksfjárhæð sem vinnuveitanda er heimilt að leggja til í sparnaðaráætlun starfsmanna á fríðindatímabili. Þú verður að velja gátreitinn Starfsmannajöfnun til að nota þennan reit. |
   | Sparnaður (til dæmis 401 (k)) | Samsvörun vinnuveitanda | Tilgreinir hvort starfsmaður leggur sitt af mörkum við sparnaðaráætlun starfsmanns. |
   | Sparnaður (til dæmis 401 (k)) | Samvörunarprósenta vinnuveitanda | Hlutfall framlags starfsmanns sem vinnuveitandinn mun jafna. |
   | Sparnaður (til dæmis 401 (k)) | Hámarkssamsvörun vinnuveitanda | Hámarkshlutfall sem vinnuveitandinn mun jafna. Til dæmis, ef vinnuveitandi mun jafna 100% af framlögum starfsmanna upp að 6% af launum starfsmanns, er samsvörunartak vinnuveitanda 6%. |

5. Í flipanum **Uppsetning** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Leyfa/halda við skráningu** | Tilgreinir hvort starfsmenn geti skráð sig í áætlunina ef þeir uppfylla hæfiskröfur.</br></br>Ef þetta er stillt á Nei verður áætlunin ekki tiltæk starfsmönnum þegar þú afgreiðir hæfi. |
   | **Sjálfvirk skráning frá fyrra ári** | Tilgreinir hvort skrá skuli skrá hæfan starfsmann sjálfkrafa í áætlunina ef hann var skráður árið á undan. |
   | **Sjálfgefin, sjálfvirk skráning** | Tilgreinir hvort sjálfkrafa eigi að velja áætlunina fyrir innritun. Áætlunin er ekki skylda, þannig að starfsmaðurinn getur breytt sjálfgefnu valinu. |
   | **Lokað er fyrir nýskráningar** | Tilgreinir hvort takmarka eigi áætlunina við aðeins hæfa starfsmenn sem voru skráðir í áætlunina árið áður. |
   | **Áskilin áætlun** | Tilgreinir hvort skrái eigi starfsmenn sjálfkrafa í áætlunina. Starfsmenn geta ekki breytt skráningarvalinu. |
   | **Stofndagur** | Dagsetningin sem áætlunin var búin til í fyrirtækinu. |
   | **Söluaðilareikningur** (fríðindabirgir) | Söluaðilinn sem fyrirtækið greiðir iðgjöld fyrir áætlunina. |
   | **Heiti** (fríðindabirgir) | Nafn lánardrottins. |
   | **Söluaðilatilvísun** (fríðindabirgir) | Tilvísun seljanda vegna áætlunarinnar. Til dæmis hópáætlunarnúmer fyrirtækisins. |
   | **Önnur tilvísun** (fríðindabirgir) | Önnur tilvísun seljanda vegna áætlunarinnar. Til dæmis reikningsnúmer fyrirtækisins. |
   | **Gjaldmiðill** (fríðindabirgir) | Gjaldmiðillinn sem er notaður til að greiða iðgjöld til birgjans. |
   | **Kostnaðarreikningur** (fríðindabirgir) | Almennur reikningur sem notaður er sem kostnaðareikningur vegna iðgjalda. |
   | **Söluaðilareikningur** (fríðindastjórnandi) | Söluaðilinn sem fyrirtækið greiðir til að stjórna áætluninni. Ef áætlunin er sjálfsstýrð, skyldu svæðið eftir autt. |
   | **Nafn** (fríðindastjórnandi) | Nafn lánardrottins fríðindastjórnanda. |
   | **Söluaðilatilvísun** (fríðindastjórnandi) | Tilvísun stjórnandalánardrottins vegna áætlunarinnar. |
   | **Önnur tilvísun** (fríðindastjórnandi) | Önnur tilvísun stjórnandalánardrottins vegna áætlunarinnar. |
   | **Gjaldmiðill** (fríðindastjórnandi) | Gjaldmiðillinn sem er notaður til að greiða fríðindastjórnanda. |
   | **Kostnaðarreikningur** (fríðindastjórnandi) | Almennur reikningur sem er notaður sem kostnaðareikningur fyrir kostnað sem fylgir stjórnun áætlunarinnar. |

6. Á flipann **Síur**, síaðu eftir þörfum. Þú getur síað eftir eftirfarandi reitum:

   - **Viðskiptaeining**
   - **Deild**
   - **Lögaðili**
   - **Staðsetning**
   - **Staða**

7. Í flipanum **Hæfnireglur** skal tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Línunúmer** | Línunúmer hæfnireglu. |
   | **Hæfnisregla** | Hæfniregla sem gildir um fríðindaáætlunina. Þessi hæfisregla verður notuð á samsvarandi aðgerðartegund og tengd tilgreindum biðtíma og frádrætti umfjöllunar. |
   | **Gerð aðgerðar** | Aðgerðin til að beita hæfisreglunni á: skráning fríðinda eða lokadagur fríðinda. |
   | **Biðtími tryggingar** | Gildi frá formi biðtíma. Biðtímabil umfjöllunar er sá fjöldi daga eða mánaða sem starfsmaður bíður eftir umfjöllun um bætur eða rennur út bætur miðað við forsendur hæfisreglunnar og gerðar aðgerða. |
   | **Biðtími frádráttar** | Gildi frá formi biðtíma. Biðtímabil frádráttar er sá fjöldi daga eða mánaða sem starfsmaður bíður eftir umfjöllun um frádrátt frá fríðindum af launagreiðslu sinni miðað við forsendur hæfisreglunnar og gerðar aðgerða. |

8. Veljið **Vista**.

## <a name="view-enrolled-workers"></a>Skoða skráða starfskrafta

Hægt er að skoða starfskrafta sem eru skráðir í valda fríðindaáætlun.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldur **Skráða starfskrafta**.

## <a name="attach-coverage-options"></a>Hengja tryggingarvalkosti við

Þú getur bætt umfjöllunarvalkostum við valið fríðindakerfi. Með því að festa umfjöllunarvalkosti kemur saman hlutfall og frádráttaruppsetning fyrir umfjöllunarvalkost.  Dæmi: Fyrir læknisáætlun myndi notandinn velja valkost fyrir fjölskyldu.  Þeir þyrftu þá að velja Fjölskylduhlutfall fyrir tilheyrandi áætlun (stillt í uppsetningu á hlutfalli) og frádráttur fyrir viðkomandi áætlun (stillt í uppsetningu á hlutfalli). Þetta gefur kostnað vinnuveitanda og starfsmanns fyrir valda tryggingu. Síðan myndir þú endurtaka ferlið fyrir starfsmann + 1 tryggingu eða tryggingu starfsmanna.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldu **Bættu við tryggingarvalkostum**.

## <a name="override-eligibility-rules"></a>Hnekkja hæfnireglum

Þú getur bætt starfsmönnum við áætlun sem undantekningar frá hæfisreglunum. Hver starfsmaður sem þú bætir við er gjaldgengur í fríðindaáætlunina.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldu **Hnekkingar á hæfnireglu**.

## <a name="view-attached-periods"></a>Skoða tengd tímabil

Þú getur séð lista yfir tiltæk fríðindatímabil.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldu **Tímabil**.

## <a name="view-plan-information"></a>Skoða upplýsingar um áætlun

Þú getur gefið lýsingu á áætluninni til að hjálpa starfsmönnum við val þeirra á fríðindum. Upplýsingar um áætlunina sem þú slærð inn birtast í sjálfsafgreiðslu starfsmanna þegar þú sveima á áætluninni í lista yfir valkosti yfir tryggingar.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldu **Áætlunarupplýsingar**.

## <a name="view-flex-credit-programs"></a>Skoða sveigjanlegar útgjaldaáætlanir

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Áætlanir**, veldu **Fríðindaáætlanir**.

2. Veldu **sveigjanlegar útgjaldaáætlanir**.
