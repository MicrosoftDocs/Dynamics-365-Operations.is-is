---
title: Keyra sérsniðnar X++ skriftur með engan niðurtíma
description: Þessi grein lýsir því hvernig á að hlaða upp og keyra dreifanlega pakka sem innihalda sérsniðnar X++ forskriftir án þess að þurfa að fresta kerfinu þínu.
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
ms.openlocfilehash: aad48fbd3ee2f28f39f6061b5e922f5c4f47c8f6
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103521"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Keyra sérsniðnar X++ skriftur með engan niðurtíma

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Þessi eiginleiki gerir þér kleift að hlaða upp og keyra dreifanlega pakka sem innihalda sérsniðnar X++ forskriftir án þess að þurfa að fara í gegnum Microsoft Dynamics Lifecycle Services (LCS) eða stöðva kerfið þitt. Þess vegna geturðu leiðrétt minniháttar ósamræmi í gögnum án þess að valda truflandi niður í miðbæ.

Ávinningurinn af því að nota X++ skriftu til að leiðrétta minniháttar ósamræmi í gögnum er að kerfið mun sjálfkrafa stilla allar tengdar töflur eftir þörfum þegar það keyrir skriftuna. Þessi nálgun hjálpar til við að tryggja heiðarleika leiðréttingarinnar og hjálpar til við að lágmarka hættuna á að koma upp nýju ósamræmi.

> [!IMPORTANT]
> Þessi eiginleiki er eingöngu ætlaður til að leiðrétta minniháttar ósamræmi í gögnum. Það má ekki nota í eftirfarandi tilgangi eða öðrum tilgangi:
>
> - Gagnasöfnun
> - Skipulagsbreytingar
> - Gagnaflutningur eða önnur langvinn ferli
> - Leiðrétting á gögnum sem hægt er að leiðrétta með öðrum hætti, svo sem venjulegum viðskiptaferlum, gagnasamræmisverkfærum eða öðrum sjálfsafgreiðsluverkfærum
>
> Eiginleikinn gerir viðurkenndum notendum kleift að breyta einingum og skrám þeirra beint, án þess að þurfa að keyra viðskiptarökfræðina sem tengist þessum aðilum. Þessar breytingar geta valdið gagnaheilleikavandamálum. Þess vegna gæti stofnun þín krafist þess að þú fáir samþykki og kvittun frá innri og ytri endurskoðendum (eða öðrum jafngildum hagsmunaaðilum) fyrir og/eða eftir að þú keyrir handrit. Af fylgniástæðum gæti einnig þurft að birta breytingar sem hafa áhrif á suma eiginleika í ytri skýrslum (svo sem reikningsskilum) eða tilkynna stjórnvöldum. Stofnunin þín ber ein ábyrgð á öllum breytingum sem gerðar eru á gögnum þess með þessum eiginleika, hvers kyns samþykki og undirritun eða birtingu þessara breytinga og samræmi við gildandi lög. Þú berð alla áhættuna af því að nota þennan eiginleika.

Allir dreifanlegir pakkar sem hlaðið er inn í kerfið fara í gegnum skyldubundið verkflæði. Sem öryggisráðstöfun, og til að tryggja aðskilnað starfa, er notandinn sem hleður upp pakka sem hægt er að nota, ekki leyft að samþykkja hann fyrir næstu skref í verkflæðinu. Annar notandi verður að samþykkja það. Hins vegar, eftir að pakkinn hefur verið samþykktur, mun notandinn sem hlóð honum upp hafa leyfi til að ljúka þeim skrefum sem eftir eru.

Kerfið krefst þess að allir pakkar sem hægt er að dreifa fari í gegnum prufukeyrslu. Áður en handritið verður leyft að keyra á framleiðslugögnum verður notandi að sannreyna að úttakið sé rétt með því að velja **Samþykkja prófunarskrá**. Ef úttakið er ekki rétt verður notandinn að merkja pakkann sem mistókst með því að velja **Að segja skilið við**. Í þessu tilviki verður handritið ekki leyft að keyra á framleiðslugögnum.

Sérhver pakki sem hlaðið er upp er vistaður í kerfinu og fer í gegnum skilgreint verkflæði atburða. Fyrir hvern atburð heldur kerfið skrá sem inniheldur tímastimpil og auðkenni þess sem framkvæmdi atburðinn. Þannig tryggir kerfið að til sé endurskoðunarslóð.

Eins og eftirfarandi mynd sýnir gefur kerfið upplýsingar um hvernig hver pakki sem hægt er að dreifa var keyrður í X++ og hvaða einingar voru snertar.

![Upplýsingasíða handrits.](media/script-details.png "Upplýsingasíða handrits")

## <a name="assign-duties-to-users-to-control-access"></a>Úthlutaðu skyldum til notenda til að stjórna aðgangi

Þessi eiginleiki veitir eftirfarandi skyldur. Stjórnendur geta notað þessar skyldur til að hjálpa til við að stjórna aðgangi að eiginleikanum.

- **Halda sérsniðnum forskriftum** - Þessi skylda veitir getu til að hlaða upp, prófa, sannreyna og keyra sérsniðnar X++ forskriftir í umhverfi (samþykkisprófun notenda\[ UAT\] og framleiðslu).
- **Samþykkja sérsniðnar forskriftir** – Þessi skylda veitir möguleika á að samþykkja sérsniðið X++ forskrift sem hlaðið er upp. Samþykki er nauðsynlegt skref áður en hægt er að prófa, sannreyna og keyra nokkurt handrit.

Til að hjálpa til við að lágmarka hættuna á skaðlegum aðgerðum verður hvert smáforrit að vera sérstaklega samþykkt af öðrum notanda en notandanum sem hlóð því upp. Áður en þú getur notað þennan eiginleika í fyrirtækinu þínu verður stjórnandi að úthluta fyrri skyldum til að minnsta kosti tveggja viðeigandi og mjög traustra notenda. Þó að einn notandi geti haft báðar skyldur, mun sá notandi samt ekki geta samþykkt eigin forskriftir.

## <a name="create-a-deployable-package"></a>Virkjanlegur pakki búinn til

Eiginleikinn krefst venjulegs dreifanlegs pakka sem hægt er að búa til í Visual Studio. Fyrir leiðbeiningar, sjá [Búðu til dreifanlega pakka af gerðum](../deployment/create-apply-deployable-package.md).

Dreifanlegur pakki þinn verður að innihalda nákvæmlega einn keyranlegan X++ flokk. Með öðrum orðum, það verður að hafa einn flokk sem inniheldur aðferð sem hefur eftirfarandi undirskrift.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Heiti aðalaðferðarinnar verður að vera lágstöfum.

## <a name="code-example"></a>Dæmi um kóða

Eftirfarandi kóðadæmi sýnir hvernig hægt er að byggja upp dreifanlegan pakka.

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

Eftirfarandi listi lýsir nokkrum bestu starfsvenjum til að skrifa, innleiða og keyra handrit með góðum árangri. Listinn er ekki tæmandi og ætti að líta á hann sem leiðbeiningar.

- **Gerðu** skrifaðu árangursskilaboð í lok handritsins. Þannig muntu geta séð að handritið keyrði án undantekninga.
- **Gerðu** bæta við skýrri meðferð á umfangi viðskipta.
- **Gerðu** nota núverandi viðskiptarökfræði, svo sem`update()` aðferðir, en **ekki gera** framhjá viðskiptarökfræði með því að nota`doUpdate()`,`doInsert()`, og`doDelete()` aðferðir. Þessi nálgun mun hjálpa til við að tryggja að háð gögn séu meðhöndluð á réttan hátt. Það mun einnig draga verulega úr hættu á frekari ósamræmi í gögnum.
- **Gerðu** halda fram samhengi fyrirtækisins. Þessi nálgun mun afhjúpa algeng mistök þegar handrit keyrir. Til dæmis mun það leiða í ljós hvort handritið sé keyrt í röngum fyrirtæki.
- **Gerðu** fullyrtu að fjöldi skráðra skráa samsvari væntingum þínum. Þessi nálgun mun leiða í ljós hvort gögn hafi breyst óvænt í kerfinu á meðan verið var að undirbúa handritið.
- **Gerðu** nota einstök flokksheiti fyrir hvert handrit (til dæmis með því að setja tilvísun í verkþátt í nafninu). Þessi aðferð kemur í veg fyrir vandamál með nafnaskil þegar þú hleður upp handritinu. Ef þörf er á nýrri endurtekningu á handriti, vertu viss um að gefa því nýtt nafn.
- **Gerðu** prófaðu hvert handrit fyrst í umhverfi sem ekki er framleiðslu. Prófaðu fyrir ætluð áhrif og fyrir óviljandi aukaverkanir á tengd gögn. Gakktu úr skugga um að hægt sé að ljúka öllum viðskiptaferlum sem gætu orðið fyrir áhrifum með góðum árangri og að fullu á eftir.

## <a name="upload-and-run-a-deployable-package"></a>Hladdu upp og keyrðu pakka sem hægt er að nota

Notaðu eftirfarandi aðferð til að hlaða upp og keyra skriftu.

1. Í fjármála- og rekstrarappinu þínu skaltu fara á **Kerfisstjórnun \> Reglubundin verkefni \> Gagnagrunnur \> Sérsniðin forskrift**.
1. Veldu **Hlaða upp**.
1. Veldu dreifanlega pakkann sem þú bjóst til eins og lýst er fyrr í þessari grein. Þú verður beðinn um að tilgreina tilgang handritsins.
1. Handritið verður nú að vera samþykkt af öðrum notanda en notandanum sem hlóð því upp. Samþykkjandinn verður að fylgja þessum skrefum:

    1. Fara til **Kerfisstjórnun \> Reglubundið \> Gagnagrunnur \> Sérsniðin forskrift**.
    1. Veldu handritið til að samþykkja og veldu síðan **Upplýsingar**.
    1. Á aðgerðarrúðunni, á **Vinnuflæði ferli** flipa, í **Byrjaðu** hópur, veldu **Samþykkja** eða **Hafna**. Ef þú velur **Samþykkja**, handritið er merkt sem samþykkt og er opnað fyrir prófun. Ef þú velur **Hafna**, handritið er læst. Í báðum tilfellum er atburðurinn skráður og afrit af handritinu geymt í kerfinu.

1. Forritið verður að prófa til að tryggja að það geri það sem því er ætlað að gera. Prófandinn getur verið sá sami og hleðsluaðilinn eða samþykkjandinn, eða það getur verið þriðji notandinn sem hefur tilskilin leyfi. Prófandi verður að fylgja þessum skrefum:

    1. Fara til **Kerfisstjórnun \> Reglubundið \> Gagnagrunnur \> Sérsniðin forskrift**.
    1. Veldu skriftuna til að prófa og veldu síðan **Upplýsingar**.
    1. Á aðgerðarrúðunni, á **Vinnuflæði ferli** flipa, í **Próf** hópur, veldu **Keyra próf**. Forskriftin er keyrð í tímabundinni færslu sem kerfið mun sjálfkrafa hætta við á meðan það safnar ýmsum annálum og SQL yfirlýsingum.
    1. Þegar handritinu er lokið skaltu fara yfir annálana og ganga úr skugga um að niðurstöðurnar standist væntingar þínar. Fylgið einu af eftirfarandi skrefum:

        - Ef þú ert ánægður með niðurstöðuna skaltu velja **Samþykkja prófunarskrá** í **Próf** hópur á **Vinnuflæði ferli** flipanum í aðgerðarrúðunni til að leyfa að keyra skriftuna. Atburðaskráin mun endurspegla þá staðreynd að handritið var prófað og það mun gefa til kynna hver prófaði það og hvenær.
        - Ef þú ert ekki ánægður með niðurstöðuna skaltu velja **Að segja skilið við** í **Enda** hópur á **Vinnuflæði ferli** flipanum í aðgerðarrúðunni til að koma í veg fyrir að handritið sé keyrt. Kerfið mun geyma afrit af handritinu ásamt skrá yfir sögu þess.

1. Þegar þú ert viss um að handritið standist væntingar þínar skaltu velja **Hlaupa** í **Hlaupa** hópur á **Vinnuflæði ferli** flipann í aðgerðarrúðunni til að keyra hann. Þessi skipun gerir það sama og fyrri prófun, en viðskiptin verða framin í lokin.
1. Eftir að handritið hefur lokið keyrslu skaltu athuga niðurstöðuna og staðfesta að handritið virkaði eins og þú ætlaðir þér. Fylgið einu af eftirfarandi skrefum:

    - Ef þú ert ánægður með niðurstöðuna skaltu velja **Tilgangur leystur** í **Enda** hópur á **Vinnuflæði ferli** flipanum í aðgerðarrúðunni. Atburðaskráin mun endurspegla þá staðreynd að handritið keyrði vel og það mun gefa til kynna hver staðfesti handritið og hvenær. Handritið er vistað en það er nú læst og ekki hægt að keyra það aftur.
    - Ef þú ert ekki ánægður með niðurstöðuna skaltu velja **Tilgangur óleystur** í **Enda** hópur á **Vinnuflæði ferli** flipanum í aðgerðarrúðunni. Atburðaskráin mun endurspegla þá staðreynd að handritið náði ekki tilætluðum tilgangi sínum og mun gefa til kynna hver keyrði handritið og hvenær. Handritið er vistað en það er nú læst og ekki hægt að keyra það aftur. Hins vegar afturkallar kerfið ekki handritsaðgerðina sjálfkrafa. Þú gætir þurft að skrifa, flytja inn og keyra nýtt forskrift til að afturkalla áhrifin sem misheppnuð forskrift hafði á kerfið þitt.

Val þitt í síðasta skrefi skilgreinir lokastöðu handritsins. Þú getur endurtekið ferlið eins og þú vilt.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Hladdu upp og keyrðu dreifanlegan pakka í gegnum LCS

Í stað þess að dreifa pakkanum þínum í gegnum notendaviðmótið fyrir fjármála- og rekstrarforritið þitt, eins og lýst er í fyrri hlutanum, geturðu hlaðið honum upp á LCS og notað venjulegt ferli til að dreifa því. Fyrir frekari upplýsingar, sjá [Settu upp dreifanlega pakka frá skipanalínunni](../deployment/install-deployable-package.md).

Þrátt fyrir að þessi aðferð hafi færri takmarkanir veitir hún minni villuvörn. Þar að auki, vegna þess að það krefst endurræsingar á öllum netþjónum, mun það valda smá niður í miðbæ.

