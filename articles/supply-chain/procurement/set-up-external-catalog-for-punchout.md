---
title: Setja upp ytri vörulista fyrir PunchOut e-procurement
description: Í þessu efnisatriði er lýst notkun á ytri vörulista eða PunchOut-vörulista til að safna upplýsingum um tilboð frá lánardrottni og bæta þeim við beiðni.
author: kamaybac
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9267047b4bf1ab4185efca9980e0f517f4b05096
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812521"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>Setja upp ytri vörulista fyrir PunchOut e-procurement

[!include [banner](../includes/banner.md)]

Með því að nota ytri vörulista er hægt að tryggja að upplýsingar um vöru og verð sem er síðan unnið úr í Supply Chain Management eru nákvæmar og uppfærðar. Beiðnin getur þá verið samþykkt og umbreytt í sölupöntun og pöntun geta verið staðsettir á lánardrottni.

Þegar ytri vörulista er að setja upp og starfsmaður undirbúning beiðni verða valkost til að beina fastakostnaði ytra setur, ytri vörulista og fara aftur í innkaupakörfu sína sem var búin til á ytra setur. Þessu samskiptaaðferðar byggist á samskiptareglur cXML og það hefur á að vera uppsett á milli kerfanna af sem kaupa og fyrirtæki seljanda.

Til að setja upp samskiptin þarf lánardrottinn að veita þér upplýsingar sem þú notar í skilgreiningu á vörulistanum, t.d. auðkenni, fyrirtækislén kaupanda, t.d. „DUNS“ eða „DUNS-númer“, innskráningarupplýsingar og vefslóðina til að komast á vörulista lánardrottna.

## <a name="setting-up-an-external-catalog"></a>Setja upp ytri vörulista

Ytri vörulista ætti að gera starfsmanns sem fer á innkaupabeiðni til að vera leyfður á ytra setur til að velja vörur. Vörunum sem starfsmaðurinn velur úr ytri vörulista er skilað með uppfærðum upplýsingum um verð og héðan er hægt bæta þeim við innkaupabeiðnina. Spurningarmerki sem á að leyfa starfsmönnum að leggja inn pöntun á ytra setur. Þegar uppsetningu ytri vörulista þarf að ganga úr skugga um að tilgangur sem aðgangur hlýst að með ytri vörulista er safnað tilboðsbeiðni en ekki raunverulegum pöntun.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Til að setja upp lista með ytri lánardrottni skal ljúka eftirfarandi verkum:

1. Setja upp tegundastigveldi innkaupa Sjá [Uppsetningarstefnur fyrir stigveldi innkaupaflokkunar](tasks/set-up-policies-procurement-category-hierarchies.md) fyrir frekari upplýsingar um hvernig setja á upp stigveldi innkaupategundar.
2. Skráðu lánardrottinn í Supply Chain Management. Áður en hægt er að setja upp skilgreiningu til að fá aðgang að ytri vörulista lánardrottins, verður að setja lánardrottin upp og tengilið lánardrottins í Microsoft Dynamics 365. Einnig þarf að bæta ytri vörulista lánardrottins við valda innkaupategund. Nánari upplýsingar um hvernig á að skrá lánardrottna er að finna í [Stjórna notendum fyrir samstarf lánardrottna](manage-vendor-collaboration-users.md). Sjá upplýsingar um hvernig á að úthluta á innkaupaflokknum lánardrottins [Samþykkja lánardrottnar fyrir tiltekið innkaupaflokkana](tasks/approve-vendors-specific-procurement-categories.md).
3. Gangið úr skugga um að eininga mælieiningin og gjaldmiðilinn sem lánardrottinn notar eru settir. Til að fá upplýsingar hvernig eigi að stofna mælieiningu, sjá [Stjórnun mælieiningar](../pim/tasks/manage-unit-measure.md).
4. Skilgreinið ytri vörulista lánardrottins með því að nota kröfurnar fyrir ytra vörulistasvæði lánardrottins. Frekari upplýsingar um þetta verk er að finna í [Grunnstilla ytri vörulista lánardrottins](#configure-the-external-vendor-catalog).
5. Prófið ytri vörulista lánardrottins til að staðfesta að stillingarnar séu gildar og að hægt sé að fá aðgang að ytri vörulista lánardrottins. Notið aðgerðina **Villuleita stillingar** til að villuleita skilaboð um beiðni um uppsetningu sem hefur verið skilgreind. Þessi skilaboð ættu að valda því að ytra vörulistasvæði lánardrottna verði opnað í vafraglugga. Við villuleit er ekki hægt að panta vörur og þjónustur frá lánardrottni. Til að panta vörur og þjónustu verður þú að fá aðgang að vörulista lánardrottins úr innkaupabeiðni.
6. Virkjaðu ytri vörulista með því að nota hnappinn **Virkja vörulista** á síðunni **Ytri vörulistar**. Virkja verður ytri vörulista áður en starfsmenn geta notað hann. Hægt er að gera ytri vörulista hvenær sem er.


## <a name="configure-the-external-vendor-catalog"></a>Grunnstilling ytri vörulista lánardrottins

Þessi hluti veitir frekari upplýsingar um verkefni 4 í undanfarandi hluta.

1. Heiti og lýsing eru færð inn fyrir ytri vörulista lánardrottins. Nafnið sem er fært inn mun birtast á körfu sem stendur fyrir ytri vörulista sem sýndur er á milli starfsmanna sem stofnar beiðni. Starfsfólk getur smellt á körfuna til að opna vörulistann á svæði ytri vörulista lánardrottins.
2. Bættu við mynd með því að nota aðgerðina **Mynd í ytri vörulista**. Myndin birtast körfu sem stendur fyrir ytri vörulista sem eru sýndar til starfsmanna sem búa til innkaupabeiðni. Athugið að breidd og hæð myndarinnar verður að vera jöfn. Annars birtist myndin ekki rétt.
3. Veldu hvort vefsvæði ytri vörulista lánardrottins eigi að birtast í sama vafraglugga og þar sem starfsmaður bjó til beiðnina, eða opnast í nýjum glugga.
4. Veldu lánardrottinn fyrir vörulistann. Í því **lögaðila** er engin línu fyrir hverja lögaðili sem lánardrottininn verið settur upp. Til að leyfa notendum að biðja um vörur beint frá vörulista lánardrottins í sumum lögaðilum en ekki öðrum, geturðu notað hnappinn **Hindra aðgang** eða **Leyfa aðgang** fyrir hvern lögaðila þar sem þú vilt að vörulistinn verði annaðhvort í boði eða ekki.
5. Í því **Sjálfgefin gildistíma (Dagar)** skal slá inn fjölda daga sem tilboð frá ytri vörulista gildir og hægt er að nota til að kaupa frá ytri lánardrottni. Þegar tilboð er stofnað og sótt úr svæði ytri vörulista lánardrottinsins, er tilboðið gilt frá og með núverandi kerfisdagsetningu, og er gild fyrir þann fjölda daga sem er færður inn í þetta svæði.
6. Smellið á **Bæta** hnappinn til að hefja innkaupaflokkana vörpun á ytri vörulistann. Síðan skal velja flokk í lista yfir flokksheiti. Lista yfir tegundir er tákna innkaupaflokkana sem lánardrottinn hefur verið varpað í öllum lögaðila sem eru settir fyrir lánardrottinn.

    > [!NOTE]
    > Innkaup reglur eru notaðar til að leyfa eða takmarka aðgang við kaupa lögaðili eða móttöku rekstrarfærslna einingu. Útskráning úr ytri vörulista krefst þess að aðgangur sé leyfður fyrir að minnsta kosti einn af innkaupaflokkunum sem eru varpaðir í vörulistann.

7. Setja upp cXML uppsetningu beiðni skilaboðin sem er sendur lánardrottni. Skilaboðasniðið myndaðar eru um sniðmát sem eru nauðsynlegar til að hefja svarsetu. Fylla verður í gildi fyrir seðlana í.

Endurhlaða má kerfismynduðu sniðmáti skilaboða hvenær sem er með því að smella á **Endurheimta sniðmát skilaboða**. Athugaðu að ef þú endurheimtir sniðmát skilaboða verður núverandi skilaboðum skipt út fyrir sjálfvirka myndun á sniðmáti skilaboða, sem hefur tóm merki.

### <a name="cxml-setup-message"></a>Uppsetning cXML skilaboð
Hér að neðan er hægt að finna lýsingu á merki sem eru hafðar með í sniðmátinu:

| Svæði | lýsing | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Fyrirtækislén kaupandans.|
|< Header >< From >< Credential>< Identity >< /Identity > | Fyrirtækiskenni kaupandans.|
|< Header >< To >< Credential domain=”” > | Fyrirtækislén lánardrottins.|
|< Header >< To >< Credential>< Identity >< /Identity> | Fyrirtækiskenni lánardrottins.|
|< Header >< Sender >< Credential domain=”” > | Fyrirtækislén kaupandans.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Fyrirtækiskenni kaupandans.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Samnýttur leynilykill fyrir fyrirtæki kaupandans.|
|< Request deploymentMode=”” >|Í prófunar- eða nets.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Vefslóð PunchOut-endastöðvar lánardrottins.|

### <a name="extrinsic-elements"></a>Extrinsic einingar

Extrinsic þáttur eru viðbótarupplýsingar á borð við notandanafn sem byggja á notandanum sem stimplar sig út. Extrinsic þáttur er stilltur þegar stimplað er út og hægt er að senda það í skilaboðum með beiðni um uppsetningu.
Lánadrottninum gæti verið þarfir fyrir móttöku extrinsic einingu í uppsetningu. Í því tilfelli ættir þú að bæta við extrinsic-einingu í listann yfir extrinsic-einingar í hlutanum **Sniðmát skilaboða** á síðunni **Ytri vörulisti**.
Tilgreinið nafn extrinsic einingarinnar sem lánardrottinn getur þekkja og tengið það gildi. Valkostir gildi eru: notandanafn, tölvupósts Notanda eða Random gildi.
Fyrir nánari upplýsingar um cXML-samskiptareglur skal sjá [cXML.org vefsvæðið](http://cxml.org/).

## <a name="post-back-message"></a>Skilaboð aftur
Skilaboð til baka eru skilaboðin sem fengin eru frá lánardrottni þegar notandi skráir sig út úr ytra svæði og fer aftur í Supply Chain Management. Ekki er hægt að stilla skilaboð til baka. Skilaboðin eru byggð á skilgreiningu á cXML samskiptareglunni. Hér eru þær upplýsingar sem geta verið hluti af skilaboðum til baka sem eru móttekin á innkaupabeiðnilínu:

| Skilaboðin sem berast frá lánardrottni | Afritað í beiðnilínu|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Magn|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Kenni ytra atriðis|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Gjaldmiðill|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Einingarverð|
|< ItemDetail >< Description ShortName=”” >|Afurðarnafn|
|< ItemDetail >< Description >< /Description >|Í vörulýsing; Heiti vöru ef ShortName er ekki tilgreindur.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Eining|
|< ItemDetail >< Classification >< /Classification >|Í vörulýsingu|
|< ItemDetail >< Classification domain=”” >|Í vörulýsingu|

## <a name="delete-an-external-catalog"></a>Eyða ytri vörulista
Ytri vörulista með Eyða aðgerðin á að eyða.

Ef vöru úr vörulista ytri lánardrottinn hefur verið beðið um, ekki er hægt að eyða vörulista ytri lánardrottni. Þess í stað stöðu vörulista ytri lánardrottni fest óvirk. Ef ætlunin er að fjarlægja aðgang að vörulistasvæði ytri lánardrottins en ekki eyða því, skal breyta stöðu ytri vörulista í óvirkt.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Viðbætur cXML-innkaupa](purchasing-cxml-enhancements.md)
- [Nota ytri vörulista fyrir PunchOut e-procurement](use-external-catalogs-for-punchout.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]