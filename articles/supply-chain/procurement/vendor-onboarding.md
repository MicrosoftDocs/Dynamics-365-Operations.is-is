---
title: Nýliðun lánardrottna
description: Þetta efnisatriði lýsir ferlinu við nýliðun lánardrottna. Það útskýrir aðgerðirnar sem krafist er af ýmsum hlutverkum meðan á þessu ferli stendur.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, SysUserRequestListPage, VendRequestListPage, VendRequestCompanyProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 396b3c4622c612fa082796080aa230a0d693ce4f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671001"
---
# <a name="onboard-vendors"></a>Nýliðun lánardrottna

[!include [banner](../includes/banner.md)]

---

Nýir lánardrottnar geta verið teknir inn og skráðir sem lánardrottnar í Microsoft Dynamics 365 Supply Chain Management, byggt á upplýsingum sem safnað er frá einstaklingi sem kemur fram fyrir hönd lánardrottins.

Ferlið samanstendur af eftirfarandi skrefum, þar sem ýmis hlutverk framkvæma aðgerðir í kerfinu.

1. **Gagnastjórnun OData** - Eininga innflutningur - Upphafleg beiðni er beiðni væntanlegs lánardrottinn um skráningu. Venjulega, þessi beiðni kemur frá upptökum, svo sem vefþjóni sem hýstur er af viðskiptamanni, sem býður upp á nafnlausan aðgang. Söluaðilar geta skráð sig með því að veita grunnupplýsingar, svo sem nafn lánardrottins, rökstuðning, fyrirtækjanúmer og nafn og netfang tengiliðar. Beiðnirnar eru fluttar inn í gegnum Gagnastjórnun viðmót.
2. **Listasíða fyrir skráningarbeiðni væntanlegs lánardrottins** - Byggt á upplýsingum sem gefnar eru upp í skráningarbeiðni væntanlegs lánardrottins ákveður innkaupastjóri hvort lánardrottinn skuli tekinn inn. Innkaupastjóri skoðar innsendar beiðnir á listasíðunni **Skráningarbeiðni væntanlegs lánardrottins**.
3. **Verkflæði notandaúthlutunar** - Þegar innkaupastjóri hefur staðfest upplýsingarnar í innsendri beiðninni og hefur ákveðið að halda áfram með nýliðunarferlið, úthlutar verkflæði notandabeiðninnar nýjum notanda og sendir boðstölvupóst til að samþykkja tengiliðinn sem sannvottaðan notanda Microsoft Dynamics 365.
4. **Leiðsagnarforrit fyrir skráningu lánardrottins** Tengiliður lánardrottins skráir sig inn með því að nota nýja notandareikninginn. Hann fylgir leiðsagnarforriti fyrir skráningu lánardrottins til að veita upplýsingar, svo sem heimilisföng, viðskiptaupplýsingar, innkaupaflokka og svör við spurningalista.
5. **Vinnuflæði samþykkis** - Beiðni lánardrottins sem inniheldur skráningarupplýsingar er búið til. Þessi beiðni lánardrottins er lögð fram til vinnuflæðis og er send til skoðunar og samþykkis.
6. **Stofnun lánadrottinssniðmáts og breyting notenda hlutverk** - Þegar lánardrottinsbeiðni er samþykkt, er búin til lánardrottnaskrá. Notandareikningur tengiliðs lánardrottins er annaðhvort veitt leyfi til samstarfs lánardrottna eða gerður óvirkt.

Eftirfarandi tafla sýnir skrefin og hlutverkin sem eru innifalin í ferlinu.

| Hlutverk og „ferli“       | Gagnastjórnun OData - innflutningur einingar | Listasíða yfir skráningarbeiðnir væntanlegs lánardrottins | Verkflæði notandaúthlutunar | Leiðsagnarforrit fyrir skráningu lánardrottins | Samþykktarverkflæði | Stofnun lánardrottinssniðmáts og breyting notandahlutverks |
|--------------------------|---|---|---|---|---|---|
| System                   | Beiðnin fyrir nýjan lánardrottinn er flutt inn. | | | | | Eftir að beiðni lánardrottins hefur verið samþykkt, er lánardrottinsskrá búin til. |
| Innkaupastjóri | | Hefja innleiðingarferlið. | | | Yfirfara og annað hvort samþykkja eða hafna lánardrottinsbeiðninni. | |
| Stjórnandi            | | | Búðu til notanda í Supply Chain Management og Microsoft Azure. | | | |
| Tengiliður lánardrottins    | | | Senda tölvupóst til tengiliðsins. | Skrá upplýsingar um lánardrottinn. | | |

Til að fá snögga sýnikennslu um innleiðingarferli lánardrottins skal horfa á þetta stutta YouTube myndband um [Hvernig skal innleiða nýjan lánardrottinn í Finance and Operations](https://www.youtube.com/watch?v=0KUc3AGaTKk).

## <a name="importing-the-prospective-vendor-registration-request"></a>Flytja inn skráningarbeiðni væntanlegs lánardrottins

Skráningarbeiðni væntanlegs lánardrottins er eining í Supply Chain Management. Hægt er að setja kerfið þannig upp að það flytji inn gögn gegnum þessa einingu. 

Eftirfarandi tafla sýnir upplýsingarnar sem þessi eining inniheldur, og hægt er að flytja inn.

| Svæði                        | lýsing |
|------------------------------|-------------|
| Nafn lánardrottins                  | Nafn lánardrottins. |
| Réttlæting viðskipta       | Ástæða eða ástæður fyrir beiðni lánardrottins. |
| Kennitala          | Opinberlega þekkt skráningarnúmer. |
| Atvinnugrein             | Auðkenna atvinnugrein lánardrottins. |
| Fornafn tengiliðar  | Fornafn einstaklingsins sem verður boðið að skrá upplýsingar lánardrottins. |
| Millinafn tengiliðar | Millinafn einstaklingsins sem verður boðið að skrá upplýsingar lánardrottins. |
| Eftirnafn tengiliðar   | Eftirnafn einstaklingsins sem verður boðið að skrá upplýsingar lánardrottins. |
| Netfang tengiliðar       | Netfangið sem verður notað til að búa til nýjan notanda í Supply Chain Management, og það verður skráð á Azure Active Directory (Azure AD) reikningnum sem leigjandi notar. |
| Dagsetning sendingar               | Dagsetning þegar beiðnin var stofnuð í ytra kerfi. |
| Lögaðili                 | Lögaðili þar sem lánardrottinn er að biðja um að fá verða lánardrottinn. Þetta gildi verður að vera kóði lögaðila sem hefur verið skráður í Supply Chain Management. Ef ekkert gildi er móttekið gegnum innflutningsferlið, er gildi frá Innkaup og aðföng færibreytur beitt. |
| Gerð lánardrottins                  | Lánardrottinn getur verið annað hvort fyrirtæki eða einstaklingur. Gerð lánardrottins ákvarðar hvernig lánardrottinn er að lokum búinn til. |

Eftir að skráningarbeiðni væntanlegs lánardrottins hefur verið flutt inn birtist það á listasíðunni yfir **skráningarbeiðni væntanlegs lánardrottins**. Frá þessari listasíðu getur innkaupastjóri boðið notanda. Notandabeiðni um að veita notandanum forsjá er send í vinnuflæði.

## <a name="submitting-a-prospective-vendor-user-request"></a>Senda inn notandabeiðni væntanlegs lánardrottins

Tilgangur notandabeiðni væntanlegs lánardrottins er að veita þeim sem sendu upphaflegu beiðnina forsjá, þannig að hann geti skráð sig inn í Supply Chain Management með því að nota tölvupóstreikninginn sem er að finna í skráningarbeiðni væntanlegs lánardrottins.

Notandabeiðni væntanlegs lánardrottins er unnin af verkflæði notandabeiðni. Verkflæði á samskipti í gegnum Azure AD AD B2B samvinnu. Það stofnar notanda í Supply Chain Management sem hefur viðeigandi öryggisstillingar.

Nýir notendur sem eru settir upp hafa eftirfarandi öryggishlutverk:

- Ytri kerfisnotandi
- Væntanlegur lánardrottinn (ytri)

Hin nýja notandi mun fá tölvupóst sem er búið til af verkflæði notandabeiðni. Þessi tölvupóstur býður notanda að skrá sig inn í kerfið.

Til að fá upplýsingar um grunnstillingar tölvupóstsins og verkflæðisins almennt, sjá lýsingu á verkflæði notandabeiðni í [Setja upp og vinna með lánardrottna](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Skráning lánardrottins

Notandi sem er væntanlegur lánardrottinn sem skráir sig inn í Supply Chain Management mun sjá fyrstu síðu leiðsagnarforrits fyrir skráningu lánardrottins, þar sem hann eða hún getur slegið inn lánardrottinsupplýsingar.

Leiðsagnarforritið endurspeglar grunnstillingar beiðni lánardrottins. Landið eða svæðið þar sem lánardrottinn á viðskipti ákvarðar hvaða upplýsingar er beðið um í leiðsagnarforritinu og hvaða upplýsingar eru áskildar.

Nánari upplýsingar um grunnstillingar fyrir lánardrottnabeiðnir sjá [Setja upp og vinna með samstarf lánardrottna](set-up-maintain-vendor-collaboration.md). Í eftirfarandi töflu er yfirlit yfir síðurnar sem notuð eru í leiðsagnarforritinu og tilgang hverrar síðu.

| Síða                       | lýsing |
|----------------------------|-------------|
| Land/svæði             | Landið eða svæðið ákvarðar þær grunnstillingar fyrir lánardrottinsbeiðni sem er beitt á eftirstandandi síðum leiðsagnarforritsins. Það ákvarðar einnig gildi í **Skattaríki** uppflettingunni. |
| Skilmálar       | Þessi síða gæti verið tiltæk, allt eftir grunnstillingum lánardrottinsbeiðninnar. Ef hún er tiltæk þarf notandi að samþykkja skilmálana til að halda áfram. |
| Lánardrottnaupplýsingar         | Þessi síða inniheldur nafn lánardrottins, sem er sjálfkrafa slegið inn frá upphaflegri skráningarbeiðni væntanlegs lánardrottins. Það inniheldur einnig fyrirtækjanúmer, símanúmer lánardrottins, faxnúmer og netfang og heimilisföng lánardrottins í ýmsum tilgangi. |
| Upplýsingar tengiliðar | Þessi síða inniheldur nafn tengiliðarins, sem er sjálfkrafa slegið inn frá upphaflegri skráningarbeiðni væntanlegs lánardrottins. Það inniheldur einnig símanúmer og netfang tengiliðar og heimilisföng tengiliðar í ýmsum tilgangi. |
| Viðskiptaupplýsingar       | Þessi síða inniheldur skattskráningarnúmer (fyrir mismunandi löndum eða svæðum) og fjölda starfsmanna. Það sýnir einnig hvort fyrirtækið er minnihluta í eigu. |
| Innkaupaflokkar     | Þessi síða inniheldur innkaupaflokkana sem lánardrottinn óskar eftir samþykki fyrir. Notandi getur valið flokkur í tegundarstigveldi innkaupa. Þú getur grunnstillt fjölda stiga sem eru sýnd í stigveldi við **Innkaup og aðföng færibreytur** &gt; **Lánardrottnasamstarf** undir **Innkaup og aðföng** &gt; **Uppsetning**. |
| Spurningalistar             | Leiðsagnarforritið gæti verið með safn spurningalista fyrir lánardrottinn. Spurningalistar sem birtast í leiðsagnarforritinu eru grunnstilltar annaðhvort á beiðni lánardrottins eða samkvæmt innkaupaflokki. Ef spurningalistar eru stilltar samkvæmt hverja innkaupaflokk, þá ákvarða innkaupaflokkarnir sem lánardrottinn óskar eftir samþykki fyrir spurningalistana sem birtast í leiðsagnarforritinu. Á síðunni **Innkaupaflokkar** er hægt að bæta við spurningalista undir viðkomandi flokki og stilla virknitegund á **Nýliðun lánardrottna**. |

Þegar notandi sem er væntanlegur lánardrottinn er búinn að fara í gegnum leiðsagnarforritið fyrir skráningu lánardrottins, er búin til beiðni lánardrottins.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Senda inn beiðni lánardrottins handvirkt eða sjálfvirkt

Beiðni lánardrottins er hægt að búa til sem drög og handvirkt sent inn á verkflæði. Að öðrum kosti getur lánardrottnabeiðnin verið send inn sjálfkrafa á verkflæði þegar búið er að fara í gegnum leiðsagnarforritið fyrir skráningu lánardrottins. Beiðni er hægt að senda inn handvirkt ef til dæmis innkaupastjóri vill meta hvort beiðni skuli flutt í gegnum samþykkisferli áður en hún er send inn á verkflæði.

- Veldu **Innkaup og aðföng færibreytur** &gt; **Lánardrottnasamstarf** og veldu síðan **Sjálfgefin innsending skráningu væntanlegs lánardrottins til verkflæðis** til að grunnstilla lánardrottnabeiðni svo að það sé sent inn sjálfkrafa til verkflæðis þegar búið er að fara í gegnum leiðsagnarforrit fyrir skráningu lánardrottins.

## <a name="vendor-requests"></a>Beiðnir lánardrottins

Lánardrottnabeiðnir eru tiltækar á **Notendabeiðnir fyrir samstarf lánardrottna** síðunni.

Lánardrottnabeiðni inniheldur upplýsingar sem væntanlegur lánardrottna notandi færði inn í leiðsagnarforrit fyrir skráningu lánardrottins.

Beiðnin leyfir þér að skoða upplýsingar um lánardrottinn og ákveða hvort lánardrottinn ætti að verða skráður lánardrottinn.

Lánardrottnabeiðnin ætti að vera send inn til vinnuflæðis og hún ætti að vera flutt til viðkomandi aðila til skoðunar og samþykktar. Grunnupplýsingar um hvernig á að setja upp verkflæði er að finna í [Innkaup og aðföng verkflæði](procurement-sourcing-workflows.md).

Eftirfarandi tafla sýnir stöðurnar sem lánardrottnabeiðnir geta haft.

| Staða                     | lýsing |
|----------------------------|-------------|
| Drög                      | Lánardrottnabeiðnin hefur ennþá ekki verið send inn. |
| Beiðni send inn          | Lánardrottnabeiðnin hefur verið send inn og fyrsta skrefið í verkflæðinu er í ferli. |
| Yfirferð í bið             | Ef það eru margir endurskoðendur í verkflæðisverkefni getur endurskoðandi samþykkt að endurskoða lánardrottnabeiðni og ljúka svo endurskoðuninni. Ef það er aðeins einn endurskoðandi, getur sá þátttakandi lokið við endurskoðunina með því að velja **Lokið** í verkflæðisaðgerðinni. Hann þarf ekki að samþykkja vinnuliðinn fyrst. |
| Beiðni bíður samþykkis   | Lánardrottnabeiðni hefur verið send til þátttakenda til samþykktar og það er möguleiki að biðja um frekari upplýsingar. Beiðni um viðbótarupplýsingar veldur því að vinnuliðurinn er flutt aftur til sendanda. Lánardrottnabeiðni getur einnig verið samþykkt eða hafnað meðan það er í þessari stöðu. |
| Beiðni um að breyta umsókn | Óskað hefur verið eftir viðbótarupplýsingum af samþykktaraðila, og lánardrottnabeiðnin hefur verið send til þess aðila sem innsendi lánardrottnabeiðnina. Innsendingaraðilinn getur bætt við nauðsynlegum upplýsingum og síðan endursent lánardrottnabeiðnina. Ef lánardrottnabeiðni er endurinnsend, er stöðunni breytt aftur í **Beiðni í bið eftir samþykki** staða. |
| Beiðni samþykkt           | Þessari staða er lokastaða. |
| Beiðni hafnað           | Þessari staða er lokastaða. |

## <a name="approving-a-vendor-request"></a>Samþykkja beiðni lánardrottins

Þegar lánardrottnabeiðni er samþykkt, er lánardrottnareikningur búinn til og staðan **Samþykkt** birtist bæði í upphaflegri skráningarbeiðni væntanlegs lánardrottins og lánardrottnabeiðninni.

Áður en þú samþykkir lánadrottnabeiðni, skaltu á síðunni **Nýr lánardrottinn**, á **Almennt** flýtiflipanum velja **Lánardrottnaflokkur** til að velja lánardrottnaflokk.

Ef væntanlegur lánadrottna notandi ætti að hafa aðgang að Supply Chain Management sem notandi samstarfs lánardrottna sem er fulltrúi lánardrottins, skal stilla samstarf lánardrottna aðgangsheimild á **Já**. Til að slökkva á notandareikningnum sem væntanlegur lánardrottinn notaði til að skrá sig inn, skaltu stilla þessa heimild á **Nei**.

Ef aðgangsheimild að samstarfi lánardrottna er stillt á **Já**, þegar lánardrottnabeiðnin er samþykkt, er beiðni lögð fram um að breyta hlutverki notanda svo að notandinn hafi hlutverkin sem eru skilgreind fyrir **Lánardrottinn** tegund í **Ytri hlutverk**. Ef þetta heimild er stillt á **Nei**, þegar lánardrottnabeiðnin er samþykkt, er beiðni send inn til að gera notandann óvirkan. Í þessu tilviki verður að setja upp verkflæði til að gera notandareiðbeini óvirka.

Ef búa á til lánardrottnareikningur þegar lánardrottnabeiðnin er samþykkt, verður númeraröð til að búa til lánardrottna frá lánardrottnabeiðnum að vera stillt á **Sjálfvirkt**.

Til að fá yfirlit yfir aðgangsheimildir notanda í samstarfi lánardrottna, sjá [Setja upp og vinna með samstarf lánardrottna](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Hafna beiðni lánardrottins

Ef lánardrottnabeiðni er hafnað skal velja ástæðu fyrir höfnun í lánardrottnabeiðninni.

Þegar lánardrottnabeiðni er hafnað er beiðni send til að gera notandann óvirkan. Í þessu tilviki verður að setja upp verkflæði til að gera notandareiðbeini óvirka. Frekari upplýsingar, sjá [Setja upp og vinna með samstarf lánardrottna](set-up-maintain-vendor-collaboration.md).

Þegar lánardrottnabeiðni er hafnað birtist staðan **Hafnað** bæði á upphaflegri skráningarbeiðni væntanlegs lánardrottins og á lánardrottnabeiðninni.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Eyða skráningarbeiðni væntanlegs lánardrottins með ýmsar stöður

Hin ýmsu stig skráningarbeiðni væntanlegs lánardrottins gefa yfirlit yfir framvindu beiðninnar.

Með því að nota **Eyða** aðgerðina á skráningarbeiðni væntanlegs lánardrottins, getur þú hreinsað og fjarlægja keðju skráa sem hefur verið búin til og þú getur gert notandareikningnum óvirkan. Niðurstaðan af **Eyða** aðgerðinni er breytileg eftir því hvaða stöðu skráningarbeiðni væntanlegs lánardrottins er með, eins og sýnt er í eftirfarandi töflu.


|          Staða          |                                                                                     Lýsing stöðu                                                                                      |                                                                                                                                                            Niðurstaða aðgerðarinnar Eyða                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Nýjar            |                                                                         Engar aðgerðir hafa verið beint að beiðninni.                                                                          |                                                                                                                                              Skráningarbeiðni væntanlegs lánardrottins er eytt.                                                                                                                                               |
|      Beðið um notanda      | Þegar þú velur <strong>Bjóða notanda</strong> er staðan breytt í <strong>Notanda boðið</strong>, og beiðni væntanlegs notanda er búin til og send inn til verkflæði notandabeiðni. |                                                                                                          Þú getur ekki eytt skráningarbeiðni væntanlegs lánardrottins sem hefur þessa stöðu, vegna þess að verkflæði notandabeiðni er ekki lokið.                                                                                                          |
|       Notanda boðið       |                                                               Verkflæði notandabeiðni er samþykkt, og notandi er stofnaður.                                                               |                                                                                                                      Beiðni um að gera notandann óvirkan er búin til og skráningarbeiðni væntanlegs lánardrottins er eytt.                                                                                                                      |
| Skráning í ferli |                                                         Nýja notandinn hefur skráð sig inn og hefur opnað leiðsagnarforrit fyrir skráningu lánardrottins.                                                          |                                                                                     Beiðni um að gera notandann óvirkan er búin til og skráningarbeiðni væntanlegs lánardrottins og gögnin sem voru slegin inn í leiðsagnarforrit fyrir skráningu lánardrottins er eytt.                                                                                      |
|  Beiðni lánardrottins stofnuð  |                                                                     Búið er að fara í gegnum leiðsagnarforrit fyrir skráningu lánardrottins.                                                                      | Beiðni um að gera notandann óvirkan er búin til og skráningarbeiðni væntanlegs lánardrottins, gögnin sem voru slegin inn í leiðsagnarforrit fyrir skráningu lánardrottins og lánardrottnabeiðninni er eytt.<blockquote>[!NOTE]<br>Þú getur ekki notað <strong>Eyða</strong> aðgerð þegar lánardrottnabeiðni er í endurskoðunarferli í verkflæðinu.</blockquote> |
|         Samþ.         |                                                                               Lánardrottnabeiðnin er samþykkt.                                                                               |                                                                                                   Skráningarbeiðni væntanlegs lánardrottins, gögnin sem voru slegin inn í leiðsagnarforrit fyrir skráningu lánardrottins og lánardrottnabeiðninni er eytt.                                                                                                    |
|         Hafnað         |                                                                               Lánardrottnabeiðninni er hafnað.                                                                               |                                                                                                   Skráningarbeiðni væntanlegs lánardrottins, gögnin sem voru slegin inn í leiðsagnarforrit fyrir skráningu lánardrottins og lánardrottnabeiðninni er eytt.                                                                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]