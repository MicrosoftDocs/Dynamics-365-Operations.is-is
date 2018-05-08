---
title: "Setja upp ytri vörulista fyrir PunchOut eProcurement"
description: "Þetta efnisatriði lýsir notkun ytri vörulista eða punchout vörulista til að safna tilboðsbeiðni upplýsingar frá lánardrottni og bæta við innkaupabeiðnina."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2892feff0ab8845515543af1a71d8f9642113726
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Setja upp ytri vörulista fyrir PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Með því að nota ytri vörulista er hægt að tryggja að upplýsingar um vöru og verð sem er síðan unnið úr í Dynamics 365 for Finance and Operations, júlí 2017, eru nákvæmar og uppfærðar. Beiðnin getur þá verið samþykkt og umbreytt í sölupöntun og pöntun geta verið staðsettir á lánardrottni.

Þegar ytri vörulista er að setja upp og starfsmaður undirbúning beiðni verða valkost til að beina fastakostnaði ytra setur, ytri vörulista og fara aftur í innkaupakörfu sína sem var búin til á ytra setur. Þessu samskiptaaðferðar byggist á samskiptareglur cXML og það hefur á að vera uppsett á milli kerfanna af sem kaupa og fyrirtæki seljanda.

Til að setja upp samskiptum lánardrottninum verður að veita stykki upplýsinga til að nota í configuraiton af vörulistanum ytri Kenni léns fyrirtækisins dreifingu, t.d. "DUNS" og "DUNS númer", eins og notendaheimildir og Vefslóð til að ná lánardrottna vörulista.

## <a name="setting-up-an-external-catalog"></a>Setja upp ytri vörulista

Ytri vörulista ætti að gera starfsmanns sem fer á innkaupabeiðni til að vera leyfður á ytra setur til að velja vörur. Vörur sem starfsmaðurinn velur ytri vörulista er skilað í Dynamics 365 til Fjármála og Aðgerðir inn verðupplýsingar og héðan er þeim er bætt við innkaupabeiðnina. Spurningarmerki sem á að leyfa starfsmönnum að leggja inn pöntun á ytra setur. Þegar uppsetningu ytri vörulista þarf að ganga úr skugga um að tilgangur sem aðgangur hlýst að með ytri vörulista er safnað tilboðsbeiðni en ekki raunverulegum pöntun.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Til að setja upp lista með ytri lánardrottni skal ljúka eftirfarandi verkum:

1. Setja upp tegundastigveldi innkaupa Sjá [Uppsetningarstefnur fyrir stigveldi innkaupaflokkunar](tasks/set-up-policies-procurement-category-hierarchies.md) fyrir frekari upplýsingar um hvernig setja á upp stigveldi innkaupategundar.
2. Skrá lánardrottins Fjármál og Aðgerða. Áður en hægt er að setja upp skilgreingu til að fara í ytri vörulista lánardrottins, verður að setja lánardrottininn upp og tengiliði lánardrottna í Microsoft Dynamics 365. Lánardrottni ytri vörulista verður einnig að vera bætt við valda innkaupategund. Nánari upplýsingar um skráningu lánardrottna í Microsoft Dynamics 365 [Stjórna lánardrottins efnisumsjón notendur](manage-vendor-collaboration-users.md). Sjá upplýsingar um hvernig á að úthluta á innkaupaflokknum lánardrottins [Samþykkja lánardrottnar fyrir tiltekið innkaupaflokkana](tasks/approve-vendors-specific-procurement-categories.md).
3. Gangið úr skugga um að eininga mælieiningin og gjaldmiðilinn sem lánardrottinn notar eru settir. Til að fá upplýsingar hvernig eigi að stofna mælieiningu, sjá [Stjórnun mælieininga](../pim/tasks/manage-unit-measure.md).
4. Skilgreinið vörulista ytri lánardrottni þarfir fyrir ytri vörulista setur við lánardrottinn. Frekari upplýsingar um þetta verk er að finna í [Grunnstilla ytri vörulista lánardrottins](#configure-the-external-vendor-catalog).
5. Prófa málskipan lánardrottins ytri vörulista afbrigði til að staðfesta stillingar séu gildar og sem hægt er að nálgast ytri vörulista lánardrottins. Notkun á **Villuleita stillingar** aðgerð til að villuleita beiðni uppsetningu skilaboð sem hefur verið skilgreint. Þessi skilaboð eigi valdið lánardrottna ytri vörulista svæði til að opna vefvafra glugga. Við villuleit, ekki er hægt að panta vörur og þjónustu frá lánardrottni. Til að panta vörur og þjónustu, er verður að nálgast lánardrottins vörulista við innkaupabeiðnina.
6. Virkja ytri vörulistanum með því að nota í **Virkja vörulista** hnappinn á á **Ytri vörulistar** síðu. Virkja þarf ytri vörulista áður en starfsmenn geta notað það. Hægt er að gera ytri vörulista hvenær sem er.


## <a name="configure-the-external-vendor-catalog"></a>Grunnstilling ytri vörulista lánardrottins

Þessi hluti veitir frekari upplýsingar um verkefni 4 í undanfarandi hluta.

1. Heiti og lýsing eru færð inn fyrir ytri vörulista lánardrottins. Nafnið sem er fært inn mun birtast á körfu sem stendur fyrir ytri vörulista sem sýndur er á milli starfsmanna sem stofnar beiðni. Starfsmenn geta smellið á körfu til að opna vörulista lánardrottins ytri vörulista staðsetningu.
2. Bætið við myndskrá með því að nota í **Ytri vörulista mynd** aðgerðar. Myndin birtast körfu sem stendur fyrir ytri vörulista sem eru sýndar til starfsmanna sem búa til innkaupabeiðni. Athugið að breidd og hæð í mynd verður að vera jafnar. Annars myndarinnar won't birtist ekki rétt.
3. Veljið hvort lánardrottins ytri vörulista vefsvæði eiga að birtast á sama vafra glugga og þar sem starfsmaðurinn hefur stofnað fyrir innkaupabeiðni, eða ef það á að opna í nýjum glugga.
4. Veldu lánardrottinn fyrir vörulistann. Í því **lögaðila** er engin línu fyrir hverja lögaðili sem lánardrottininn verið settur upp. Til að gera notendum kleift að biðja um vörum úr vörulista lánardrottins í sumum lögaðila en ekki önnur, er hægt að nota í **Hindra aðgang** eða **Leyfa aðgang** fyrir hverja lögaðili á vörulista sem eða ekki að vera til staðar.
5. Í því **Sjálfgefin gildistíma (Dagar)** skal slá inn fjölda daga sem tilboð frá ytri vörulista gildir og hægt er að nota til að kaupa frá ytri lánardrottni. Þegar tilboð er stofnað og sótt úr svæði ytri vörulista lánardrottinsins, er tilboðið gilt frá og með núverandi kerfisdagsetningu, og er gild fyrir fjölda daga sem eru færðir inn í þetta svæði.
6. Smellið á **Bæta** hnappinn til að hefja innkaupaflokkana vörpun á ytri vörulistann. Síðan, í listanum Heiti flokks, skal velja flokk. Lista yfir tegundir er tákna innkaupaflokkana sem lánardrottinn hefur verið varpað í öllum lögaðila sem eru settir fyrir lánardrottinn.
[!NOTE]
Innkaup reglur eru notaðar til að leyfa eða takmarka aðgang við kaupa lögaðili eða móttöku rekstrarfærslna einingu. Punchout við ytri vörulista þarfnast aðgangi að leyfilegt að minnsta kosti einn innkaupaflokkana sem er varpað á vörulista.
7. Setja upp cXML uppsetningu beiðni skilaboðin sem er sendur lánardrottni. Skilaboðasniðið myndaðar eru um sniðmát sem eru nauðsynlegar til að hefja svarsetu. Fylla verður í gildi fyrir seðlana í.

Hvenær sem er hægt er að sækja aftur sniðmátið kerfið hefur myndað birtast með því að smella á **skilaboðasniðið Endurheimta**. Athugið að ef skilaboðasniðið, endurheimta gildandi skilaboð skipt sjálfvirkum skilaboðasniðið sem hefur autt merki.

### <a name="cxml-setup-message"></a>Uppsetning cXML skilaboð
Hér að neðan er hægt að finna lýsingu á merki sem eru hafðar með í sniðmátinu:

| Svæði | lýsing | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Umdæmi í dreifing fyrirtækisins.|
|< Header >< From >< Credential>< Identity >< /Identity > | Kenni fyrirtækisins í dreifingu.|
|< Header >< To >< Credential domain=”” > | Umdæmi lánardrottins í fyrirtækinu.|
|< Header >< To >< Credential>< Identity >< /Identity> | Kenni fyrirtækisins lánardrottins.|
|< Header >< Sender >< Credential domain=”” > | Umdæmi í dreifing fyrirtækisins.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Kenni fyrirtækisins í dreifingu.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Samnýttu secret á dreifing fyrirtækisins.|
|< Beiðni deploymentMode = "" >|Í prófunar- eða nets.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Veffang lánardrottins punchout endastöð.|

### <a name="extrinsic-elements"></a>Extrinsic einingar

Extrinsic þáttur eru viðbótarupplýsingar á borð við notandanafn sem byggja á notandanum sem stimplar sig út. Extrinsic þáttur er stilltur þegar stimplað er út og hægt er að senda það í skilaboðum með beiðni um uppsetningu.
Lánadrottninum gæti verið þarfir fyrir móttöku extrinsic einingu í uppsetningu. Í því tilfelli er eigi við extrinsic einingar yfir extrinsic einingar í í **skilaboðasniðið** hluta í **Ytri vörulista** síðu. Tilgreinið nafn extrinsic einingarinnar sem lánardrottinn getur þekkja og tengið það gildi. Valkostir gildi eru: notandanafn, tölvupósts Notanda eða Random gildi.
Fyrir nánari upplýsingar um cXML samskiptareglur skal sjá: http://cxml.org/

## <a name="post-back-message"></a>Skilaboð aftur
Bóka skilaboðin aftur er skilaboðin sem berast frá lánardrottni gengur úr ytri svæði og til Fjármála og Aðgerðir. Bóka aftur skilaboð ekki er hægt að skilgreina. Fyrir skilaboð er byggður á skilgreiningunni cXML samskiptareglur. Hér eru upplýsingar sem hluta af bóka aftur skilaboðin sem er móttekið á línu innkaupabeiðninnar:

| Skilaboðin sem berast frá lánardrottni | Afrita línu Fjármál og Aðgerðir|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Magn|
|< ItemIn >< ItemID >< SupplierPartID >< /SupplierPartID >|Kenni ytra atriðis|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Gjaldmiðill|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Einingarverð|
|< ItemDetail >< Description ShortName=”” >|Afurðarnafn|
|< ItemDetail >< Description >< /Description >|Í vörulýsing; Heiti vöru ef ShortName er ekki tilgreindur.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Eining|
|< ItemDetail >< Classification >< /Classification >|Í vörulýsingu|
|< ItemDetail >< Classification domain=”” >|Í vörulýsingu|

## <a name="delete-an-external-catalog"></a>Eyða ytri vörulista
Ytri vörulista með Eyða aðgerðin á að eyða.

Ef vöru úr vörulista ytri lánardrottinn hefur verið beðið um, ekki er hægt að eyða vörulista ytri lánardrottni. Þess í stað stöðu vörulista ytri lánardrottni fest óvirk. Ef þú vilt fjarlægja aðgang að setrinu vörulista ytri lánardrottni en ekki að eyða henni, breyta stöðu ytri vörulista Inactive.


