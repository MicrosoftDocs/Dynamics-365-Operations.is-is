---
title: Fyrirbyggjandi gæðauppfærslur
description: Þessi grein veitir upplýsingar um fyrirbyggjandi afhendingu gæðauppfærslna.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 60f9d84b240016671ff726fc3cca2e02cfd811ca
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689225"
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

- **Nánast núll uppfærsla á niðritíma** – Til að ýta undir tíðari umhverfi er nauðsynlegt að draga úr áhrifum á aðgengi umhverfisins til að varðveita Dynamics 365 Service Level Agreements (SLAs). Uppfærsla á næstum núlli niður í miðbæ var upphaflega kynnt til að bæta mánaðarlega lagfæringu stýrikerfis með því að nota cluster failover til að virkja uppfærðu myndina með lágmarks röskun. Verið er að bæta vélbúnaðinn til að beita uppfærslum þannig að hann truflar enn minna og hann mun ná yfir bæði stýrikerfisuppfærslur og gæðauppfærsluuppfærslu.

    Fyrir gagnvirka notendur gæti virk lota verið rofin og tilraunin fer aftur í uppfært umhverfi. Með tilkomu [forgangstengd lotuáætlun](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), sem er nú fáanlegt á grundvelli opt-in, bata tímasetningu og vinnsla bata og halda áfram strax eftir uppfærsluna. Forgangsbundin lotuáætlun verður til staðar fyrir viðskiptavini áður en þeir byrja að taka þátt í fyrirbyggjandi dreifingu á gæðauppfærslum fyrir framleiðsluumhverfi þeirra.

- **Myrkra tímar** – Myrkratímar eru skilgreindir fyrir hvert Azure svæði og uppfærslur á niðritíma næstum núll munu eiga sér stað á myrkutímatímabilinu.

## <a name="the-proactive-update-process"></a>Fyrirbyggjandi uppfærsluferlið

Dreifing fyrirbyggjandi gæðauppfærslu mun fylgja öruggu dreifingarferli (SDP). Sérkenni SDP munu þróast, en gæðauppfærslur verða upphaflega settar í sandkassaumhverfi. Ferlið mun byrja með umhverfi sem opnar fyrir snemmtæka dreifingu. Eftir því sem hlutfall sandkassa sem tókst að dreifa eykst mun dreifing í framleiðsluumhverfi hefjast. Enn og aftur mun ferlið byrja með umhverfi sem opnar fyrir snemmtæka dreifingu. Hlustunarkerfi munu fylgjast með kerfisfjarmælingum og atvikum á Livesite og munu stöðva útsetningu ákveðinnar útgáfu ef einhver afturför greinist. Viðskiptavinir munu samt geta dregið gæðauppfærslurnar á undan fyrirbyggjandi dreifingu ef þeir vilja.

Núverandi útgáfustjórnunargögn sýna að minna en 3 prósent af afturköllun eru kynnt í gæðauppfærslum. Með aukinni áherslu á að útrýma afturhvarfi og aukinni SDP, verða hugsanleg áhrif afturhvarfs verulega minni en gæðaávinningurinn sem næst með því að fá lagfæringar hraðar til viðskiptavina almennt.

## <a name="process-changes"></a>Breytingar á ferli

Verið er að innleiða sett af ferlibreytingum fyrir virkjun á fyrirbyggjandi gæðauppfærsluuppfærslu:

- **Skema** – Verkfæri munu tryggja að gæðauppfærslur innihalda aðeins skemabreytingar sem hægt er að beita á meðan þjónustan er á netinu. Þessi nálgun mun hjálpa til við að viðhalda getu til að beita uppfærslunni með næstum núlli niður í miðbæ.
- **Aukið eftirlit með breytingum** – Eins og er, er nú þegar aukaferlisskref til að samþykkja breytingar fyrir innlimun í gæðauppfærslu. Athugunin í aukaskrefinu verður aukin til að draga úr möguleikum á afturförum. Brotandi breytingar eru ekki leyfðar í gæðauppfærslum og aukin athugun á breytingum mun hjálpa til við að tryggja að við náum þessu markmiði.
- **Skyggni** - Við munum senda tilkynningar í gegnum stjórnendamiðstöðina, Lifecycle Services (LCS) og aðrar tiltækar rásir fyrir komandi fyrirbyggjandi gæðauppfærslur. Að auki munu stuðningsteymi og atviksleiðir hafa sýnilegt hvar gæðauppfærslur hafa verið settar á fyrirbyggjandi hátt.
 > [!NOTE]
 > Samskiptateymið Microsoft er að rannsaka áframhaldandi hnignun á tölvupóstverkfærum sem kemur í veg fyrir afhendingu tölvupósttilkynninga. Vinsamlegast haltu áfram að fylgjast með Microsoft 365 Skilaboðamiðstöð fyrir inngöngu- og tilkynningatengd skilaboð.
- **Fail Safe með flugi** – Flug verður notað til að verja kóðabreytingar þar sem það á við í gæðauppfærslu villuleiðréttingu eða nota núverandi eiginleika flug sem skipta máli fyrir lagfæringuna. Ef þörf er á að breyta til baka eða slökkva á breytingu eftir fyrirbyggjandi uppsetningu er hægt að gera það í gegnum flugkerfið til að forðast frekari bilanir.
- **Samstillingarheiti fyrir sandkassa** - Innan við 20 prósent viðskiptavina í dag eru með marga sandkassa og halda einum sandkassa uppbyggðum þar sem útgáfan passar við framleiðslu, til að hjálpa við bilanaleit. Ef viðskiptavinur notar sandkassa til að prófa nýrri útgáfu en framleiðslu hans mun sá sandkassi fá gæðauppfærslur í nýrri útgáfuna.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Hver er útfærsluvegaáætlun fyrir gæðauppfærslur?

Búist er við að dreifing á fyrirbyggjandi gæðauppfærslum fyrir sandkassaumhverfi hefjist seint í september eða október 2022 fyrir viðskiptavini Azure almenningsskýja. Reynsluumhverfi munu einnig byrja að fá fyrirbyggjandi uppfærsluuppfærslu á þeim tíma. Í september verður tilkynning send til hvers viðskiptavinar til að upplýsa þá um væntanlega tímaáætlun fyrir umhverfi sitt. Undantekningar frá fyrirbyggjandi uppfærðu dreifingarferli verða aðeins leyfðar fyrir viðskiptavini sem eru undir eftirliti FDA. Við erum enn að vinna úr því hvernig stjórnað umhverfi og skýjaviðskiptavinum ríkisins og stjórnvalda verður stjórnað.

Á næsta sex mánaða tímabili munum við smám saman auka hlutfall sandkassaumhverfa sem fá fyrirbyggjandi uppfærslur, þar til öll tilnefnd umhverfi eru tekin með og framfarir í að uppfæra framleiðsluumhverfi. Allt tímabilið munum við fylgjast með til að tryggja að dreifingarferlið sé óaðfinnanlegt og að við séum að ná markmiði okkar um hleðslu sem ekki truflar.

Vegna þess að viðskiptavinir munu reglulega fá minni hleðslu, gerum við ráð fyrir því að ferlið við að vera núverandi verði einfaldara. Við munum breyta tíðni uppfærsluuppfærslu þegar við sýnum getu til að keyra ferlið án truflana. Þetta ferli er nú þegar að virka á áhrifaríkan hátt fyrir okkar Dataverse vettvang og forrit, og er að skila væntanlegum framförum í þjónustugæðum. Okkur langar til að stíga sama skref fram á við fyrir umsóknir um fjármál og rekstur.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Hvenær hefjast gæðauppfærslur fyrir framleiðsluumhverfi?
Eins og er miða gæðauppfærslur aðeins á sandkassa. Við munum uppfæra þetta rými með upphafsdagsetningu fyrir framleiðsluumhverfi þegar við höfum áþreifanlegri gögn og mælikvarða frá fyrirbyggjandi uppfærslum fyrir sandkassa til að meta tilbúið til framleiðslu.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Hver er áætlunin fyrir fyrirbyggjandi gæðauppfærslur í sandkassa?
Fyrir upplýsingar um myrkur stundir fyrir hvert svæði, sjá [Hverjir eru fyrirhugaðir viðhaldsgluggar eftir svæðum](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?.

### <a name="proactive-quality-update-release-10028"></a>Fyrirbyggjandi gæðauppfærsluútgáfa: 10.0.28
**App útgáfa: 10.0.1265.89**
**Samsvarandi nýjustu KB grein: 745340**

| Stöð | Svæði | Útfyllt dagskrá| Komandi Sandbox Dagskrá
|---|---|---|---|
| Stöð 1 | Kanada Mið, Kanada Austur, Frakkland Mið, Indland Mið, Noregur Austur, Sviss Vestur | 15. september til 18. september 2022, 19. september til 22. september 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 2 | Frakkland Suður, Indland Suður, Noregur Vestur, Sviss Norður, Suður Afríka Norður, Ástralía Austur, Bretland Suður, UAE Norður, Japan Austur, Ástralía Suð Austur, Suðaustur Asía | 25. september til 28. september 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 3 | Austur-Asía, Bretland Vestur, Japan Vestur, Brasilía Suður, Vestur-Evrópa, Austur-Bandaríkin, Mið UAE | 26. september til 29. september 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 4 | Norður-Evrópa, Mið-Bandaríkin, Vestur-Bandaríkin | 28. september til 1. október 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 5 | DoD, Government Community Cloud, Kína | Ekki áætlað | Ekki áætlað |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Fyrirbyggjandi gæðauppfærsluútgáfa: 10.0.29
**App útgáfa: 10.0.1326.70**
**Samsvarandi nýjustu KB grein: 748926**

| Stöð | Svæði | Komandi Sandbox Dagskrá
|---|---|---|
| Stöð 1 | Kanada Mið, Kanada Austur, Frakkland Mið, Indland Mið, Noregur Austur, Sviss Vestur | 14. október til 17. október 2022 |
| Stöð 2 | Frakkland Suður, Indland Suður, Noregur Vestur, Sviss Norður, Suður Afríka Norður, Ástralía Austur, Bretland Suður, UAE Norður, Japan Austur, Ástralía Suð Austur, Suðaustur Asía | 15. október til 18. október 2022 |
| Stöð 3 | Austur-Asía, Bretland Vestur, Japan Vestur, Brasilía Suður, Vestur-Evrópa, Austur-Bandaríkin, Mið UAE | 16. október til 19. október 2022 |
| Stöð 4 | Norður-Evrópa, Mið-Bandaríkin, Vestur-Bandaríkin | 17. október til 20. október 2022 |
| Stöð 5 | DoD, Government Community Cloud, Kína | Ekki áætlað |

> [!IMPORTANT] 
> Fimm daga fyrirvara mun Microsoft uppfæra áætlunina á undan og senda tilkynningar í tölvupósti til þess hóps umhverfis sem áætlað er að fái þessar gæðauppfærslur. Fyrri áætlun á aðeins við um umhverfi sem hefur verið tilkynnt um væntanlega uppfærslu. Fyrir upplýsingar um myrkur stundir fyrir hvert svæði, sjá [Hverjir eru fyrirhugaðir viðhaldsgluggar eftir svæðum](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?.
>
> Fyrir hvern svæðishóp, eða *stöð*, þar sem áætlað er að gæðauppfærsla verði sett út, sýnir áætlunin fjögurra daga bil. Gæðauppfærslur byrja aðeins með sandkassaumhverfi. Síðan, eftir því sem hlutfall sandkassa sem tókst að dreifa eykst, mun dreifing í framleiðsluumhverfi hefjast með fyrirfram tilkynningum til viðskiptavina.
> 
> Gæðauppfærslur munu alltaf eiga sér stað í hringi sem gerir okkur kleift að miða á sett af umhverfi í samræmi við áætlun og klára öll sett fyrir lok fjórða dags fyrir stöð. Hins vegar þýðir þetta ekki að umhverfisuppfærsla taki fjóra daga. Það þýðir bara að við getum ekki fyrirfram ákveðið hvaða umhverfi verður uppfært á tilteknum degi innan fjögurra daga bilsins. Allar uppfærslur verða gerðar á dimmum tímum, með næstum núlli niður í miðbæ. Uppfærslum lýkur endanlega innan myrkrastunda glugga tiltekins svæðis.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hvernig er myrkri klukkustundum meðhöndlað fyrir viðskiptavini sem eru með eitt fjármála- og rekstrarforrit en eru virkir á mörgum tímabeltum? 
Það eru engar sérstakar áætlanir utan myrkra tíma þar sem tilfelli fjármála- og rekstrarforrita er til, þar sem við ætlum að setja út gæðauppfærslur á sem minnst truflandi hátt með [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Hver er núverandi útsetningartíðni fyrir fyrirbyggjandi gæðauppfærslur?
Fyrirbyggjandi gæðauppfærslur (PQUs) eru sendar einu sinni í mánuði fyrir hverja studda útgáfu af þjónustuuppfærslu. Aðeins er ýtt á eina uppfærslu á mánuði fyrir valið sandkassaumhverfi nema viðskiptavinir fari yfir í nýja þjónustuuppfærsluútgáfu. Í því tilviki gætu þeir fengið fyrirfram áætlaða PQU sem hluta af núverandi lest fyrir nýju þjónustuuppfærsluna. Eftir að útfærslu um allan heim er lokið árið 2023 mun tíðni þessara uppfærslu aukast. Þú færð alltaf a.m.k. eins mánaðar fyrirvara í hvert skipti sem breytingar verða á sendingartíðni.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hvernig mun Microsoft tryggja gæði þessara uppfærslu?
Microsoft leitast við að halda útgáfupípunni nógu skilvirkri til að skila litlum farmi til að halda löggildingarkostnaði lágum. Sérhver lagfæring í gæðauppfærslu fer í gegnum strangt og öruggt dreifingarferli sem hjálpar til við að bæta gæði og áreiðanleika og dregur þannig úr áhrifum viðskiptavina. Dreifing mun gerast í áföngum á sandkassaumhverfi fyrst og síðan framleiðsla. Sviðsuppsetning gerir kleift að fylgjast með réttu eftirliti til að ákvarða hvort frekari dreifing sé örugg. Við munum stöðva útfærsluna ef vandamál finnast hjá hverjum hópi viðskiptavina sem notaðir eru og tryggja að hvert skref í útfærslunni hafi nægan tíma til að vandamál komi upp á yfirborðið. Fyrir hverja væntanlega gæðauppfærslu munum við veita sýnileika í áætluninni með uppfærslum á opinberum skjölum og tölvupóstum, svo viðskiptavinir geti skipulagt fram í tímann.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Geta viðskiptavinir seinkað, breytt tímasetningu eða gert hlé á gæðauppfærslu?
Nr. Meginmarkmið gæðauppfærslna er að tryggja að grundvallaratriði eins og öryggi, friðhelgi einkalífs, áreiðanleika, framboð og afköst séu stöðugt að bæta fyrir viðskiptavini okkar. Með því að seinka eða gera hlé á uppfærslu er öryggi, aðgengi og áreiðanleiki í hættu.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Hvernig veit ég hvaða mengi breytinga fór í gæðauppfærsluhleðslu?
Eftirfarandi skref eru tímabundin lausn þar sem við höldum áfram að vinna að því að bjóða upp á betri lausn til að bera kennsl á listann yfir breytingar sem fara í gæðauppfærsluhleðslu. 

Notaðu KB# 745340 fyrir 10.0.28 gæðauppfærslulestina og tengda app útgáfu 10.0.1265.89.

1. Í LCS, opnaðu **Umhverfisupplýsingar** síðu fyrir sandkassann þinn. 
2. Í **Tiltækar uppfærslur** kafla, veldu **Skoða uppfærslu** fyrir nýjustu gæðauppfærslu smíðina. 
3. Flyttu út bygginguna í CSV eða Microsoft Excel skrá.
4. Í útfluttu skránni skaltu flokka upplýsingarnar út frá tíma (elstu fyrst) og leita síðan að KB númerinu 745340 í **Uppfæra auðkenni** dálki. Þú ættir nú að geta séð delta listann yfir KBs.
 
 > [!NOTE]
 > Útflutningur í CSV eða Excel skrá verður að gerast áður en umhverfið er uppfært. Annars geturðu notað umhverfi með svipaða uppsetningu sem er ekki með uppfærsluna uppsetta og fylgdu skrefunum hér að ofan.

[![Dæmi um umhverfi með gæðauppfærslu.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Hvert er ferlið ef mikilvægt vandamál finnst eftir gæðauppfærslu?
Mikilvægt mál eða afturför er einn eða fleiri atburðir sem venjulega valda því að margir viðskiptavinir hafa skerta reynslu af einni eða fleiri þjónustu okkar. Þessi vandamál geta valdið ófyrirséðri niður í miðbæ, þar með talið óaðgengi, skert frammistöðu og truflun á þjónustustjórnun. Ef það eru víðtæk áhrif á viðskiptavini vegna slíkra aðhvarfs, munum við stöðva útgáfu gæðauppfærslu þar til við getum haft samskipti og lagað vandamálið. Venjulega mun næsta gæðauppfærsla hafa nauðsynlega lagfæringu til að hefja útsetningu á ný.

Ef umhverfi eins viðskiptavinar verður fyrir áhrifum skaltu hafa samband við þjónustudeild Microsoft til að opna miða. Byggt á rökstuðningnum munum við stöðva útfærslu gæðauppfærslunnar í öll önnur umhverfi í því verkefni þar til vandamálið hefur verið dregið úr.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Geta viðskiptavinir samt beitt flýtileiðréttingum handvirkt frá LCS?
Já. Til að tryggja áframhaldandi jafnræði við hvernig flýtileiðréttingar virka, er enn hægt að beita flýtileiðréttingum á umhverfi viðskiptavina í LCS. Hins vegar er mikilvægt að hafa í huga að bráðaleiðréttingar sem eru settar upp sem hluti af gæðauppfærslu fara í gegnum staðlaða SDP áður en uppfærslan er sett á laggirnar. Þetta dregur úr hættu á afturförum vegna meiri gæða. Við mælum með því að þú veljir gæðauppfærslu en að beita flýtileiðréttingum handvirkt til að auka áreiðanleika.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Geta viðskiptavinir sett upp gæðauppfærsluuppfærslu á undan áætlun?
Já. Þú getur sett upp gæðauppfærslu fyrirbyggjandi. Microsoft mun sleppa uppfærslunni ef núverandi byggingarútgáfa umhverfisins er jöfn eða hærri en viðkomandi gæðauppfærsla.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Ef umhverfi er með væntanlega mánaðarlega þjónustuuppfærslu innan viku, mun það samt fá gæðauppfærslur?
- Gæðauppfærslur eru ekki notaðar á framleiðsluumhverfi ef það er yfirvofandi þjónustuuppfærsla áætluð innan viku frá því að gæðauppfærslan á að gerast.
- Ef sandkassaumhverfi er með sömu eða hærri byggingarútgáfu en yfirvofandi gæðauppfærsla verður því sleppt.
- Ef framleiðsluumhverfi er með sömu eða hærri byggingarútgáfu en yfirvofandi gæðauppfærsla verður henni sleppt.
- Ef sandkassi er með sömu eða hærri byggingarútgáfu vegna gæðauppfærslu eða handvirkrar uppfærslu á framleiðslunni mun framleiðslan samt fá áætlaða útgáfu mánaðarlegrar þjónustuuppfærslu. Ef þú vilt ekki að áætlað framleiðsluumhverfi verði uppfært í þjónustuuppfærsluútgáfuna geturðu gert hlé á þjónustuuppfærslunni frá LCS. 
- Við mælum með því að þú notir nýjustu gæðauppfærslugerðina til að prófa breytingarnar þínar fyrir væntanlega þjónustuuppfærslu fyrir betri stöðugleika og árangur.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Ef umhverfi hefur væntanlega áætlaða aðgerð og áætlaða gæðauppfærslu í sama viðhaldsglugga, mun það samt fá gæðauppfærsluna?
Ef einhver ágreiningur er um fyrirfram tímasetta aðgerð, td Point In Time Restore (PITR), verður gæðauppfærslan færð aftur í næsta tiltæka viðhaldsglugga innan fjögurra daga gluggans. Fyrir frekari upplýsingar um dagskrá, sjá [Hver er áætlunin fyrir fyrirbyggjandi gæðauppfærslur](#schedule)?. 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Er hægt að færa umhverfi aftur í fyrra ástand ef það eru vandamál eftir að gæðauppfærslu er beitt?
Eftir að gæðauppfærslu hefur verið beitt er engin afturköllun undir neinum kringumstæðum. Það eru aðeins möguleikar á áframhaldandi plástra í boði til að draga úr vandamálum.

## <a name="what-about-fda-regulation-and-gpx"></a>Hvað með FDA reglugerð og GPX?
Áætlunin fyrir viðskiptavini sem eru háðir FDA fullgildingu og reglugerð er enn í þróun. Búast má við fleiri uppfærslum á þessu svæði fljótlega. Í bili eru allir slíkir viðskiptavinir undanþegnir gæðauppfærslum. Til að tryggja að viðskiptavinur falli undir reglugerðir FDA, vinsamlegast farðu á [Microsoft Azure GPX tilboð](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Hvaða útgáfur af þjónustuuppfærslum eru studdar fyrir þessar gæðauppfærslur?
Viðskiptavinir á öllum studdum útgáfum af þjónustuuppfærslum eiga rétt á gæðauppfærslum. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Innleiðing fjármála- og rekstrarforrita með smásöluíhlutum krefst venjulega viðbótarvinnu auk þess að þurfa að endurútfæra MPOS. Hvaða áhrif munu þessar gæðauppfærslur hafa á RetailSDK? 
Vegna þess að eðli flýtileiðréttingarinnar sjálfrar breytist ekki í gæðauppfærsluhleðslunni, gerum við ekki ráð fyrir neinum frekari áhrifum sem tengjast sérstaklega smásöluíhlutum eins og er.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Eru einhver áhrif á Cloud Hosted Environments (CHE)? 
CHE umhverfi er utan svigrúms fyrir gæðauppfærslur vegna þess að þau eru utan verksviðs Microsoft

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Eru einhver samþættingarvandamál með Microsoft Dataverse? 
Það eru engin þekkt samþættingarvandamál fyrir gæðauppfærslur með Dataverse.

