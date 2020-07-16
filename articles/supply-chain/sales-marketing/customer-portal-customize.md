---
title: Sérsníða og nota viðskiptavinagátt
description: Þetta efnisatriði útskýrir hvernig á að sérsníða viðskiptavinagátt þegar búið er að bæta henni við kerfið.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3ab79bc9203309c0cfa1ff18f75580297ae1001
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413976"
---
# <a name="customize-and-use-the-customer-portal"></a>Sérsníða og nota viðskiptavinagátt

Þetta efnisatriði lýsir mismunandi síðum sem eru í boði í tilbúinni viðskiptavinagátt. Það útskýrir hvað síðurnar gera og hvernig hægt er að sérstilla þær.

Viðskiptavinagáttin býður upp á nokkrar tilbúnar vefsíður og aðgerðir. Eftirfarandi veftré veitir yfirlit yfir þessar vefsíður og aðgerðir og hlutverkin sem geta framkvæmt aðgerðirnar.

![![Veftré viðskiptavinagáttar](media/customer-portal-site-map.png "Veftré viðskiptavinagáttar")](media/customer-portal-site-map.png "Customer portal site map")

## <a name="typical-customizations"></a>Dæmigerðar sérstillingar

Eftirfarandi efnisatriði munu hjálpa til við að læra grunnatriði varðandi Power Apps-gáttir og hvernig hægt er að sérsníða gáttir:

- [Vinna með sniðmát](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – Í þessu efnisatriði er boðið upp á almennt yfirlit um hvernig Power Apps-gáttar virka og hvernig hægt er að gera einfaldar sérstillingar á gáttum.
- [Stjórna efni gáttar](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – Þetta efnisatriði útskýrir hvernig hægt er að stjórna og sérsníða efnið sem er flett upp í gáttinni.
- [Breyta CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – Þetta efnisatriði hjálpar til við að gera flóknari sérsnið í notendaviðmóti gáttarinnar.
- [Stofna þema fyrir gáttina](https://docs.microsoft.com/dynamics365/portals/create-theme) – Þetta efnisatriði hjálpar til við að stofna þema notandaviðmóts fyrir gáttina þína.
- [Búa til og sýna efni gáttar á auðveldan hátt](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – Þetta efnisatriði hjálpar til við að stjórna undirliggjandi gögnum og einingum sem eru notaðar í gáttinni.
- [Skilgreina tengilið fyrir notkun á gátt](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – Þetta efnisatriði útskýrir hvernig á að búa til og sérsníða notandahlutverk og hvernig öryggi og sannvottun virka í Power Apps gáttum.
- [Skilgreina athugasemdir fyrir skjámyndir eininga og vefs í gáttum](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – Þetta efnisatriði útskýrir hvernig á að bæta skjölum og viðbótargeymslum við gáttina.
- [Villumeðhöndlun fyrir vefsvæði gáttar](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – Þetta efnisatriði útskýrir hvernig á að skoða villuskráningar gáttar og geyma þær í blob-geymslureikningi Microsoft Azure.

## <a name="customize-the-order-creation-process"></a>Sérsníða stofnferli pantana

Þegar notandi sendir inn pöntun með því að nota viðskiptavinagáttina er pöntunin sjálfkrafa samstillt við viðeigandi Dynamics 365 Supply Chain Management-umhverfi. Vegna þess að notandinn er ytri viðskiptavinur eru einhverjar nauðsynlegar upplýsingar faldar fyrir honum eða henni. Þessar upplýsingar verða sjálfkrafa fylltar út þegar skjámyndin er send inn.

Þessi hluti sýnir hvernig á að setja upp tengiliði til að komast hjá villum. Þar eru reitir útskýrðir sem eru sjálfkrafa stilltir og útskýrt hvernig hægt er að breyta gildi þessara reita ef þörf krefur.

### <a name="the-out-of-box-order-creation-process"></a>Tilbúið stofnferli pantana

Hér eru stöðluð skref til að senda inn pöntun úr viðskiptavinagátt.

1. Á heimasíðunni skal velja reitinn **Stofna pöntun** til að opna leiðsagnarforritið **Stofna pöntun**.
1. Á síðunni **Upplýsingar um pöntun** skal stilla eftirfarandi reiti:

    - **Umbeðin móttökudagsetning** – Tilgreinið dagsetningu afhendingar.
    - **Afhendingaraðsetur** – Færa skal inn aðsetrið sem senda á pöntunina til.
    - **Fyrirtækið** - Veljið heiti á fyrirtæki viðskiptavinar. Þetta reitur er sjálfkrafa stilltur fyrir notendur sem ekki eru stjórnendur.
    - **Númer beiðni** – Sláið inn beiðninúmer pöntunarinnar. Þessi reitur er ekki áskilinn.
    - **Senda til lands/svæðis** – Færið inn land eða svæði sem vörurnar verða sendar til. Þetta reitur er sjálfkrafa stilltur fyrir notendur sem ekki eru stjórnendur.

    ![![Pöntunarupplýsingasíða](media/customer-portal-order-information.png "Pöntunarupplýsingasíða")](media/customer-portal-order-information.png "Order Information page")

1. Veljið **Næst**.
1. Á síðunni **Vörur** skal velja **Bæta við vöru**.

    ![![Vörusíða](media/customer-portal-items.png "Vörusíða")](media/customer-portal-items.png "Items page")

1. Í svarglugganum **Upplýsingar um vöru** skal stilla eftirfarandi reiti:

    - **Afurðarheiti** – Finna og velja afurð til að bæta við pöntunina.
    - **Magn** - Færið inn magn valinnar afurðar.
    - **Eining** – Tilgreinið mælieininguna (til dæmis, **ea.**, **kg** eða **kassi**).
    - **Áætluð nettóupphæð** – Gildið er reiknað út sem áætlað verð vörunnar × magn fyrir valda einingu.

    ![![Upplýsingagluggi vöru](media/customer-portal-item-information.png "Upplýsingagluggi vöru")](media/customer-portal-item-information.png "Item Information dialog box")

1. Smellið á **Senda inn** til að bæta vöru við pöntun.
1. Endurtakið skref 4 til 6 þar til öllum vörum hefur verið bætt við pöntun.
1. Þegar búið er að bæta við vörum skal velja **Næst** á síðunni **Vörur**.
1. Síðan **Pöntunarupplýsingar** sýnir samantekt pöntunar. Yfirfarið upplýsingar um innihald pöntunar og afhendingar. Ef allt lítur rétt út skal velja **Senda** til að senda pöntunina.

    ![![Pöntunarupplýsingasíða](media/customer-portal-order-submit.png "Pöntunarupplýsingasíða")](media/customer-portal-order-submit.png "Order Information page")

### <a name="standard-data-setup"></a>Stöðluð gagnauppsetning

Til að tryggja liprari notendaupplifun fyllir viðskiptavinagáttin sjálfkrafa út gildin fyrir nokkra áskilda reiti. Þessi gildi eru byggð á upplýsingum í tengiliðafærslu viðskiptavinarins sem er að senda pöntunina.

Fyrir hverja [tengiliðafærslu](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) sem tilheyrir viðskiptavini sem notar viðskiptavinagáttina til að senda inn pantanir, verða gildi að vera tilgreind fyrir eftirfarandi áskilda reiti. Annars koma upp villur.

- **Fyrirtæki** – Lögaðili sem pöntunin tilheyrir
- **Mögulegur viðskiptavinur** - Viðskiptavinalykill sem tengist pöntuninni
- **Verðlisti** – Sérsniðin verðlisti fyrir viðskiptavin
- **Gjaldmiðill** – Gjaldmiðill verðsins
- **Senda til lands/svæðis** – Landið eða svæðið sem vörurnar verða sendar til

Eftirfarandi reitir eru sjálfkrafa stilltir fyrir einingu sölupöntunar:

- **Tungumál** - Tungumál pöntunarinnar (Gildið er sjálfkrafa tekið úr tengiliðafærslunni.)
- **Senda til lands/svæðis** – Landið eða svæðið sem vörurnar verða sendar til (gildið er sjálfkrafa tekið úr tengiliðafærslunni.)
- **Tengiliður** – notandi sem hægt er að hafa samband við til að fá upplýsingar um pöntunina (gildið er sjálfkrafa tekið úr tengiliðafærslunni.)
- **Fyrirtæki** - Lögaðilinn sem pöntunin tilheyrir (gildið er sjálfkrafa tekið úr tengiliðafærslunni.)
- **Mögulegur viðskiptavinur** - Viðskiptavinalykill sem tengist pöntuninni (sjálfgefið er að gildið sé tekið úr tengiliðafærslu.)
- **Reikningur viðskiptavinar** – Greiðslureikningur pöntunar (sjálfgefið gildi er mögulegur viðskiptavinur úr tengiliðafærslu.)
- **Heiti sölupöntunar** – Heiti sölupöntunar (sjálfgefið gildi er **sölupöntun**.)
- **Gjaldmiðill** – Gjaldmiðill verðs (sjálfgefið er að gildið sé tekið úr tengiliðafærslu.)
- **Verðlisti** – Sérsniðinn verðlisti fyrir viðskiptavininn (sjálfgefið er að gildið sé tekið úr tengiliðafærslu.)
- **Lýsing afhendingaraðseturs** – Afhendingaraðsetur sölupöntunar (sjálfgefið gildi er **lýsing á afhendingaraðsetri**.)

### <a name="modify-the-order-creation-process"></a>Breyta stofnferli pöntunar

Hægt er að breyta að vild útliti og notandaviðmóti viðskiptavinagáttar ef grunnstofnferli pöntunar er ekki breytt. Ef ætlunin er að breyta stofnferli pöntunar þarf að hafa nokkur atriði í huga.

Ekki fjarlægja eftirfarandi reiti úr einingu sölupöntunar í Common Data Service, því að þeir eru nauðsynlegir til að stofna sölupöntun í tvískiptum skrifum:

- **Fyrirtæki** – Lögaðili sem pöntunin tilheyrir
- **Heiti** - Heiti sölupöntunar
- **Gjaldmiðill** – Gjaldmiðill verðsins
- **Verðlisti** – Sérsniðin verðlisti fyrir viðskiptavin
- **Senda til lands/svæðis** – Landið eða svæðið sem vörurnar verða sendar til
- **Mögulegur viðskiptavinur** - Viðskiptavinalykill sem tengist pöntuninni
- **Tungumál** - Tungumál pöntunar (yfirleitt er þetta tungumál hugsanlegs viðskiptavinar.)
- **Lýsing afhendingaraðseturs** – Afhendingaraðsetur sölupöntunar

Fyrir vörur eru eftirfarandi reitir nauðsynlegir:

- **Afurð** – Afurðin sem á að panta
- **Magn** - Magn valdrar afurðar
- **Einng** – Mælieiningin (t.d., **þ.e.**, **kg** eða **kassi**)
- **Senda til lands/svæðis** – Land eða svæði afhendingar
- **Lýsing afhendingaraðseturs** – Afhendingaraðsetur pöntunar

Ganga þarf úr skugga um að viðskiptavinargáttin sendi á einhvern hátt gildi fyrir alla þessa reiti.

Ef bæta á reitum við síðuna, eða fjarlægja reiti, sjá [Stofna eða breyta fljótlegri stofnun skjámynda fyrir einfalda upplifun gagnaskráningar](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Ef ætlunin er að breyta því hvernig reitir eru forstilltir og hvernig gildi eru stillt þegar síðan er vistuð skal skoða eftirfarandi upplýsingar í fylgiskjölum Power Apps-gátta:

- [Fylla út reiti fyrirfram](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Stilla gildi á vista](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Sérsníða heimasíðu

Allar stýringar í gátt viðskiptavinar eru innbyggðar Power Apps-gáttastýringar. Hægt er að sérstilla þær með því að fylgja skrefunum í [Búa til síðu](https://docs.microsoft.com/powerapps/maker/portals/compose-page) í fylgiskjali Power Apps-gátta.

Eina sérstillta stýringin sem er í sniðmáti viðskiptavinagáttar er notuð til að búa til reitina á heimasíðunni.

![![Reitir á heimasíðunni](media/customer-portal-home-page-tiles.png "Reitir á heimasíðunni")](media/customer-portal-home-page-tiles.png "Tiles on the home page")

Til að breyta reitunum skal fylgja þessum skrefum.

1. Opnið [Forrit gáttarstjórnunar](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).
1. Á yfirlitssvæðinu vinstra megin er valið **Sniðmát pantana**.

    ![![Yfirlitssvæði gáttarstjórnunar](media/customer-portal-nav.png "Yfirlitssvæði gáttarstjórnunar")](media/customer-portal-nav.png "Portal Management navigation pane")

1. Velja skal síðusniðmátið sem kallast **Heim**.
1. Í reitnum **Vefsniðmát** skal velja tengilinn **Heim** til að opna frumkóðann fyrir þá síðu.

    ![![Reitur vefsniðmáts](media/customer-portal-web-template.png "Reitur vefsniðmáts")](media/customer-portal-web-template.png "Web Template field")

1. Nú ættirðu að sjá allan frumkóðann fyrir heimasíðuna og hægt er að breyta honum eftir þörfum.

## <a name="resources"></a>Forði

Frekari upplýsingar um hvernig hægt er að setja upp og sérsníða viðskiptavinagáttina eru í eftirfarandi tilföngum:

- [Power Apps fylgiskjöl gátta](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Tvískrifuð fylgiskjöl](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Um stuðningstíma gáttar](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Uppfæra gátt](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Flytja grunnstillingu gáttar](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 fyrir forrit Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)