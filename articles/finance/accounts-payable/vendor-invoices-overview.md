---
title: Yfirlit yfir reikninga lánardrottna
description: Þetta efnisatriði veitir almennar upplýsingar um reikninga lánardrottins.
author: abruer
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0299eb3470f500bf469c3367f1c426715067a5dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993317"
---
# <a name="vendor-invoices-overview"></a>Yfirlit yfir reikninga lánardrottna

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir almennar upplýsingar um reikninga lánardrottins. Reikningar lánardrottins eru beiðnir um móttekna greiðslu fyrir vörur og þjónustu. Lánardrottnareikningar geta táknað reikning fyrir yfirstandandi þjónustu, eða þeir geta verið byggðir á innkaupapöntunum fyrir tilteknar vörur og þjónustu.

## <a name="vendor-invoices"></a>Reikningar frá lánardrottni

Reikningur lánardrottins úr innkaupapöntun er búinn til þegar afurðir eða þjónustur eru mótteknar samkvæmt innkaupapöntun sem var gerð hjá lánardrottni. Reikningur lánardrottins inniheldur haus og ein eða fleiri línur fyrir vörur eða þjónustu. Reikningur lánardrottins lýkur ferlinu úr innkaupapöntun til innhreyfingarskjals afurðar til reiknings lánardrottins.

Þó að sumir reikningar lánardrottins tengist við innkaupapöntun, getur reikninga lánardrottins líka innihaldið línur sem samsvara ekki innkaupapöntunarlínum. Hægt er að búa líka til reikninga lánardrottna sem eru ekki tengdir við neinar innkaupapantanir. Þessir reikningar lánardrottins gætu staðið fyrir yfirstandandi þjónustu eins og rafmagnsreikningi. Ekki þarf að vísa í innkaupapöntun þegar yfirstandandi þjónustu er bætt við.

Það eru nokkrar leiðir til að færa inn reikning lánardrottins:

- Komubók lánardrottins gerir kleift að slá hratt inn reikninga sem ekki vísa til innkaupapöntunar, þannig að hægt er að safna upp kostnaðinum. Með því að nota samþykktarbók reikninga lánardrottins, er hægt að velja þá reikninga og bóka á stöðu lánardrottna til að bakfæra uppsöfnun.
- Reikningabók lánardrottins leyfir þér að færa inn reikninga fljótt sem ekki vísa til innkaupapöntun, í einu skrefi.
- Ásamt Reikningasafn lánardrottna, leyfir komubók lánardrottins að slá hratt inn reikninga til að safna upp kostnaðar. Hægt er að opna tengd innkaupapantanir seinna til að bóka reikning gagnvart á kostnaðarlykil.
- **Opna lánardrottnareikninga** og **Biðreikninga lánardrottins** síður gera mögulegt að stofna reikninga lánardrottna frá staðfestar innkaupapantanir.

Eftirfarandi umræðu veita meiri upplýsingar um hvernig á að nota síðurnar **Opna lánardrottnareikninga** eða **Biðreikninga lánardrottins** til að búa til reikning lánardrottins úr innkaupapöntun.

## <a name="understanding-invoice-line-quantities"></a>Skilja magn reikningslínu

Þegar reikningur lánardrottins er opnaður úr tengdri innkaupapöntun stofnar kerfið reikningslínur úr innkaupapöntuninni. Kerfið tekur að sjálfgefnu magnið úr innhreyfingarskjali afurðar. Hins vegar er hægt að nota eitthvað af eftirfarandi sjálfgefinni hegðun:

- **Magn sem móttaka á nú** – Nota þennan valkost fyrir hlutasendingar. Kerfið stilltir sjálfgefna gildið í **Magninu** úr magninu sem er gefið upp í reitnum **Móttekið nú** í innkaupapöntuninni.
- **Pantað magn** – hægt er að Nota þennan valkost fyrir fullbúnar sendingar. Kerfið stilltir sjálfgefna gildið í **Magninu** úr magninu sem er gefið upp í reitnum **Pantað** í innkaupapöntuninni.
- **Skráð magn** – notið þennan valkost ef varan þarfnast skráningar sem tilgreind er í **vörulíkanaflokkur** síðu. Sjálfgefna gildið í svæðinu **magn** er efnislega uppfærslumagnið sem hefur verið skráð.
- **Magn á innhreyfingarskjali afurða** – Notið þennan valkost ef innhreyfingarskjal afurða hefur þegar verið móttekinn fyrir pöntuninni. Kerfið tekur sjálfgefna gildið í reitnum **Magn** úr heildarmagni tiltækra innhreyfingarskjala afurða.
- **Skráð magn og þjónustur** – Notið þennan valkost ef magn hefur verið skráð í komubókum fyrir vörur í birgðum eða vörur sem ekki eru í birgðum. Þessi valkostur inniheldur einnig þjónustu, án tillits til þess hvort hún sé skráð.

Ef lögaðili þinn notar reikningsjöfnun, geturðu skoða niðurstöður úr jöfnun magns í **jöfnun magns fyrir Innhreyfingarskjal afurða** dálkur. Einnig er hægt að nota hnappinn **Jöfnunarupplýsingar** í **Yfirfara** flipanum í aðgerðarúðunni til að skoða niðurstöður jöfnunar magns.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Bæta við línu sem ekki var á innkaupapöntun

Hægt er að bæta við línu sem ekki var á innkaupapöntun við reikning lánardrottins. Velja verður við vörunúmer eða innkaupategund. Þá er Hægt að bæta magn, verð og upphæðir á línu. Línan verða teknar með aðeins í jöfnunarreglur fyrir heildarupphæð reiknings.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sendir reikning lánardrottins til yfirferðar

Fyrirtækið gæti notað verkflæði til að stjórna endurskoðunarferli fyrir lánardrottnareikninga. Hægt er að nota verkflæði yfirferðar fyrir reikningshausa, reikningslínu, eða bæði. Verkflæðisstýringin á við haus eða línu, eftir því hvað áherslan liggur áður en stýringin er valin. Í staðinn fyrir hnappinn **Bóka** sýnir **Senda inn** hnappur sendingu lánardrottnareiknings í gegnum ferli yfirferðar.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Kemur í veg fyrir að reikningur verði sendur inn í verkflæði 

Eftirfarandi eru nokkrar leiðir til að koma í veg fyrir að reikningi sé sent inn í verkflæði.

- **Heildarupphæð reiknings og skráðar heildartölur stemma ekki.** Sá sem sendi inn reikninginn fær viðvörun um að samtölurnar séu ekki jafnar. Viðvörunin býður upp á tækifæri til að leiðrétta stöður áður en reikningurinn er sendur aftur í verkflæðið. Þessi eiginleiki er tiltækur ef kveikt er á færibreytunni **Banna innsendingu í verkflæði þegar heildarupphæð reiknings og skráð heildarupphæð reiknings stemma ekki** á síðunni **Eiginleikastjórnun**. 

- **Reikningur inniheldur óúthlutuð gjöld.** Sá eða sú sem sendi inn reikninginn mun fá viðvörun um að reikningurinn sé með óúthlutuð gjöld svo viðkomandi geti leiðrétt reikninginn áður en hann er sendur aftur í verkflæði. Þessi eiginleiki er tiltækur ef kveikt er á færibreytunni **Banna innsendingu í verkflæði þegar það eru óúthlutuð gjöld á reikningi lánardrottins** á síðunni **Eiginleikastjórnun**.

- **Reikningur inniheldur sama reikningsnúmer og annar bókaður reikningur.** Sá eða sú sem sendi inn reikninginn mun fá viðvörun um að reikningur með tvítekið númer hafi fundist svo viðkomandi geti leiðrétt hann áður en hann er sendur aftur í verkflæði. Þessi viðvörun verður birt þegar færibreytan **Athuga notað reikningsnúmer** í viðskiptaskuldum er stillt á **Hafna afriti**. Þessi eiginleiki er tiltækur ef kveikt er á færibreytuni **Banna innsendingu í verkflæði þegar reikningsnúmerið er þegar til á bókuðum reikningi og kerfið er ekki sett upp til að samþykkja tvítekin reikningsnúmer** á síðunni **Eiginleikastjórnun**.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Jafna lánardrottnareikninga við innhreyfingarskjöl afurða

Hægt er að færa inn og vista upplýsingar fyrir reikninga lánardrottins og hægt er að jafna reikningslínur við línur í innhreyfingarskjali afurðar. Einnig er hægt að jafna hlutamagn fyrir línu

Hægt er að stofna reikning lánardrottins á grundvelli línuvara innhreyfingarskjals afurða sem hafa verið mótteknar fram að þessu, jafnvel þó allar vörurnar fyrir tiltekna innkaupapöntun hafa ekki verið mótteknar enn. Til dæmis er hægt að nota þennan valkost ef lánardrottinn sendir einn reikning á mánuði sem nær yfir allar afhendingar sem eru sendar þennan mánuð. Hvert innhreyfingarskjal afurða birtir hluta eða alla afhendingu varanna á innkaupapöntuninni.

Þegar reikningur er í verkflæði getur samþykktaraðili uppfært reikningsmagn þannig að það samsvari gildinu í reitnum **Magn innhreyfingarskjals afurðar til jöfnunar**. Til að gera það skal velja eiginleikann **Uppfæra reikningsmagn til að samsvara magni innhreyfingarskjals afurðar í verkflæði** á vinnusvæðinu **Eiginleikastjórnun** og velja **Virkja**. Ef samþykktaraðili í verkflæðisferlinu hefur fjarlægt allar jafnanir frá öllum innhreyfingarskjölum afurða úr reikningslínunni, verður reikningslínunni eytt. Þegar þessi eiginleiki er ekki virkur verður reikningsmagn ekki uppfært fyrir reikninga í verkflæði.

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu móttekins magns úr völdum innhreyfingarskjal afurða. Ef bæði **Reikningsafgangur** magnið og **Eftirstöðvar afhendingar** fyrir allar og vörur á innkaupapöntun jafngildir núlli (0), breytist staða innkaupapöntunar í **Reikningsfært**. Ef magn **Reikningsafgangs** er ekki 0, er staða sölupöntunar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.

Þetta ferli gerir ráð fyrir að minnsta kosti eitt innhreyfingarskjal afurða hafi verið bókað fyrir innkaupapöntunina. Reikningur lánardrottisins er byggður á viðkomandi innhreyfingarskjali afurða og endurspeglar magnið á þeim. Fjárhagslegar upplýsingar sem koma fram á reikningnum eru byggðar á upplýsingunum sem færðar eru inn þegar reikningurinn er bókaður.

Frekari upplýsingar, sjá [Skrá reikning lánardrottins og bera saman við móttekið magn](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Stilltu sjálfvirkt verk fyrir verkflæði reikninga lánardrottins til að bóka reikning lánardrottins með runuvinnslu

Þú getur bætt sjálfvirku bókunarverki við verkflæði fyrir reikninga lánardrottins svo að reikningar séu unnir í runu. Með því að setja inn reikninga í runu getur verkflæðisferlið haldið áfram án þess að þurfa að bíða eftir að bókuninni ljúki, sem bætir árangur allra verka sem eru send inn í verkflæðið.

Til að bóka reikning lánardrottins í runu skal á síðunni **Eiginleikastjórnun** kveikja á færibreytunni **Runubókun reiknings lánardrottins**. Verkflæði fyrir lánardrottna eru stillt með því að fara í **Viðskiptaskuldir > Uppsetning > Verkflæði viðskiptaskulda**.

Þú getur séð verkið **Bóka reikning lánardrottins með runu** í verkflæðiritlinum, óháð því hvort færibreytan **Runubókun reiknings lánardrottins** sé virk. Þegar færibreytan er ekki virk mun reikningur sem inniheldur **Bóka reikning lánardrottins með runuverki** ekki vera unninn í verkflæði fyrr en breytan er virk. Verkið **Bóka reikning lánardrottins með runu** má ekki vera notaður í sama verkflæði og sjálfvirka verkið **Bóka reikninga lánardrottins**. Einnig ætti verkið **Bóka reikning lánardrottins með runu** ætti að vera síðasti þátturinn í verkflæðisstillingunni.

Þú getur tilgreint fjölda reikninga sem á að taka með í rununa og fjölda klukkustunda sem á að bíða áður en runa er enduráætluð með því að fara í **Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda > Reikningur > Verkflæði reikninga**. 

## <a name="working-with-multiple-invoices"></a>Vinna með marga reikninga

Hægt er að vinna með marga reikninga á sama tíma og bóka þá alla samtímis. Ef stofna þarf marga reikninga skal nota síðuna **Reikningar frá lánardrottni í bið**. Ef þarf að bóka og prenta marga reikninga lánardrottna skal nota færslubókarsamþykkt reiknings. Ef þú ert að nota samþykktarbók reikninga, þarf að minnsta kosti eitt innhreyfingarskjal afurða hafi verið bókað fyrir innkaupapöntunina og að reikningur fyrir innkaupapöntunina þarf að hafa verið bókaður í komubók. Fjárhagsupplýsingarnar fyrir reikninginn koma úr reikningnum sem var bókaður í komubókina.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Endurheimta reikninga lánardrottna sem eru notaðir

Þó að reikningur lánardrottins sé notaður getur annar notandi ekki breytt honum. Hins vegar getur staða á reikningi stundum gefið til kynna að verið sé að nota reikninga, jafnvel þótt ekki sé verið að breyta honum. Til dæmis gæti forritið hafa hætt að svara á meðan reikningnum var breytt eða notandi kann að hafa óvart skilið reikninginn eftir opinn í forritinu.

Hægt er að nota síðuna **Endurheimta reikninga lánardrottna** til að endurheimta eða losa reikninga lánardrottins sem hafa veirð í notkun í meira en fjórar klukkustundir, svo hægt sé að breyta þeim. Hægt er að opna þessa síðu af síðunni **Reglubundið verk** eða reit á vinnusvæðinu **Reikningsfærsla lánardrottins**. Eftir að reikningur er endurheimtur verður hægt að breyta honum á síðunni **Reikningur lánardrottins**.

Aðeins er hægt að fá aðgang að síðunni **Endurheimta reikninga lánardrottna** ef þér er úthlutað öryggisskyldunum og réttindunum **Endurheimta reikninga lánardrottna sem eru í notkun**. Auk þess þarf að kveikja á færibreytunni **Leyfa endurheimt á reikningum lánardrottna** á síðunni **Færibreytur viðskiptaskulda**.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Endurstilling á stöðu verkflæðis fyrir reikninga lánardrottins úr óendurkræf í drög

Verkflæðistilvik sem hefur stöðvast út af óendurkræfri villu verður með stöðu verkflæðis sem **Óendurkræft**. Þegar staðan á verkflæði fyrir reikning lánardrottins er **Óendurkræf** er hægt að endurstilla hana á **Drög** með því að velja **Afturkalla**. Síðan er hægt að breyta reikningi lánardrottins. Þessi eiginleiki er í boði ef kveikt er á færibreytunni **Endurstilling á stöðu verkflæðis fyrir reikninga lánardrottins úr óendurkræf í drög** á síðunni **Eiginleikastjórnun**.

Hægt er að nota síðuna **Sama verkflæðis** til að endurstilla verkflæðisstöðuna sem **Drög**. Þú getur opnað þessa síðu úr **Reikningur lánardrottins** eða úr **Algengar > Fyrirspurnir > Verkflæði** siglingar. Til að núllstilla stöðu flæðis á **Drög**, veldu **afturkalla**. Þú getur einnig endurstillt stöðu flæðis á Drög með því að velja **Afturkalla** aðgerð á **Reikningur lánardrottins** eða **Bíður reikninga lánardrottins** síðu. Eftir að verkflæðisstaðan hefur verið endurstillt í **Drög** verður hún opin fyrir breytingar á síðunni **Reikningur lánardrottnins**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Skoðun heildarupphæðar reiknings á síðunni „Reikningar frá lánardrottni í bið“
Hægt er að skoða heildarupphæð reiknings á síðunni **Reikningar frá lánardrottni í bið** með því að virkja færibreytuna **Birta heildarupphæð reiknings á reikningslista lánardrottins í bið** á síðunni **Færibreytur viðskiptaskulda**. 



## <a name="additional-resources"></a>Frekari upplýsingar

- [Setja upp reikningsreglur lánardrottins](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Lykilgögn reiknings í AP kerfið með því að nota reikning lánardrottins](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Færa reikningsgögn inn í viðskiptaskuldir með færslubókarsamþykkt](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Skrá reikning lánardrottins í reikningabók](tasks/record-vendor-invoice-invoice-journal.md)
