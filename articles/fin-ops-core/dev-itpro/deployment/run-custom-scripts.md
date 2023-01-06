---
title: Keyra sérsniðnar X++ skriftur með engan niðurtíma
description: Þessi grein útskýrir hvernig á að hlaða upp og keyra virkjanlega pakka sem innihalda sérsniðnar X++ forskriftir án þess að setja kerfið í bið.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 3d00f842da69f889738fbcb293c7489bb018e810
ms.sourcegitcommit: f62c9b24c2205d03e2fd6e7c67f7b5c316233b12
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2022
ms.locfileid: "9598083"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Keyra sérsniðnar X++ skriftur með engan niðurtíma

[!include [banner](../includes/banner.md)]

Þessi eiginleiki gerir þér kleift að hlaða upp og keyra virkjanlega pakka sem innihalda sérsniðnar X++ forskriftir án þess að fara í gegnum Microsoft Dynamics Lifecycle Services (LCS) eða setja kerfið í bið. Þess vegna er hægt að leiðrétta minniháttar ósamræmi í gögnum án þess að það valdi verulegum niðurtíma.

Kosturinn við að nota X++ forskriftir til að leiðrétta minniháttar ósamræmi í gögnum er sá að kerfið leiðréttir sjálfkrafa allar tengdar töflur eins og þörf er á þegar það keyrir forskriftina. Þessi aðferð hjálpar til við að tryggja heilleika leiðréttingarinnar og dregur úr hættu á nýju ósamræmi.

> [!IMPORTANT]
> Þessi eiginleiki er eingöngu ætlaður til leiðréttingar á minniháttar ósamræmi gagna. Ekki má nota þetta í eftirfarandi tilgangi eða í öðrum tilgangi:
>
> - Gagnasöfnun
> - Breytingar á skemum
> - Gagnaflutningur eða önnur ferli sem hafa verið lengi í vinnslu
> - Leiðrétting á gögnum sem hægt er að leiðrétta með öðrum leiðum, svo sem reglulegum viðskiptaferlum, gagnasamræmisverkfærum eða öðrum sjálfsafgreiðsluverkfærum
>
> Eiginleikinn gerir viðurkenndum notendum kleift að breyta einingum og færslum þeirra beint án þess að keyra viðskiptagrunninn sem tengist þessum einingum. Þessar breytingar geta valdið vandamálum varðandi heilleika gagna. Þess vegna gæti fyrirtækið þitt farið fram á að þú fáir samþykki og undirskrift frá innri og ytri endurskoðendum (eða öðrum sambærilegum hagsmunaaðilum) fyrir og/eða eftir að forskriftin hefur verið keyrð. Af reglufylgniástæðum gæti þurft að taka fram breytingar sem hafa áhrif á sum einkenni í ytri skýrslum (t.d. fjárhagsskýrslum) eða tilkynna yfirvöldum um þær. Fyrirtækið ber alfarið ábyrgð á öllum breytingum sem gerðar eru á gögnum þess með þessum eiginleika, samþykki, undirritun eða birtingu þeirra og að farið sé eftir gildandi lögum. Þú berð alla áhættuna af því að nota þennan eiginleika.

Allir virkjanlegir pakkar sem hlaðnir eru upp í kerfið fara í gegnum áskilið verkflæði. Til öryggis og til að tryggja aðskilnað á skyldum er notanda sem hleður upp virkjanlegum pakka ekki heimilt að samþykkja hann fyrir næstu skref í verkflæðinu. Annar notandi verður að samþykkja það. Eftir að pakkinn hefur verið samþykktur fær notandinn sem hlóð honum upp hins vegar að ljúka þeim skrefum sem eftir eru.

Kerfið krefst þess að allir virkjanlegir pakkar fari í gegnum prufukeyrslu. Áður en forskriftin fær að keyra á framleiðslugögnum verður notandi að staðfesta að úttakið sé rétt með því að velja **Samþykkja prufukladda**. Ef útkoman er ekki rétt verður notandinn að merkja pakkann sem misheppnaðan með því að velja **Yfirgefa**. Í þessu tilfelli er forskriftinni ekki leyft að keyra á framleiðslugögnum.

Allir pakkar sem hlaðið er upp eru vistaðir í kerfinu og fara í gegnum skilgreint verkflæði viðburða. Fyrir hvern viðburð heldur kerfið skrá með tímastimpli og auðkenni þess sem framkvæmdi viðburðinn. Þannig tryggir kerfið að slóð færslna sé til staðar.

Eins og eftirfarandi mynd sýnir veitir kerfið upplýsingar um hvernig hver virkjanlegur pakki var keyrður í X++ og hvaða einingar voru snertar.

![Upplýsingasíða forskriftar.](media/script-details.png "Upplýsingasíða forskriftar")

## <a name="assign-duties-to-users-to-control-access"></a>Úthluta skyldum til notenda til að stýra aðgangi

Þessi eiginleiki veitir eftirfarandi skyldur. Kerfisstjórar geta notað þessar skyldur til að stýra aðgangi að eiginleikanum.

- **Vinna með sérsniðnar forskriftir** – Þessi aðgangsheimild veitir getu til að hlaða upp, staðfesta og keyra sérsniðnar X++ forskriftir í umhverfum (samþykkisprófun notanda \[UAT\] og framleiðsla).
- **Samþykkja sérsniðnar forskriftir** – Þessi aðgangsheimild veitir getu til að samþykkja sérsniðna X++ forskrift sem hlaðið hefur verið upp. Samþykki er nauðsynlegt skref áður en hægt er að prófa, staðfesta og keyra hvaða skriftu sem er.

Til að lágmarka hættu á skaðlegum aðgerðum verður hver skrifta að vera sérstaklega samþykkt af öðrum en þeim sem hlóð henni upp. Áður en hægt er að nota þennan eiginleika í fyrirtækinu verður stjórnandi að úthluta áðurnefndum aðgangsheimildum á að minnsta kosti tvo viðeigandi og trausta notendur. Þótt einn notandi getið verið með báðar aðgangsheimildirnar getur sá notandi samt ekki samþykkt sínar eigin forskriftir.

## <a name="create-a-deployable-package"></a>Virkjanlegur pakki búinn til

Eiginleikinn krefst venjulegs virkjanlegs pakka sem hægt er að búa til í Visual Studio. Leiðbeiningar eru í [Stofna virkjanlega pakka af líkönum](../deployment/create-apply-deployable-package.md).

Virkjanlegi pakkinn verður að innihalda nákvæmlega einn X++ klasa sem hægt er að keyra. Í öðrum orðum verður hann að vera með einn klasa sem inniheldur aðferð sem er með eftirfarandi undirskrift.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Heiti aðalaðferðarinnar verður að vera með litlum staf.

## <a name="code-example"></a>Kóðadæmi

Eftirfarandi dæmi um kóða sýnir hvernig virkjanlegur pakki er skipulagður.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Bestu venjur

Eftirfarandi listi lýsir nokkrum bestu aðferðum við að skrifa, framkvæma og keyra skriftu. Listinn er ekki tæmandi og hann ætti aðeins að vera til leiðbeiningar.

- **Skrifið** skilaboð um árangur við lok forskriftarinnar. Þannig er hægt að sjá að skrifta keyrði án undantekninga.
- **Bætið** við sérstakri meðhöndlun á umfangi færslunnar.
- **Nota** skal fyrirliggjandi viðskiptagrunn, t.d. `update()` aðferðir, en **ekki** fara framhjá viðskiptagrunni með því að nota `doUpdate()`, `doInsert()` og `doDelete()` aðferðir. Þessi aðferð hjálpar til við að tryggja að rétt sé farið með háð gögn. Það mun einnig draga verulega úr hættunni á frekari ósamræmi gagna.
- **Staðfestið** samhengi fyrirtækisins. Þessi aðferð mun birta algeng mistök þegar forskrift keyrir. Til dæmis mun það leiða í ljós hvort skriftan sé keyrð í röngu fyrirtæki.
- **Fullvissaðu** þig um að fjöldi færslna sem var breytt sé í samræmi við væntingar þínar. Þessi aðferð mun leiða í ljós hvort gögn færðust óvænt til í kerfinu á meðan forskriftin var undirbúin.
- **Nota** skal einkvæmt klasaheiti fyrir hverja forskrift (til dæmis með því að hafa með tilvísun í vinnuatriði í heitinu). Þessi aðferð kemur í veg fyrir árekstra við heiti þegar þú hleður upp forskriftinni. Ef þörf er á nýrri endurtekningu skriftu skal gefa henni nýtt heiti.
- **Prófið** hverja forskrift í fyrst í umhverfi sem ekki er fyrir framleiðslu. Prófaðu ætluð áhrif og fyrir óvæntum hliðarverkunum á tengdum gögnum. Gættu þess að hægt sé að klára eftir á alla viðskiptaferla sem kunna að verða fyrir áhrifum.

## <a name="upload-and-run-a-deployable-package"></a>Hlaða upp og keyra virkjanlegan pakka

Notið eftirfarandi ferli til að hlaða upp og keyra forskrift.

1. Í forriti fjármála- og reksturs skal fara í **Kerfisstjórnun \> Reglubundin verk \> Gagnagrunnur \> Sérsniðnar forskriftir**.
1. Veldu **Hlaða upp**.
1. Veldu virkjanlega pakkanna sem þú bjóst til eins og lýst var fyrr í þessari grein. Beðið verður um að þú tilgreinir tilgang skriftunnar.
1. Nú verður annar notandi en notandinn sem hlóð forskriftinni upp að samþykkja hana. Samþykkjandi verður að fylgja þessum skrefum:

    1. Opnið **Kerfisstjórnun \> Reglubundin \> Gagnagrunnur \> Sérsniðnar forskriftir**.
    1. Veljið forskriftina til að samþykkja og svo **Upplýsingar**.
    1. Á aðgerðasvæðinu, í flipanum **Vinna úr verkflæði**, í flokknum **Byrja**, skal velja **Samþykkja** eða **Hafna**. Ef þú velur **Samþykkja** er skriftan merkt sem samþykkt og er opin til prufu. Ef þú velur **Hafna** er forskriftin læst. Í báðum tilvikum er atburðurinn skráður inn og afrit af forskriftinni er geymt í kerfinu.

1. Prófa þarf forskriftina til að tryggja að hún geri það sem til er ætlast. Prófunaraðilinn getur verið sá sami og sá sem hlóð efninu upp eða sá sem veitir samþykki eða hann getur verið þriðji notandi sem hefur tilskildar heimildir. Próftaki verður að fylgja þessum skrefum:

    1. Opnið **Kerfisstjórnun \> Reglubundin \> Gagnagrunnur \> Sérsniðnar forskriftir**.
    1. Veljið forskrift til að prófa og svo velja **Upplýsingar**.
    1. Á aðgerðasvæðinu, í flipanum **Vinna úr verkflæði**, í flokknum **Prófa**, skal velja **Keyra prófun**. Forskriftin er keyrð innan í tímabundinni færslu sem kerfið mun sjálfkrafa hætta við þegar það safnar ýmsum klöddum og SQL-yrðingum.
    1. Þegar forskriftin er hætt að keyra skal yfirfara kladdana og staðfesta að niðurstöðurnar uppfylli væntingar. Fylgið einu af eftirfarandi skrefum:

        - Ef prófniðurstöðurnar eru fullnægjandi skal velja **Samþykkja prufukladda** í hópnum **Prófun** í flipanum **Vinna úr verkflæði** á aðgerðasvæðinu til að leyfa forskriftinni að keyra. Viðburðarkladdinn mun endurspegla þá staðreynd að forskriftin var prófuð og hann mun sýna hver prófaði hana og hvenær.
        - Ef prófniðurstöðurnar eru ekki fullnægjandi skal velja **Hætta** í hópnum **Ljúka** í flipanum **Vinna úr verkflæði** á aðgerðasvæðinu til að koma í veg fyrir að forskriftin verði keyrð. Kerfið mun geyma afrit af forskriftinni saman með kladda yfir feril hennar.

1. Þegar þú ert viss um að forskriftin uppfylli væntingar skal velja **Keyra** í hópnum **Keyra** í flipanum **Vinna úr verkflæði** á aðgerðasvæðinu til að keyra hana. Þessi skipun gerir það sama og fyrri prufukeyrsla en færslan verður skráð í lokin.
1. Eftir að forskriftin er hætt að keyra skal athuga niðurstöðuna og staðfesta að forskriftin virkaði sem skyldi. Fylgið einu af eftirfarandi skrefum:

    - Ef niðurstaðan er fullnægjandi skal velja **Tilgangur leystur** í hópnum **Ljúka** í flipanum **Vinna úr verkflæði** á aðgerðasvæðinu. Viðburðarkladdinn mun endurspegla þá staðreynd að forskriftin hafi náð að keyra og hann mun sýna hver staðfesti forskriftina og hvenær. Forskriftin er vistuð en hún er nú læst og ekki hægt að keyra hana aftur.
    - Ef niðurstaðan er ekki fullnægjandi skal velja **Tilgangur óleystur** í hópnum **Ljúka** í flipanum **Vinna úr verkflæði** á aðgerðasvæðinu. Viðburðarkladdinn mun endurspegla þá staðreynd að forskriftin hafi mistekist að uppfylla ætlaðan tilgang og hann mun sýna hver keyrði forskriftina og hvenær. Forskriftin er vistuð en hún er nú læst og ekki hægt að keyra hana aftur. Kerfið afturkallar hins vegar ekki sjálfkrafa forskriftaraðgerðina. Hugsanlega þarftu að skrifa, flytja inn og keyra nýja forskrift til að draga til baka þau áhrif sem misheppnaða forskriftin hafði á kerfið þitt.

Valið í síðasta skrefinu skilgreinir endanlegt ástand fyrir skriftuna. Þú mátt endurtaka ferlið eins og þú krefst.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Hlaða upp og keyra virkjanlegan pakka í gegnum LCS

Í stað þess að setja upp virkjanlegan pakka í gegnum notendaviðmótið fyrir forrit fjármála- og reksturs, eins og lýst er í hlutanum hér á undan, er hægt að hlaða hann upp í LCS og nota hefðbundið ferli til að setja hann upp. Frekari upplýsingar eru í [Setja upp virkjanlega pakka úr skipanalínunni](../deployment/install-deployable-package.md).

Þótt þessi nálgun sé með færri takmarkanir er ekki eins mikil vernd gegn villum. Þar að auki, vegna þess að það krefst endurræsingar á öllum þjónum, mun það valda nokkrum biðtíma.

