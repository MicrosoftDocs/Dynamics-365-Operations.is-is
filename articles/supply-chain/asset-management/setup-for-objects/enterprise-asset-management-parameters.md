---
title: Færibreytur eignastýringar
description: Í eignastýringu verður að setja upp almennar breytur sem varða eignir, verkbeiðnir og tímasetningu vinnutilboða.
author: josaw1
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99ef5169d2c6a31efd3e7a7c92beade994f6e5f5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252010"
---
# <a name="asset-management-parameters"></a>Færibreytur eignastýringar

[!include [banner](../../includes/banner.md)]

Í eignastýringu verður að setja upp almennar breytur sem varða eignir, verkbeiðnir og tímasetningu vinnutilboða. Í þessu efnisatriði er útskýrt hvernig á að setja þær upp. Veldu **Eignastýringu** > **Uppsetningu** > **Færibreytur eignastýringar** til að opna síðuna.

> [!NOTE]
> Ef þú vilt setja upp kerfi sem inniheldur kynningu gagna til að prófa eiginleika Eignastýringar, sjá [Uppsetning sýniútgáfuumhverfis](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) fyrir leiðbeiningar.

## <a name="the-assets-tab"></a>Eignaflipinn

 Flipinn **Eignir** býður upp á eftirfarandi stillingar:

- **Sjálfgefin staðsetning** er staðalbúnaðurinn, sem er sjálfkrafa valinn á eignir þegar þú býrð til nýjar eignir.  
- Í reitnum **Venjulegt dagatal** velurðu dagatal sem á að nota til að reikna KPI eigna ef engin auðlind er valin á eign.  
- Í reitnum **Skoða** veldu staðalskjáinn sem sýndur er þegar þú opnar **Eignasýn** (**Eignastýring** > **Sameiginlegt** > **Eignir** > **Eignasýn**).
- **Sjálfgefin tegund beiðni** er venjuleg tegund viðhaldsbeiðni, sem er sjálfkrafa valin þegar þú býrð til nýja beiðni.  
- Spár um vinnslugerðir eru vistaðar í verkinu sem valið var í reitnum **Spáð verk**. Fyrir hverja verkgerð er ný virkni búin til í spáverkefninu. Spár um verkgerðina eru síðan vistaðar í spáverkefninu.  
- Í reitnum **Líkan** veldu spálíkanið sem notað er við verkgerð og verkbeiðnispár.

## <a name="the-work-orders-tab"></a>Flýtiflipi verkbeiðna

Flipinn **Verkbeiðnir** býður upp á eftirfarandi stillingar:

- **Sjálfgefin gerð verkbeiðna** skilgreinir staðlaðar stillingar við stofnun verkbeiðni.  
- **Gerð fyrirbyggjandi verkbeiðni** skilgreinir gerð verkbeiðni sem notuð er við stofnun verkbeiðna úr viðhaldsáætlunum. Ef þessi reitur er látinn vera auður er gerð verkbeiðnar í reitnum **Sjálfgefin gerð verkbeiðni** notaður.  
- Í reitnum **Tengd sía verkbeiðni** skilgreinir þú hámarksfjölda verkbeiðna sem geta tengst verkbeiðni. Til dæmis gerir ## þér kleift að hafa allt að 99 verkbeiðnir tengdar. Ef þú skilgreinir síu eins og lýst er hér, verða tengdar verkbeiðnir tölusettar [verkskilríki verkbeiðninnar sem verkbeiðni tengist] -01, -02, -03, og svo framvegis. Ef þú skilgreinir ekki síu á þenan reit fær tengd verkbeiðni næsta röð verkskilríkja.  
- Veldu **Já** fyrir **Afrita bilanir** ef þú vilt sjálfkrafa afrita bilanir sem eru skráðar í verkbeiðnum í tengdar viðhaldsbeiðnir. 
- Í reitnum **Stig** skilgreinir þú virkt staðsetningarstig sem er sjálfkrafa sett inn í verkbeiðni ef öll tengd verkpöntunarstörf vísa til sömu virku staðsetningar. Ef verkbeiðnistörfin tengjast ekki öll sama virku staðsetningu á skilgreindu stigi er reiturinn **Virk staðsetning** hafður auður í verkbeiðninni. Til dæmis, ef þú setur töluna „1“ inn í þennan reit, þá er það efsta stigið í virkri staðsetningu. Ef þú setur inn töluna „0“ í þennan reit hefur þú ekki skilgreint sérstakt virkni staðsetningarstig, aðeins að öll verkbeiðnistörf í verkbeiðni verða að tengjast sama virku staðsetningu fyrir þá virku staðsetningu til að vera bætt við verkbeiðni.  
- Hægt er að velja bækur sem notuð eru þegar neysla er lögð í verkbeiðni á flýtiflipanum **Almennt** í reitunum **Klukkustund**, **Liður**, og **Kostnaður**.  
- Í retinum **Upprunamál afurðar** velurðu hvaða tungumál á að nota fyrir vöruheiti í eignastjórnunarskýrslum. Þú getur valið tungumálið sem sett er upp á fyrirtækjareikningnum, eða tungumálið sem sett er upp fyrir notandann sem er skráður inn.  
- Veldu **Já** fyrir **Rauntímauppfærsla** ef þú vilt uppfæra sjálfkrafa breytingar á vanskilum á starfstegund, viðhaldsáætlunum og viðhaldsumræðum.
  - Ef þú velur **Nei** eru breytingar á vanskilum starfstegunda, viðhaldsáætlunum og viðhaldsumræðum ekki uppfærðar sjálfkrafa í eignastýringu.
  - Veldu **Nei** ef mikið magn gagna er samstillt, til dæmis margar eignir eða virkar staðsetningar sem settar eru upp í viðhaldsáætlunum eða viðhaldsumferðum, eða mikill fjöldi viðhaldsáætlana eða umferða.  
  - Ef þú gerir breytingar á vanskilum í starfi eða viðhaldsáætlunum eða viðhaldsumferðum og þú hefur valið **Nei** í rauntíma uppfærslu, gæti verið að viðvörun sé ekki sýnd ef breytingarnar hafa áhrif:
    - Virkar staðsetningar settar upp á viðhaldsáætlunum eða umferðum  
    - Hlutir settir upp á viðhaldsáætlunum eða umferðum  
    - Uppsetning viðhaldsáætlana  
    - Uppsetning á viðhaldslotur  
- Á flytiflipanum **Flokkur** er hægt að skilgreina sjálfgefna flokka sem varða neyslu í verkbeiðnum.  

## <a name="the-work-order-scheduling-tab"></a>Áætlanaflipi verkbeiðni

Flipinn **Áætlanagerð verkbeiðni** býður eftirfarandi stillingar á flýtiflipanum **Almennt**:

- **Tímamörk áætlunar** skilgreinir tímabil í dögum, reiknað út frá áætluðum upphafsdegi verkbeiðni, þar sem verkbeiðnir eru skipulögð.  
- **Aðaláætlun** snýr að auðlindum í einingunni **Fyrirtækisstjórnun**. Ef þú velur aðalskipulag á þessu sviði muntu geta séð fyrirvara um afkastagetu sem tengjast verkbeiðni í **Frátekin afkastageta** (flipinn **Fyrirtækisstjórnun** > **Tilföng** > **Tilföng** > velja tilföng > flipinn **Tilföng** > hnappurinn **Frátekin afkastageta**). Ef þú hefur þennan reit auðan geturðu séð álag sem tengist verkbeiðnum í **Álag** (**Fyrirtækisstjórnun** \> **Tilföng** \> **tilföng** \> velja tilföng á flipanum \> **Tilföng** \> hnappnum **Álag**).  

>[!NOTE]
>Valið varðandi notkun aðalskipulags í einingunni **Eignastýring** og tengt form sem notað er til að fá yfirsýn yfir frátekna afkastagetu eða álag er stöðluð uppsetning. Það fer eftir uppsetningu þinni í reitnum **Aðaláætlun** en þú munt geta fengið aðgang að upplýsingum um afkastagetu í annaðhvort **Frátekinni afkastagetu** eða **Álagi** í **Fyrirtækjastjórnun**. Það er ekki hægt að búa til uppsetningu þar sem frátekin afkastageta er sýnd í báðum skjánum.  

Reitirnir sem lýst er í eftirfarandi lista tengjast allir reiknuðum matseinkunnum, sem eru notaðir til að reikna forgang verkbeiðni við tímasetningu verkbeiðni.

- **Forgangur** - Einkunnagjöf reiknuð ásamt einkunnagjöf í reitunum **Markástand** og **Upphafsdagur**. Tölunni á þessu sviði er deilt með tölunni í reitnum **Forgangsröðun** í verkbeiðni. Til dæmis, ef gildið „5,00“ er sett inn í þennan reit og verkbeiðni hefur forgang „20“ er einkunnagjöf fyrir forgang 0,25.  
- **Markástand** - Einkunnagjöf reiknuð ásamt einkunnagjöf í reitunum **Forgangur** og **Upphafsdagur**. Tölunni á þessu sviði er margfölduð með tölunni í reitnum **Markástand** í verkbeiðni. Til dæmis, ef gildið „10,00“ er sett inn í þennan reit og verkbeiðni hefur markástand „5“ er einkunnagjöf fyrir markástand 50.  
- **Upphafsdagur** - Einkunnagjöf reiknuð ásamt einkunnagjöf í reitunum **Forgangur** og **Markástand**. Þessi reitur gefur til kynna daglegt stig sem neikvætt gildi og er borið saman við reitinn **Væntanlegt upphaf** í verkbeiðni. Til dæmis, ef gildið „10,00“ er sett inn í þennan reit og áætlaður upphafsdagur verkbeiðni er þrír dagar frá nú er matsniðurstaðan mínus 30,00. Bætir við niðurstöðum 0,25 og 50 úr dæmunum í reitunum **Forgangsröðun** og **Markástand** sem lýst er hér að ofan gefur samtals plús 20,25. Sú tala er borin saman við allar aðrar einkunnir verkbeiðni við tímasetningu vinnu og þá er stigahæsta einkunnin síðan skipulögð.  
- **Ábyrgur starfskraftur** - einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfsmannahópur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Ef gildið „50,00“ er sett inn í þennan reit og ábyrgur starfskraftur hefur verið valinn í verkbeiðni fær starfskrafturinn 50 stig í heildarútreikningi starfskrafta við tímasetningu verkbeiðni.  
- **Ábyrgur starfsmannahópur** - einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfskraftur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Ef gildið „50,00“ er sett inn í þennan reit og ábyrgur starfskraftur hefur verið valinn í verkbeiðni fær starfskrafturinn 50 stig í heildarútreikningi starfskrafta við tímasetningu verkbeiðni.  
- **Takmarka við ábyrgð** - Þetta takmarkar fjölda starfskrafta sem eru tiltækir fyrir tímasetningu verkbeiðni. Veldu **Nei** ef þú vilt reikna stig fyrir alla starfskrafta, óháð því hvort þeir eru settir upp sem ábyrgir starfskraftar eða hluti af ábyrgum starfsmannahópi. Veldu **Já** ef þú vilt reikna stig fyrir starfskrafta sem eru settir upp sem ábyrgir starfskraftar í verkbeiðninni og / eða eru með í ábyrgum starfsmannahópi sem valinn var í verkbeiðni.  
- **Æskilegur starfskraftur** - Einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfsmannahópur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Fjögur stigaskorin eru reiknuð út og lögð saman til að veita stig sem er notað til að velja hvaða starfsmanni skuli úthlutað til hvaða verkbeiðni meðan á tímasetningu verkbeiðni stendur. Ef gildið „10,00“ er sett inn í þennan reit og starfskraftur hefur verið valinn sem æskilegur starfskraftur í verkbeiðni fær sá starfskrafturinn 10 stig í heildarútreikningi starfskrafta við tímasetningu verkbeiðni.  
- **Æskilegur starfsmannahópur** - Einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfsmannahópur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Ef gildið „10,00“ er sett inn í þennan reit og starfskrafti hefur verið úthlutað í æskilegan starfsmannahóp sem er valinn í verkbeiðni fær sá starfskraftur 10 stig í heildarútreikningi starfskrafta við tímasetningu verkbeiðni.  
- **Takmarka við æskilegt** - Þetta takmarkar fjölda starfskrafta sem eru tiltækir fyrir tímasetningu verkbeiðni. Veldu **Nei** ef þú vilt reikna stig fyrir alla starfskrafta, óháð því að þeir eru settir upp sem æskilegir starfskraftar eða hluti af æskilegum starfsmannahópi. Veldu **Já** ef þú vilt aðeins reikna stig fyrir alla starfskrafta, sem settir upp sem æskilegir starfskraftar og/eða eru hluti af æskilegum starfsmannahópi.  
- **Staðsetning** - Einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfsmannahópur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Ef gildi „3.000,00“ er sett inn í þennan reit fær starfsmaður 3.000 stig í útreikningnum ef starfsmaðurinn er staðsettur í sömu verksmiðju eða aðstöðu og eignin sem áætla á vinnslu á.  
  - Ef fyrirtæki þitt notar virkar staðsetningar fá starfskraftar fulla einkunn ef þeir eru staðsettir á virkri staðsetningu sem tengist eigninni. Ef virk staðsetning eignarinnar hefur yfireign, þá fá starfskraftr á þeirri virku staðsetningu 1/2 stig. Ef þessi staðsetning er einnig með yfireiningu fá starfskraftar á þeim stað 1/3 stig. Ef þessi staðsetning er einnig með yfireiningu fá starfskraftar á þeim stað 1/4 stig o.s.frv.  
  - Ef fyrirtæki þitt notar eignastaðsetningu, sem við mælum ekki með, er staðsetning, landsvæði og svæði notað til að reikna staðsetningarskor. Starfsmenn fá fulla einkunn ef þeir eru staðsettir á staðsetningu og landsvæði og svæði sem tengjast eigninni. Ef staðsetning starfskrafts passar aðeins við staðsetningu og landsvæði er einkunnagjöf fyrir starfsmanninn 2/3 af fullri einkunn. Ef staðsetning starfskrafts passar aðeins við staðsetningu er einkunnagjöf fyrir starfsmanninn 1/3 af fullri einkunn.  
- **Takmarka við staðsetningu** - Þetta takmarkar fjölda starfskrafta sem eru tiltækir fyrir tímasetningu verkbeiðni. Veldu **Nei** ef þú vilt reikna stig fyrir alla starfsmenn á öllum starfhæfum stöðum. Veldu **Já** ef þú vilt aðeins reikna stig fyrir starfsmenn sem eru tengdir virkri staðsetningu verkbeiðninnar.

>[!NOTE]
>Reitirnir þrír "Takmarka við..." auka hraðann á tímasetningu verkbeiðni til að takmarka fjölda skora sem reiknað er fyrir starfsmenn.

**Upphafsdagur starfskrafts** - Einkunnagjöf reiknuð ásamt einkunnagjöfunum **Ábyrgur starfsmannahópur**, **Æskilegur starfskraftur**, **Æskilegur starfsmannahópur**, **Eignastaðsetning**, og **Upphafsdagur**. Þessi reitur gefur til kynna daglegt stig sem neikvætt gildi og er borið saman við reitinn **Væntanlegt upphaf** í verkbeiðni. Ef gildið „10,00“ er sett inn í þennan reit og áætlaður upphafsdagur verkbeiðni er á morgun er matsniðurstaðan mínus 10,00.

  - Að því gefnu að enginn ábyrgur starfsmaður og ábyrgur starfsmannahópur hafi verið valinn í vinnuskipun sem á að skipuleggja - þú bætir við og dregur frá stigagjöf í dæmunum í reitunum **Æskilegur starfsmaður**, **Valinn starfsmannahópur**, **Eignastaðsetning** og **Upphafsdagur** hér að ofan færðu samtals 3.010,00. Þetta þýðir háa einkunn fyrir starfsmanninn sem þegar er valinn valinn starfsmaður sem og innifalinn í valinn starfsmannahópur í vinnutilskipuninni, og starfsmaðurinn er einnig staðsettur í sömu aðstöðu og eignin sem þarf að skipuleggja starf fyrir. Það þýðir að góðar líkur eru á því að viðkomandi starfskraftur verði valinn til að ljúka verkinu meðan á tímasetningu vinnu stendur.  
  - Ef gildið „0,00“ er sett inn í einn af átta reitum hér að ofan, verður það einkunnagjöf ekki notuð við tímasetningu verkbeiðni.  

## <a name="the-document-types-tab"></a>Flipi skjalagerðar

Veldu skjalategundirnar sem eiga að vera tiltækar til að prenta viðhengi sem tengjast vinnuskýrslu. Þetta er gert með því að velja skjalagerðina í hlutanum **Laus** og velja hnappinn ![áfram ör](media/15-setup-for-objects.png). Ef þú vilt fjarlægja valda skjalategund skaltu velja skjalagerðina í hlutanum **Valið** og velja ![aftur ör](media/16-setup-for-objects.png).

## <a name="the-number-sequences-tab"></a>Flipinn Númeraraðir

Veldu nauðsynlegar töluraðir í þessum kafla. Það eru tvær töluraðir fyrir eignir: ein fyrir handvirkt stofnaðar eignir og ein fyrir eignir búnar til með eignum í bið.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]