---
title: Fyrirbyggjandi gæðauppfærslur
description: Þessi grein veitir upplýsingar um fyrirbyggjandi afhendingu gæðauppfærslna.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338137"
---
# <a name="proactive-quality-updates"></a>Fyrirbyggjandi gæðauppfærslur

[!include[banner](../includes/banner.md)]

Á undanförnum árum hefur Microsoft náð stöðugum framförum í því sem við vísum til sem [Ein útgáfa](../../dev-itpro/lifecycle-services/oneversion-overview.md). Forsenda One Version er einföld: því nær sem við komumst að hafa alla viðskiptavini á sömu hugbúnaðarútgáfu, því meiri gæði sem við getum skilað. Við finnum og lagum vandamál einu sinni og við fáum þessar lausnir í hendur fleiri viðskiptavina hraðar.

Þessi forsenda er staðfest af niðurstöðunum: lægri atvikafjöldi á vörum okkar. Þegar viðskiptavinir eru ekki á sömu útgáfu, sjáum við stöðugt að þeir verða fyrir áhrifum af vandamálum sem lausn er þegar tiltæk fyrir. Við höfum þegar náð miklum framförum með Dynamics 365 Finance, Dynamics 365 Supply Chain,Dynamics 365 Project Operations, og Dynamics 365 Commerce, og þökk sé nýlegum tækniframförum er nú hægt að taka næsta skref. Eftirfarandi upplýsingar segja til um hvað við ætlum að gera, hvað við höfum þegar gert til að setja sviðið og hvernig og hvenær við munum kynna nýja möguleikana án truflana.

## <a name="focus-on-quality-updates"></a>Einbeittu þér að gæðauppfærslum

Við útvegum nú sjö [þjónustuuppfærslur](public-preview-releases.md) hvert ár. Til dæmis er útgáfa 10.0.29 þjónustuuppfærsla. Þar til nýlega voru átta uppfærslur á ári. Hins vegar slepptum við einni uppfærslu til að bregðast við athugasemdum viðskiptavina sem sýndu löngun til að forðast breytingar undir lok almanaksársins.

Við munum ekki breyta hraðauppfærslum þjónustunnar. Þess í stað er lögð áhersla á næsta skref okkar fram á við í One Version ferðinni *gæðauppfærslur*. Gæðauppfærslur eru uppsafnaðar uppbyggingar af flýtileiðréttingum. Þeir innihalda ekki nýja eiginleika. Á hverjum tíma dreifist allt samfélag viðskiptavina okkar á milli þriggja eða fjögurra nýjustu þjónustuuppfærslna. Hins vegar, fyrir hverja tiltekna þjónustuuppfærslu, er hægt að nota heilmikið af mismunandi gæðauppfærsluútgáfum innan hópsins, allt eftir dagsetningum þegar fólk fór á vettvang. Í næsta skrefi okkar munum við senda út gæðauppfærslur fyrirbyggjandi. Við notum nú þegar þetta líkan fyrir okkar Dataverse -undirstaða forrita og hafa séð væntanlegan árangur af bættum gæðum og minni stuðningsatvikum.

Auðvitað gæti minnkun á göllum dregið úr eða algjörlega eytt þörfinni á gæðauppfærslum. Við erum með mörg frumkvæði á flugi til að draga úr göllum sem krefjast gæðauppfærslu. Jafnvel þegar hleðsla minnkar í gæðauppfærslunni mun samkvæmni þvert á viðskiptavinahópinn bæta stuðning, fá endurbætur til viðskiptavina hraðar og draga úr tíðni viðskiptavina sem lenda í vandamálum sem lausnir eru þegar til fyrir.

## <a name="making-proactive-distribution-possible"></a>Gerir fyrirbyggjandi dreifingu mögulega

Margar framfarir hafa þegar verið settar í notkun sem gera kleift að senda gæðauppfærslur fyrirbyggjandi:

- **Nánast núll uppfærsla á niðritíma** – Til að ýta undir tíðari umhverfi er nauðsynlegt að draga úr áhrifum á aðgengi umhverfisins til að varðveita Dynamics 365 Service Level Agreements (SLAs). Uppfærsla á næstum núlli niður í miðbæ var upphaflega kynnt til að hjálpa til við að bæta mánaðarlega lagfæringu stýrikerfis með því að nota þyrpingabilun til að virkja uppfærðu myndina með lágmarks truflun. Verið er að bæta vélbúnaðinn til að beita uppfærslum þannig að hann truflar enn minna og mun ná yfir bæði stýrikerfisuppfærslur og gæðauppfærsluuppfærslu.

    Fyrir gagnvirka notendur gæti virk lota verið rofin og tilraunin fer aftur í uppfært umhverfi. Með tilkomu [forgangstengd lotuáætlun](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), sem er nú fáanlegt á grundvelli opt-in, bata tímasetningu og vinnsla bata og halda áfram strax eftir uppfærsluna. Forgangsbundin lotuáætlun verður til staðar fyrir viðskiptavini áður en þeir byrja að taka þátt í fyrirbyggjandi dreifingu á gæðauppfærslum fyrir framleiðsluumhverfi þeirra.

- **Myrkra tímar** – Myrkratímar eru skilgreindir fyrir hvert Azure svæði og uppfærslur á niðritíma næstum núll munu eiga sér stað á myrkutímatímabilinu.

## <a name="the-proactive-update-process"></a>Fyrirbyggjandi uppfærsluferlið

Dreifing fyrirbyggjandi gæðauppfærslu mun fylgja öruggu dreifingarferli (SDP). Sérkenni SDP munu þróast, en gæðauppfærslur verða upphaflega settar í sandkassaumhverfi. Ferlið mun byrja með umhverfi sem opnar fyrir snemmtæka dreifingu. Eftir því sem hlutfall sandkassa sem tókst að dreifa eykst mun dreifing í framleiðsluumhverfi hefjast. Enn og aftur mun ferlið byrja með umhverfi sem opnar fyrir snemmtæka dreifingu. Hlustunarkerfi munu fylgjast með kerfisfjarmælingum og atvikum á Livesite og munu stöðva útsetningu ákveðinnar útgáfu ef einhver afturför greinist. Viðskiptavinir munu samt geta dregið gæðauppfærslurnar á undan fyrirbyggjandi dreifingu ef þeir vilja.

Núverandi útgáfustjórnunargögn sýna að minna en 3 prósent af afturköllun eru kynnt í gæðauppfærslum. Með aukinni áherslu á að útrýma afturhvarfi og aukinni SDP verða hugsanleg áhrif afturhvarfs verulega minni en gæðahagnaðurinn sem næst með því að fá lagfæringar hraðar til viðskiptavina víða.

## <a name="process-changes"></a>Breytingar á ferli

Verið er að innleiða sett af ferlibreytingum fyrir virkjun á fyrirbyggjandi gæðauppfærsluuppfærslu:

- **Skema** – Verkfæri munu tryggja að gæðauppfærslur innihalda aðeins skemabreytingar sem hægt er að beita á meðan þjónustan er á netinu. Þessi nálgun mun hjálpa til við að viðhalda getu til að beita uppfærslunni með næstum núlli niður í miðbæ.
- **Aukið eftirlit með breytingum** – Eins og er, er nú þegar aukaferlisskref til að samþykkja breytingar fyrir innlimun í gæðauppfærslu. Athugunin í aukaskrefinu verður aukin til að draga úr möguleikum á afturförum. Brotandi breytingar eru ekki leyfðar í gæðauppfærslum og aukin athugun á breytingum mun hjálpa til við að tryggja að við náum þessu markmiði.
- **Skyggni** - Við munum senda tilkynningar í gegnum tölvupóst og Lifecycle Services (LCS) fyrir komandi fyrirbyggjandi gæðauppfærslur. Að auki munu stuðningsteymi og atviksleiðir hafa sýnilegt hvar gæðauppfærslur hafa verið settar á fyrirbyggjandi hátt.
- **Til baka útgáfu** – Flug verður notað til að flokka allar breytingar í fyrirbyggjandi gæðauppfærslu. Ef þörf er á fallback eftir fyrirbyggjandi dreifingu er hægt að gera það í gegnum flugkerfið.
- **Samstillingarheiti fyrir sandkassa** - Innan við 20 prósent viðskiptavina í dag eru með marga sandkassa og halda einum sandkassa uppbyggðum þar sem útgáfan passar við framleiðslu, til að hjálpa við bilanaleit. Í náinni framtíð munum við kynna möguleika viðskiptavina til að tilgreina sandkassaumhverfi sem ætti ekki að fá fyrirbyggjandi gæðauppfærsluuppfærslu ásamt öðrum sandkassa, en það ætti þess í stað að fá það síðar ásamt framleiðsluumhverfinu. Athugaðu að ef viðskiptavinur notar sandkassa til að prófa nýrri útgáfu en framleiðslu hans mun sá sandkassi fá gæðauppfærslur á nýrri útgáfuna.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Hvenær byrja fyrirbyggjandi gæðauppfærslur?

Búist er við að dreifing á fyrirbyggjandi gæðauppfærslum fyrir sandkassaumhverfi hefjist seint í september eða október 2022 fyrir viðskiptavini Azure almenningsskýja. Reynsluumhverfi munu einnig byrja að fá fyrirbyggjandi uppfærsluuppfærslu á þeim tíma. Í september verður tilkynning send til hvers viðskiptavinar til að upplýsa þá um væntanlega tímaáætlun fyrir umhverfi sitt. Undantekningar frá fyrirbyggjandi uppfærðu dreifingarferli verða aðeins leyfðar fyrir viðskiptavini sem eru undir eftirliti FDA. Við erum enn að vinna úr því hvernig stjórnað umhverfi og skýjaviðskiptavinum ríkisins og stjórnvalda verður stjórnað.

Á næsta sex mánaða tímabili munum við smám saman auka hlutfall sandkassaumhverfa sem fá fyrirbyggjandi uppfærslur, þar til öll tilnefnd umhverfi eru tekin með og framfarir í að uppfæra framleiðsluumhverfi. Allt tímabilið munum við fylgjast með til að tryggja að dreifingarferlið sé óaðfinnanlegt og að við séum að ná markmiði okkar um hleðslu sem ekki truflar.

Vegna þess að viðskiptavinir munu reglulega fá minni hleðslu, gerum við ráð fyrir því að ferlið við að vera núverandi verði einfaldara. Við munum breyta tíðni uppfærsluuppfærslu þegar við sýnum getu til að keyra ferlið án truflana. Þetta ferli er nú þegar að virka á áhrifaríkan hátt fyrir okkar Dataverse vettvang og forrit, og er að skila væntanlegum framförum í þjónustugæðum. Okkur langar til að stíga sama skref fram á við fyrir umsóknir um fjármál og rekstur.
