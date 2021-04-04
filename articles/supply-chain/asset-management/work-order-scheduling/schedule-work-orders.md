---
title: Áætla verkbeiðnir
description: Þetta efni útskýrir hvernig á að raða verkbeiðnum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderSchdulePreviewPart, EntAssetWorkOrderScheduleExclusively, EntAssetWorkOrderSchduleInfoPart, EntAssetWorkOrderScheduleListPage, EntAssetWorkOrderSchedule, EntAssetWorkOrderScheduleDelete
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6c9a15d90d2cb5d24bcc18f8cbd4f0076efaf6a8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263833"
---
# <a name="schedule-work-orders"></a>Áætla verkbeiðnir

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir hvernig á að raða verkbeiðnum í eignastýringu. 

Nauðsynlegur fjöldi klukkustunda fyrir verkbeiðni er skilgreindur af summunni yfir spáða tíma að frádregnum bókuðum tímum. Ef þörf er á meiri tíma verður að aðlaga spána til samræmis. Í **Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir** er hægt að skoða eða breyta spám um verkbeiðni með því að velja verkbeiðnina og smella á **Spá** á flipanum **Verkbeiðni**. Þegar verkbeiðnir hafa verið búnar til og áætlaðar er næsta skref að úthluta nauðsynlegu viðhaldsstarfsfólki og verkfærum til að ljúka verkbeiðnunum.

Aðeins er hægt að skipuleggja verkbeiðnir með líftímastöðu verkbeiðni sem gerir ráð fyrir tímasetningu. Leyfa tímasetningu er sett upp á flýtiflipanum **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Líftímastöður** > **Almennt** > skiptihnappnum **Leyfa tímasetningu**.

1. Smelltu á **Eignastjórnun** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir**.

2. Veldu verkbeiðnirnar sem þú vilt raða í listanum. Til dæmis geturðu raðað listanum eftir **Núverandi líftímastöðu**.

3. Á flipanum **Almennt** er smellt á **Áætlun**.

4. Í glugganum **Tímasetja verkbeiðnir** er hægt að bæta við vali um áætlaðan upphafsdag og þjónustustig, ef þess er krafist. Ef áætlunarferlið á að fylgjast með takmörkunum afkastagetu varðandi tilföng sem eru þegar áætluð fyrir aðrar vinnslur skal tryggja að skiptihnapparnir **Eign**, **Verkfæri** og **Starfskraftur** séu stilltir á „Já“.

    [!NOTE]
    Ef þú stillir skiptihnappana **Eignir**, **Verkfæri** og **Starfskraftur** á „Nei“ verða núverandi frátekningar hunsaðar. Í upplýsingakladdanum verður listi yfir skörun á verkbeiðnum sýndur og hægt er að smella á skilaboðin til að opna verkbeiðni og endurskipuleggja, ef þess þarf.

5. Til að sjá ítarlegar upplýsingar um áætlunarferlið skaltu velja „Já“ á skiptihnappnum **Oflengd**. Þetta þýðir að nákvæmar upplýsingar um reiknuð stig á verkbeiðnunum og viðhaldsstarfsmenn verða sýnd í athugasemdakladda.

6. Smellið á **Í lagi** til að hefja röðunarferlið.

7. Þegar tímasetningu er lokið sýnir athugasemdakladdinn fjölda verkbeiðna og einnig ítarlegri upplýsingar ef skiptihnappurinn **Oflengd** var stilltur á „Já“.

>[!NOTE]
>Verkbeiðnir eru áætlaðar í einni lotu í hverri verkbeiðni, en ekki í hverju verkbeiðniverki. Þú getur einnig opnað gluggann **Tímasetja verkbeiðnir** beint í **Eignastjórnun** > **Reglubundið** > **Verkbeiðnir** > **Tímasetja verkbeiðnir**. Gerðu val þitt og smelltu á **Í lagi** til að hefja tímasetningu verkbeiðni. Það er mögulegt að setja upp tímasetningar verkbeiðni sem runuvinnslu í glugganum **Tímasetja verkbeiðnir** > flýtiflipanum **Keyra í bakgrunni**.

*Dæmi:* Á myndinni hér að neðan mun formúlan sem sett er inn í reitnum **Vænt upphaf** mynda tímasetningar verkbeiðna fyrir allar verkbeiðnir með áætlaðan upphafsdag eftir viku héðan í frá og síðar. Þessi formúla kann að vera gagnleg þegar þú keyrir tímasetningu verkbeiðni en þú vilt ganga úr skugga um að verkbeiðnum sem áætlaðar eru næstu 5-6 daga sé ekki endurraðað.

![Mynd 1](media/03-work-order-scheduling.png)

Gerð verkbeiðni sem tengist verkbeiðnunum getur sett upp tímasetningu fyrir einn viðhaldsstarfsmann (skiptihnappurinn **Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Gerðir verkbeiðna** > **Einn viðhaldsstarfsmaður** stilltur á „Já“). Þetta þýðir að ef tegund verkbeiðni er notuð í verkbeiðni er skiptihnappurinn **Einn viðhaldsstarfsmaður** sjálfkrafa stilltur á „Já“ á upplýsingasíðunni **Allar verkbeiðnir** > sýninni **Haus** > flýtiflipanum **Tímasetja**. Meðan á verkbeiðniröðun stendur verða öllum verkbeiðniverkum sem eru stofnuð í verkbeiðninni raðað á sama viðhaldsstarfsmann. Ef þess er þörf geturðu breytt valinu á skiptihnappnum **Einn viðhaldsstarfsmaður** í **Öllum verkbeiðnum** til að leyfa tímasetningu nokkurra starfsmanna eða eins starfsmanns í verkbeiðniverkunum.

Tímasetningarferlið í eignastjórnun inniheldur nokkra þætti í útreikningi tímasetningar:

- Reiknar út stig fyrir bæði verkbeiðnir og viðhaldsstarfsmenn. Stig fyrir verkbeiðnir og viðhaldsstarfsmenn eru sett upp í **Færibreytur eignastýringar**. 
- Leitaðu að samsvarandi færni, þ.e.a.s. færni og skírteina sem þarf til að framkvæma vinnsluna. Færni og skírteini eru sett upp á viðhaldsfólki í einingunni **Mannauður** (**Mannauður** > **Starfskraftar** > **Starfskraftar** > veldu starfsmann á listanum > flipanum **Starfskraftur** > kaflanum **Hæfni** > hnappnum **Færni** og **Skírteini**). Einnig er hægt að bæta færni og skírteini við tegundir viðhaldsverka og viðskipti með viðhaldsverk. Lestu meira um færni og gerðir viðhaldsverka í [Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Stig notuð við tímasetningu verkbeiðni

Útreikningur skora fyrir verkbeiðniverk byggist á áætluðum upphafsdegi og þjónustustigi verkbeiðninnar.

**Upphafsdagur** útreikningur: Fyrir hvern framtíðardag sem reiknuð er út frá áætluðum upphafsdegi er stigadagsetningin dregin frá og margfölduð með stiginu, sem er „10“ í dæmunum hér að neðan.

**Mikilvægi** útreikningur: Mikilvægisstig margfaldað með mikilvægi á verkbeiðni.

**Þjónustustig** útreikningur: Stigagjöf þjónustustigs deilt með þjónustustigi í verkbeiðni.

Í dæmunum hér að neðan er stigagjöfin „2“ og stig þjónustustiganna eru „5“ og „100“.

**Dæmi 1:**

| Auðkenni verkbeiðni | Væntanleg upphafsdagsetning | Mikilvægi verkbeiðni | Þjónustustig verkbeiðni | Útreikningur               | Einkunn      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Á morgun            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Eftir tvo daga   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Eftir tvo daga   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Verkbeiðnirnar verða áætlaðar í eftirfarandi röð: WO-000108 **16**, WO-000108 **18**, WO-000108 **17**.

**Dæmi 2:**

| Auðkenni verkbeiðni | Væntanleg upphafsdagsetning | Mikilvægi verkbeiðni | Þjónustustig verkbeiðni | Útreikningur                 | Einkunn    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Á morgun            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Eftir tvo daga   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Eftir tvo daga   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Ef stig stig þjónustunnar er hækkað í '100' í stað '5' verður tímasetningarröðin: WO-000108 **18**, WO-000108 **16**, WO-000108 **17**.

Matseinkunnir sem varða útreikning á því hvaða viðhaldsstarfsmenn ættu að vinna í verkbeiðnunum eru allar settar upp sem tölur, sem er bætt við hvern útreikning viðhaldsaðila við tímasetningu verkbeiðni. Viðhaldsstarfsmaðurinn með hæstu einkunn er valinn í verkbeiðninni. Hér er stutt lýsing á skorum starfsmanna viðhalds:

| Einkunn viðhaldsstarfskrafts| Lýsing |
|---|---|
| Ábyrgur starfskraftur | Ef viðhaldsstarfsmaður er valinn sem ábyrgur starfsmaður í verkbeiðninni er stiginu bætt við. |
| Hópur ábyrgra viðhaldsstarfskrafta | Ef viðhaldsstarfsmaður er hluti af ábyrgum viðhaldsstarfsmannahóp í verkbeiðninni er stiginu bætt við. |
| Æskilegur starfskraftur viðhalds         | Ef viðhaldsstarfsmaður er valinn sem forgangsstarfsmaður viðhalds á eigninni er stiginu bætt við. |
| Æskilegur hópur viðhaldsstarfskrafta   | Ef viðhaldsstarfsmaður er hluti af forgangsstarfsmannahóp viðhalds á eigninni er stiginu bætt við.  |
| Staðsetning  | Ef fyrirtæki þitt notar virkar staðsetningar fá viðhaldsstarfsmenn fulla einkunn ef þeir eru staðsettir á virkri staðsetningu sem tengist eigninni. Ef virk staðsetning eignarinnar hefur yfirstaðsetningu, þá fá viðhaldsstarfsmenn á þeirri virku staðsetningu 1/2 stig. Ef þessi staðsetning er einnig með yfireiningu fá viðhaldsstarfsmenn á þeim stað 1/3 stig. Ef þessi staðsetning er einnig með yfireiningu fá viðhaldsstarfsmenn á þeim stað 1/4 stig o.s.frv. Ef fyrirtækið notar eignastaðsetningu, sem við mælum ekki með, er staðsetning, landsvæði og svæði notað til að reikna staðsetningarskor. Starfsmenn fá fulla einkunn ef þeir eru staðsettir á staðsetningu og landsvæði og svæði sem tengjast eigninni. Ef staðsetning starfskrafts passar aðeins við staðsetningu og landsvæði er einkunnagjöf fyrir viðhaldsstarfsmanninn 2/3 af fullri einkunn. Ef staðsetning viðhaldsstarfsmanns passar aðeins við staðsetningu og landsvæði er einkunnagjöf fyrir viðhaldsstarfsmanninn 1/3 af fullri einkunn. |
| Fyrsti starfsdagur starfskrafts  | Fyrir hverja dagsetningu sem áætlaður upphafsdagur er síðar en væntur upphafsdagur er dregið frá stiginu.  |

>[!NOTE]
>Ef stig er stillt á „0“ er það stig ekki reiknað. Þetta er gagnlegt ef þú t.d. vilt ekki taka ábyrgan starfskraft inn í tímasetninguna.

## <a name="competencies-used-in-work-order-scheduling"></a>Færni notuð við tímasetningu verkbeiðni

Hægt er að setja upp hæfileika og vottorðskröfur um gerðir viðhaldsstarfa (**Eignastjórnun** > **Uppsetning** > **Vinnslur** > **Gerðir viðhaldsverka**) og viðskipti með viðhaldsverk (**Eignastjórnun** > **Uppsetning** > **Vinnslur** > **Viðskipti með viðhaldsverk**). 

Gerðir viðhaldsverka og viðskipti með viðhaldsverk eru valin á verkbeiðnaverkum. Ef færni eða skírteini hafa verið valin í gerð viðhaldsverka eða viðskiptum með viðhaldsverk og sú gerð viðhaldsverka eða viðskipti með viðhaldsverk eru notuð í verkbeiðniverki eru einungis viðhaldsstarfsmenn með samsvarandi færni og skírteini áætlaðir að vinna í verkbeiðninni.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Vinna með tímasettar vinnupantanir með gantt-grafi

**Gantt-graf áætlaðra vinnupantana** býður upp á myndrænt viðmót þar sem hægt er að skoða og enduráætla vinnupantanir.

Til að skoða og vinna með gantt-grafið:

1. Farðu í **Eignastýring > Vinnupantanir > Gantt-graf áætlaðra vinnupantana**.

1. Notaðu fellilistana og reitina í hlutanum **Stillingar** til að setja upp hvaða virku staðsetningu, tímabil og tímakvarða á að sýna í gantt-grafi.

1. Veljið **Bæta við**.

    - Gantt-grafið uppfærist til að sýna áætlaðar vinnupantanir sem passa við stillingarnar þínar. Hver vinnupöntun er sýnd með bláum ferhyrningi.
    - Til að enduráætla sýnda vinnupöntun skal velja hana og sleppa á nýja dagsetningu og tíma.

1. Ef þú gerðir einhverjar breytingar skaltu velja **Vista** á aðgerðasvæðinu til að vista þær.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]