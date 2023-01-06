---
title: Sjálfvirkni reiknings fyrir skönnuð skjöl
description: Í þessari grein er fjallað um aðgerðir sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, jafnvel reikninga með viðhengi.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0449a13989bad45cf0456a2678e5724036d2af3d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070695"
---
# <a name="invoice-automation-for-scanned-documents"></a>Sjálfvirkni reiknings fyrir skönnuð skjöl

[!include [banner](../includes/banner.md)]

Í þessari grein er fjallað um gagnaeiningar sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, þar með talið reikninga með viðhengi.

Fyrirtæki sem vilja hagræða ferlum Viðskiptaskulda (AP) auðkenna oft reikningsvinnslur sem ein af aðalferlunum sem þurfa að vera skilvirkari. Í mörgum tilvikum láta þessi fyrirtæki ótengdan þjónustuaðila með ljósskynjun stafa (OCR) um vinnslu reikninga á pappír. Þeir fá síðan tölvulesanleganleg lýsigögn reiknings ásamt skannaðri mynd af hverjum reikningi. Til að aðstoða við sjálfvirkni er "síðasta kílómetra" lausn síðan myndað til að auðvelda notkun á þessum hlutum í reikningsfærslukerfinu. Núna er þessi „síðustu metrunum“ sjálfvirkni virkjuð beint úr kassanum með því að nota lausn sjálfvirkra reikninga.

## <a name="solution-context"></a>Lausnasamhengi

Reikningur sjálfvirkni lausn virkjar staðlað viðmót sem getur samþykkt reiknings lýsigögn á reikningshausinn og reikningslínur og viðhengjum sem á við um reikninginn. Öll utanaðkomandi kerfi, sem getur myndað gervinga sem samræmast þessu viðmóti munu geta sent færslurnar inn til sjálfvirkrar vinnslu á reikningum og viðhengjum.

Eftirfarandi skýringarmynd sýnir sýnishorn af samþættingaraðstæðum þar sem Contoso hefur gerst meðeigandi með OCR-þjónustuveitanda fyrir vinnslu á reikningi lánardrottins. Lánardrottnar Contoso senda reikninga til þjónustuveitu með tölvupósti. Í gegnum OCR-vinnslu myndar þjónustuveitan lýsigögn reikningsins (haus og/eða línur) og skannaða mynd af reikningnum. Samþættingarlag umbreytir þessum gervingum síðan svo að hægt sé að geta nota þær.

![Dæmi um samþættingaraðstæður.](media/vendor_invoice_automation_01.png)

Nokkur tilbrigði með fyrrgreint dæmi eru mögulegur ef samþætting reiknings er nauðsynleg. Gagnaflutningur er dæmi um aðra notkun þar sem hægt er að nota þetta viðmót til að stofna reikninga og viðhengi.

### <a name="solution-components"></a>Lausnaíhlutir

Lausnafótsporið samanstendur af eftirfarandi þáttum:

+ Gagnaeiningar fyrir reikningshausinn, línur á reikningi og reikningsviðhengi
+ Undantekningavinnsla fyrir reikninga
+ Hlið-við-hlið viðhengjabirtir í reikningum

Afgangurinn af þessari grein gefur ítarlegar lýsingar á þessum lausnaþáttum.

## <a name="data-entities"></a>Gagnaeiningar

Gagnapakki er sú vinnueining sem þarf að senda svo að hægt sé að stofna reikningshausa, reikningslínur og reikningsviðhengi. Eftirfarandi gagnaeiningar eru notaðar fyrir gervinga sem mynda gögn pakka:

+ Reikningshaus lánardrottins
+ Reikningslína lánardrottins
+ Viðhengi reikningsskjals lánardrottins

Skjalaviðhengi lánardrottnareikningsins er ný gagnaeining sem er kynnt sem hluti af þessari aðgerð. Hauseining lánardrottnareiknings hefur verið breytt þannig að hann styður viðhengi. Línueining lánardrottnareiknings hefur ekki verið breytt fyrir þetta sérkenni.

Ítarlegar upplýsingar um gagnapakka er að finna í [Yfirlit gagnastjórnunar](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Frekari upplýsingar um hvernig á að búa til gagnapakka með vinnusvæði gagnastjórnunar er að finna í [Meðhöndla og nota gagnapakka í Dynamics 365 forritslausn fyrir fjármál- og rekstur](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Fylgið eftirfarandi skrefum til að mynda prófun gagna sem inniheldur reikninga og viðhengja.

1. Skráðu þig inn á tilvikið.
1. Fara í **Viðskiptaskuldir** > **Reikningar** > **Opna lánardrottnareikninga**.
1. Stofna reikninga sem hafa línur og viðhengi.

    > [!NOTE]
    > Viðhengin verða að vera viðhengi við haus. Sem stendur styður skjalaviðhengjaeining lánardrottnareiknings ekki viðhengi við línur.

1. Opnaðu vinnusvæðið **Gagnastjórnun**.
1. Stofna útflutningsvinnslu sem inniheldur reikningshaus lánardrottins, reikningslínu lánardrottins og skjalaviðhengiseiningu lánardrottnareiknings.
1. Flyttu út gögnin.
1. Sæktu útflutt gögnin sem pakka. Nú má nota pakkanum til að flytja gögn inn í marktilvik til prófunar.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Ákvörðun lögaðila fyrir reikning

Reikningar sem eru innfluttir með gagnapakka er hægt að tengja lögaðila sem þeir tilheyra á tvo vegu:

+ Innflutningsvinnslan sem vinnur reikninginn flytur hann inn í sama fyrirtækið sem þar vinnslan var í röðun á vinnusvæðinu **Gagnastjórnun**. Með öðrum orðum ákvarðar fyrirtæki vinnslunnar fyrirtækið sem reikningurinn tilheyrir.
+ Þegar gagnapakki sem inniheldur reikninga er sendur til Finance, getur hringjandi (þ.e.a.s. samþættingarforritið sem keyrir utan Finance) nefnt kenni fyrirtækisins skýrt í HTTP-beiðninni. Í þessu tilfelli er fyrirtækjasamhenginu sem keyrir vinnsluna í Finance hnekkt og reikningarnir eru fluttir inn í fyrirtækið sem var beint í gegnum svar HTTP.

> [!NOTE]
> Þessi hegðun er stöðluð gagnastjórnunarhegðun. Það er útskýrt hér, í samhengi við reikninga, fyrir sakir heildarinnar.

## <a name="exception-processing"></a>Undantekningavinnsla

Í aðstæðum þar sem lánardrottinsreikningar koma inn í fjármál- og rekstur með samþættingu þarf að vera til staðar auðveld leið fyrir meðlimi viðskiptaskulda til að vinna úr undantekningum eða reikninga sem ekki eru samþykktir og stofna reikninga í bið út frá reikningum sem mistókst. Þessi frábrigðavinnsla fyrir reikninga lánardrottins er nú hluti af fjármálum- og rekstri.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Listasíða reikninga lánardrottna sem ekki tókst að flytja inn

Nýja listasíðan fyrir reikningsundantekningar er alltaf tiltæk í **Viðskiptaskuldum** > **Reikningum** > **Flytja verkefnismistök** > **reikningar Lánardrottins sem hefur mistekist að flytja**. Þessi síða sýnir allar hausfærslur lánardrottnareiknings úr sviðsetningartöflunni í gagnaeiningu hauss lánardrottnareiknings. Athugið að hægt er að skoða sömu skrár á vinnusvæðinu **Gagnastjórnun**. Hægt að framkvæma sömu aðgerðir sem eru gefnar í undantekningunni meðhöndlun aðgerð af vinnusvæðinu **Gagnastjórnun**. Eiginleiki meðhöndlunar undantekninga hefur verið fínstillt fyrir virkan notanda sem auðveldar notkun hans.

![Listasíða undantekninga.](media/vendor_invoice_automation_02.png)

Þessi listasíða felur í sér eftirtalin svæði sem berast inn í gegnum streymi:

+ **Fyrirtæki** – Það fyrirtæki sem reikningurinn tilheyrir
+ **Villuboð** – Villuboðin sem ramminn stjórnun gagna úthreyfingar til að útskýra af hverju ekki var hægt að stofna reikning
+ **Númer** – Reikningsnúmer
+ **Reikningslykill**
+ **Nafn** – Nafn lánardrottins
+ **Lykill lánardrottins**
+ **Innkaupapöntun** – Númer innkaupapöntunar fyrir reikninginn
+ **Bókunardagsetning**
+ **Reikningsdagsetning**
+ **Lýsing reiknings**
+ **Gjaldmiðill**
+ **Kladdi**
+ **Línutilvísun** – Kennið sem er fengið frá utanaðkomandi kerfi

    > [!NOTE]
    > Línutilvísun er ekki reikningskenni.

Þessi listasíða hefur einnig forskoðunarrúðu sem þú getur notað á eftirfarandi hátt:

+ Skoða öll villuboðin svo að ekki þurfi að útvíkka dálkinn **Villuboð** í hnitanetinu.

Listasíðan styður eftirfarandi aðgerðir:

+ **Breyta** – Opna undantekningarfærsluna í breytingarham, þannig að hægt sé að laga vandamálin.
+ **Valkostir** – Farðu í staðlaða valkostina sem eru tiltækir á listasíðunum. Hægt er að nota valkostinn **Bæta við vinnusvæði** til að festa listasíðu undantekninga á vinnusvæðið sem lista eða reit.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Upplýsingasíða reikninga lánardrottna sem ekki tókst að flytja inn

Þegar breytingastilling er ræst opnast upplýsingasíða **Reikningar lánardrottna sem ekki tókst að flytja inn** fyrir reikninginn sem er með vandamál. Ef vandamál koma upp með reikning sem er með viðhengi verður viðhengið ekki birt. Viðhengi verður að vera endurhengt við reikninginn.

**Reikningar lánardrottna sem ekki tókst að flytja inn** upplýsingasíðan gerir notanda kleift að stofna biðreikning. Þegar vandamál á reikningnum hafa verið löguð sem hluti af undantekningavinnslu, skal velja **Stofna reikning í bið** til að stofna reikning í bið. Biðreikningurinn verður búinn til í bakgrunni. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Samnýtt þjónusta samanb. v. fyrirtækjabyggða undantekningavinnslu

Listasíða undantekninga styður staðlaða öryggisbyggingu sem vinnusvæðið **Gagnastjórnun** styður fyrir vinnslu á stigaðgerðir færslur. Hægt er að tryggja innflutningsvinnslu reiknings á eftirfarandi hátt:

+ Eftir notandahlutverki
+ Eftir notanda
+ Eftir lögaðila

![Innflutningsvinnsla sem er tryggð eftir hlutverki notanda og lögaðila.](media/vendor_invoice_automation_04.png)

Ef öryggi er skilgreint fyrir innflutningsvinnslu reiknings virðir listasíða undantekninga þessar stillingar. Notendur geta aðeins séð undantekningafærslur reikninga sem þessi uppsetning leyfir þeim að sjá.

Til dæmis hefur Contoso ákveðið að keyra reikningsundantekningar eftir lögaðilum. Þar af leiðandi er öryggi skilgreint í innflutningsvinnslu reikninga á þann hátt að notandi í lögaðila A getur aðeins séð undantekningar reikninga í lögaðila A, en notandi í lögaðila B getur aðeins séð undantekningar reikninga í lögaðila B. Þessi uppsetning virkjar aðskilnað á skyldum fyrir stjórnun á undantekningum reikninga.

Contoso gæti einnig ákveðið að tryggja ekki neitt öryggi, þannig að notendur geti keyrt undantekningar reikninga fyrir allar einingar lögaðila. Þessi uppsetning virkjar samnýtta þjónustuaðstæður fyrir stjórnun á undantekningum reikninga.

## <a name="side-by-side-attachment-viewer"></a>Hlið-við-hlið viðhengjabirtir

Til að aðstoða við að skoða viðhengi fyrir reikninga lánardrottins, veita eftirfarandi síður sem eru notaðar í reikningsfærslunni núna viðhengjabirti:

+ **Meðhöndlun undantekninga**
+ Síðan **Lánardrottnareikningar í bið** (einnig tiltæk i endurskoðunarferli reikninga)
+ Fyrirspurnasíða **Reikningabók** (fyrir bókaða reikninga)

Hér eru aðalaðgerðir sem viðhengjabirtirinn veitir:

+ Skoðið allar viðhengjagerðir sem skjalastjórnun styður (skrár myndir, Vefföng og athugasemdir).
+ Skoða TIFF-skrár með mörgum síðum.
+ Framkvæmið eftirfarandi aðgerðir í myndaskrám:
  + Merkið hluta myndarinnar.
  + Felur hluta myndarinnar.
  + Bæta athugasemdum við myndina.
  + Þysjar inn og út á myndina.
  + Víðmynd myndarinnar.
  + Afturkalla og endurgera aðgerðir.
  + Breyttu myndarinni svo að hún passi.

> [!NOTE]
> Þessar aðgerðir eru tiltækar fyrir myndskrár (JPEG, TIFF, PNG og svo framvegis). Allar breytingar sem gerðar eru á mynd með því að nota þessar aðgerðir eru vistaðar í myndskrá. Eins og stendur felur viðhengjabirtir ekki í sér útgáfu- eða endurskoðunargetu.

### <a name="default-attachment"></a>Sjálfgefið viðhengi

Ef reikningur lánardrottins hefur fleiri en eitt viðhengi er hægt að stilla eitt af skjölunum sem sjálfgefið viðhengi á síðunni **Viðhengi**. Valkosturinn **Er sjálfgefið viðhengi** er nýr valkostur sem var bætt við sem hluta af þessum aðgerðum. Þessi valkostur er líka sýndur í gagnaeiningu skjalaviðhengis lánardrottnareiknings. Þess vegna er hægt að stilla sjálfgefið viðhengi í gegnum samþættingar.

Aðeins er hægt að stilla eitt skjal sem sjálfgefið viðhengi. Eftir að skjal er stillt sem sjálfgefið viðhengi er það sjálfkrafa sýnt í viðhengjabirti þegar reikningurinn er opnaður. Ef ekkert skjal er stillt sem sjálfgefið viðhengi sýnir birtirinn ekki sjálfkrafa nein viðhengi þegar reikningurinn er opnaður.

### <a name="showhide-invoice-attachments"></a>Sýna/fela reikningsviðhengi

Ný hnappur sem er tiltækur á fyrirspurnasíðunum **Undantekningar vinnslu**, **Reikningur í bið** og **Reikningabók** gerir kleift að sýna eða fela viðhengjabirtinn.

## <a name="security"></a>Öryggi

Eftirfarandi aðgerðum í viðhengjabirti er stjórnað með öryggi eftir hlutverkum:

+ Auðkennt
+ Varið
+ Athugasemd

### <a name="pending-vendor-invoices-page"></a>Síðan Lánardrottnareikningar í bið

Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir:

+ **Viðhalda mynd lánardrottnareiknings** – Þessi réttindi veta les/skrif aðgang.
+ **Skoða mynd lánardrottnareiknings** – Þessi réttindi veta lesaðgang.

Eftirfarandi skyldur veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:

+ **Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda lánardrottnareikningi eru tengd þessum skyldum.
+ **Gera fyrirspurn um reikningsstöðu lánardrottins** – Myndaréttindin Skoða lánardrottnareikningi eru tengd þessum skyldum.

Eftirfarandi hlutverk veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:

+ **Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.
+ **Afgreiðslumaður lánardrottna**, **stjórnanda lánardrottna**, **Lykla lánardrottna miðstýrðar greiðslur afgreiðslumaður**, og **Lykla lánardrottna greiðslur afgreiðslumaður** – í Spyrjast fyrir um lánardrottinn reikningi stöðuna gjald er úthlutað á þessum hlutverkum.

### <a name="vendor-invoice-attachment"></a>Viðhengi reiknings lánardrottins

Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir.

> [!NOTE]
> Hlutverk sem eru nefnd í þessum hluta veita aðeins til lestrar aðgang að myndir reikning í viðhengjabirti utan í reitinn. Ef hlutverk verður einnig að hafa skrifaðgang að myndunum, má veita skrifaðgang að því hlutverki með heimildinni og gjald sem er lýst hér.

+ **Viðhalda lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les/skrif aðgang að reikningur myndirnar í viðhengjabirti.
+ **Skoða lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les aðgang að reikningsmyndinni í viðhengjabirti.

Eftirfarandi skyldur veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:

+ **Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda hauseiningu lánardrottnareiknings eru tengd þessum skyldum.

Eftirfarandi hlutverk veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:

+ **Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.

Sjálfgefið ef hlutverki notanda veitir breyta réttindi á öllum síðum notanda mun einnig hafa breyta heimildir í viðhengjabirti fyrir merkingar-, blokkunar- og athugasemdaaðgerðir. Hins vegar í tilvikum þar sem tiltekið hlutverk á að hafa breytingarheimildir á síðunni en ekki í viðhengjabirtinum er hægt að nota viðeigandi réttindi úr fyrrgreindum lista til að uppfylla notkunartilvik.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

