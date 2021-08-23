---
title: Afstemma bankayfirlit með ítarlegri bankaafstemmingu
description: Ítarleg bankaafstemming aðgerð gerir það mögulegt að flytja inn rafrænt bankayfirlit og afstemma þau sjálfkrafa við bankafærslu í Microsoft Dynamics 365 Finance. Þessi skrá útskýrir ferli afstemmingar.
author: saraschi2
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfa999d2aaa4b6dad711bb57916a68fb37c57d9add09092783ad3a8d6450c1f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714449"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Afstemming bankayfirlits með ítarlegri bankaafstemmingu

[!include [banner](../includes/banner.md)]

Ítarleg bankaafstemming aðgerð gerir það mögulegt að flytja inn rafrænt bankayfirlit og afstemma þau sjálfkrafa við bankafærslu í Dynamics 365 Finance. Þessi skrá útskýrir ferli afstemmingar.  

## <a name="import-an-electronic-bank-statement"></a>Flytja inn við rafræna bankayfirlit

Þú flytja inn bankayfirlit þitt með því að nota í **flytja Inn yfirlit** aðgerð á **Bankayfirlit** síðuna. Bankareikningurinn er auðkennd í bankayfirliti með samsetningu gilda sem stillt eru í upplýsingar bankareiknings. Þessi gildi hafa nafn banka, bankareikningsnúmer, leiðarnúmer, auðkenniskóði banka (SWIFT) , og alþjóðlegt bankareikningsnúmer (IBAN). 

Hægt er að hlaða upp bankayfirlit sem inniheldur upplýsingar annað hvort um einn lykil eða marga lykla. Ef um marga lykla er að ræða, geta lykla verið í mismunandi lögaðila.

-   Til að flytja staka bankayfirlitsskránn fyrir einn lykil, er stilltur **Flytja yfirlit fyrir mörgum bankareikningum í öllum lögaðilum** valkostinn til á **Nei**, og veljið bankareikning sem er tengd við yfirlitið. Smellið á **Fletta** til að velja tengda bankayfirlitsskránni og smellið síðan á **hlaða upp**.
-   Til að flytja marga bankayfirlitsskrár fyrir einn lykil, er stilltur **Flytja yfirlit fyrir mörgum bankareikningum í öllum lögaðilum** valkostinn til á **já**. Smellið á **Fletta** til að velja tengda bankayfirlitsskránni og smellið síðan á **hlaða upp**.

Ef eitthvað uppgjör í rafrænni skrá getur ekki verið tengt við bankareikning, eða ef það er tengt með mörgum bankareikningum með auðkennandi svæðunum, verður það ekki flutt inn. Hins vegar er enn hægt að flytja inn önnur yfirlit í skránni. Notandinn fær skilaboð sem tilgreinir að innflutningur bankayfirlits mistókst fyrir tiltekna bankareikninga. Athugið að notandinn sem flytur inn bankayfirlitsskránni þarf að hafa aðgang að lögaðila til að flytja inn yfirlit fyrir bankareikninga þess lögaðila. 

Einnig er hægt að hlaða upp margar yfirlitsskrár í Finance í einu ferli með því að nota zip-skrár. Til að flytja margar bankayfirlitsskrár fyrir marga lykla, skal sameina allar bankayfirlitsskrár í eina zip-skrá. Í á **flytja Inn bankayfirlit** svargluggann er stilltur valkosturinn **flytja Inn yfirlit fyrir mörgum bankareikningum í öllum lögaðilum** á **Já**. Smellið á **Fletta** til að velja zip-skrá sem inniheldur bankayfirlitsskrárnar og smellið síðan á **hlaða upp**. Innflutningsferli þekkja zip-skrá og hleður upp hverju yfirliti sem er innifalin í því, óháð lögaðila bankareikningsins.

Valkosturinn **Stemma af eftir innflutning** er tiltækur. Þegar þessi valkostur er stilltur á **Já**, villuleitar kerfið sjálfkrafa bankayfirlit, stofnar nýja bankaafstemmingu og vinnublað, og keyrir Sjálfgefna samsvörunarreglusettið þegar bankayfirlitið hefur verið hlaðið upp. Þessi aðgerð gerir ferliið sjálfvirkt upp að þeim punkti þar sem færslur þarft að handvirkt jafna.

## <a name="validate-the-bank-statement"></a>Villuleita bankayfirlit
Til að Villuprófa uppgjör, á í **Bankayfirlit** síðu smella **Villuleita** . Bankayfirlit verður að vera villuleituð áður en þær geta verið afstemmdar. Þetta skref er sjálfkrafa klárað ef **Afstemming eftir innflutning** valkostur var stilltur á **Já** við innflutning. 

Villuleit á bankayfirlit staðfestir eftirfarandi upplýsingar:

-   Bankayfirlitið samsvarar völdum bankareikningi.
-   Gjaldmiðill Bankayfirlits samsvarar gjaldmiðli bankareiknings.
-   Opnunarstaða yfirlits jafngildir lokunarstöðu fyrra yfirlits fyrir bankareikninginn.
-   Dagsetning skarast ekki gagnvart dagsetningu annars bankayfirlits fyrir sama bankareikning.
-   Engar eyður eru í dagsetningar fyrir yfirlit fyrir bankareikninginn.
-   Dagsetningar á í uppgjörslínunum eru milli frá-dagsetningu og til-dagsetning bankayfirlits.
-   Opnunarstaða og samanteknar línuupphæðir eru jöfn lokastöðu.

Þegar villuleit er lokið er stöðu á bankayfirlit uppfærð í **sannprófuð**. Bankayfirlit verður að vera villuleituð áður en þær geta verið afstemmdar.

## <a name="reconcile-the-bank-statement"></a>afstemma bankayfirlit
Eftir að þú hefur flutt inn rafræn bankayfirlit og villuleita uppgjör á í **Bankayfirlit** síðu, er hægt að stemma af bankayfirlit með því að nota í **bankaafstemming** og **vinnublað bankaafstemmingar** síður. 

Á **bankaafstemming** síðunni er smellt á **Nýtt** til að stofna nýja afstemmingu, og veljið síðan bankareikninginn yfirlits sem var flutt inn. Bankareikningur getur haft aðeins eina opna bankaafstemmingu. Lokadagsetning ákvarðar bankayfirlitsfærslur og Operations-bankafærslur sem eru innifaldar í vinnublaði bankaafstemmingar. Að sjálfgefnu er núverandi kerfisdagsetning notuð sem lokadagsetning, en hægt er að breyta dagsetningu fyrir afstemmingu. Eftirstandandi upplýsingar úr haus eru sjálfkrafa teknar úr yfirlitinu. Þetta skref er sjálfkrafa klárað ef **Afstemming eftir innflutning** valkostur var stilltur á **Já** við innflutning. 

Á **bankaafstemming** síðunni er smellt á **Vinnublað** til að opna í **vinnublað bankaafstemmingar** síðu. Ef **Afstemming eftir innflutning** valkostur var stillt á **Já**, er Sjálfgefið samsvörunarreglusett sjálfkrafa keyrt fyrir afstemminguna. Til að Keyra samsvörunarreglur handvirkt er smellt á **Keyra samsvörunarreglur** til að velja samsvörunarreglusett eða samsvörunarreglur til að keyra á móti bankafærslur. Ef margar færslur þarf að vinna, er hægt að ljúka þessu skrefi sem runuvinnslu. 

**vinnublað bankaafstemmingar** síða hefur fjóra hnitanet sem innihalda færslur. Tvær efri hnitanet sýna færslur frá bankayfirlit og Operations sem hefur ekki enn verið jafnað. Tvær neðri hnitanet sýna jafnaðar færslur. **upplýsingar um bankayfirlitsfærslur** flipi sýnir upplýsingar um ójöfnuð bankayfirlitsfærslur sem valinn er í efra hnitanetinu. 

Þrjár leiðir eru til að jafna eða afstemma bankayfirlitsfærslur:

-   Jafna færslur með Operations-bankafærslum.
-   Jafna færslur með bakfærslu bankayfirlitsfærslna.
-   Merktu færslur sem **Nýtt** svo það sé hægt að bóka þær síðar sem bankafærslur í Finance.

Til að jafna færslur handvirkt skal velja færslur í **bankayfirlitsfærslur** hnitaneti, velja samsvarandi færslur í á **Operations-bankafærslur** hnitaneti, og smella svo á **Jafna**. Valdar færslur eru fluttar úr efri hnitanet fyrir ójafnaðar færslur í neðri hnitanet fyrir jafnaðar færslur. Þar að auki er ójöfnuð og jöfnuð heildarupphæðir uppfærðar. Hægt er að vera með eina við eina, margar við eina, og margar við margar-færslujafnanir. Samsvaranir verða að að fylgja reglur fyrir leyfðan mismun dagsetninga og vörpun færslugerða. Þessar reglur eru stilltar á **færibreytur reiðufjár- og bankastjórnunar** síðu.

Auramismunur getur komið upp í við afstemmingu. Hægt er að jafna staka bankayfirlitsfærslu og staka Operations-bankayfirlitsfærslu sem hafa auramismun ef auramismunur eru innan vikmörk upphæðar sem er skilgreindur í **Leyfður auramismunur** reitnum á bankareikningi. Upphæðin er sýnd í á **leiðréttingarupphæð** reit á jöfnuðum Operations-bankafærslum. Þegar bankaafstemming er merkt sem afstemmd, eru leiðréttingar bókaðar sjálfkrafa með því að nota aðallykil sem er skilgreind á tengda bankafærslugerð. Leiðréttingar eru ekki studdar fyrir skjalagerðir **Athuga** og **Innborgun**. 

Bankfærslur bankayfirlitsfærslna eru jafnaðar með því að nota vinnublað bankaafstemmingar. Hægt er að jafna tvær uppgjörslínur ef upphæðirnar eru andstæðar, og ef ein færsla er merkt sem bakfærsla. Einnig er hægt að setja upp samsvörunarregla fyrir aðgerðina **Hreinsa bakfærslulínur** .

Bakfærðar Operations bankafærslur Verður að stemma af með því að nota **Operations-bankafærslur** síðu. Hægt er að stemma af tveimur Operations-bankafærslur saman ef skjölin eru með sama bankareikning, gerð skjals og greiðslutilvísun og ef þær hafa andstæðar upphæðir. Einnig er Hægt er að stemma af eina ávísun sem hætt var við til að koma í veg fyrir þær færslur birtist á vinnublað afstemmingar. 

Ef til staðar eru færslur sem bankinn hefur frumkvæði að, eins og vexti, þóknanir og gjöld sem ekki eru enn í Finance, er hægt er að bæta þeim við færslubók sem er tengt við valda afstemmingu bankayfirlits. Velja bankayfirlitsfærslu í á **bankayfirlitsfærslu** hnitaneti fyrir ójöfnuð færslur og smelltu svo á **Merkja sem nýtt**. Staða færslunnar er stillt á **Nýtt**, og færsla er færð í **bankayfirlitsfærslur** hnitaneti fyrir jafnaðar færslur. Þú munt bóka færslur sem eru merktar sem **Nýtt** síðar, úr síðunni **Bankayfirlit** . 

Hægt er að fjarlægja jöfnun færslna sem rangt var jafnað. Velja skal jafnaða bankayfirlitsfærslu og smella síðan á **afjafna**. Allar tengdar færslur eru færð aftur í efri hnitanet fyrir ójöfnuð færslur, og jafnaðar og ójafnaðar heildarupphæðir eru uppfærðar. 

Að afstemmingarferli loknu á að merkja vinnublað bankaafstemmingar sem afstemmt.  Ferlið mun sjálfkrafa birta leiðréttingarupphæðir með því að nota reikningana sem eru stilltir á síðunni **Færslugerð banka**.  Bankaafstemming fyrir uppgjör er hægt að merkja sem afstemmda hvenær sem er, jafnvel þó að það séu bankayfirlitslínur sem ekki stemma saman.  Færslur án samsvörunar færast sjálfkrafa yfir á næsta afstemmingarblað sem færslur á bankayfirliti án samsvörunar til afstemmingar.  Athugaðu að þegar afstemming bankayfirlits hefur verið lokið er ekki hægt að afturkalla hana.  Afstemmingin verður ekki lengur breytanleg og þú munt ekki lengur geta uppfært afstemminguna.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Bóka nýjar færslur sem tengjast valinni afstemmingu.
Bankayfirlitsfærslur sem voru merktar sem **Nýtt** á afstemmingarvinnublaði eru bókaðar á **Bankayfirlit** síðu. Á **Bankayfirlit** síðunni, veljið Kenni uppgjörs til að skoða upplýsingar um yfirlit. Á **Bókhald** valmyndinni, er hægt að nota **Skoða dreifingu** og **Skoða bókhald** valkosti til að skoða upplýsingar um nýjum færslum og tengdar fjárhagsfærslur. Velja skal **Bóka** valkost til að bóka bankayfirlitslínur sem merktar eru sem **Nýtt** í fjárhag. Athugaðu að bókun má ljúka aðeins einu sinni fyrir hvert bankayfirlit.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]