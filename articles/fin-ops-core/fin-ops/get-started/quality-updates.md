---
title: Fyrirbyggjandi gæðauppfærslur
description: Þessi grein veitir upplýsingar um afhendingu fyrirbyggjandi gæðauppfærslna.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 4e30ca84d20425c73c658179d2136920195aa920
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788487"
---
# <a name="proactive-quality-updates"></a>Fyrirbyggjandi gæðauppfærslur

[!include[banner](../includes/banner.md)]

Á síðustu árum hefur Microsoft tekið stöðugum framförum í því sem við nefnum [eina útgáfu](../../dev-itpro/lifecycle-services/oneversion-overview.md). Forsenda einnar útgáfu er einföld: Því nær sem við getum komist því að allir viðskiptavinir fái sömu hugbúnaðarútgáfu, þeim mun meiri gæði getum við veitt. Við leitum að og leysum vandamál í eitt skipti fyrir öll og leggjum slíkar lausnir í hendur fleiri viðskiptavinum hraðar.

Þessi forsenda er staðfest með niðurstöðunum: færri atvikafjöldi á öllum vörum okkar. Þegar viðskiptavinir fá ekki sömu útgáfu sjáum við stöðugt að þeir glíma við vandamálum sem lausn er þegar í boði fyrir. Við höfum nú þegar náð frábærum árangri með Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations og Dynamics 365 Commerce og þökk sé nýlegum tækniframförum er nú hægt að taka næsta skref. Eftirfarandi upplýsingar segja til um hvað við ætlum að gera, hvað við höfum þegar gert til undirbúnings og hvernig og hvenær við kynnum nýju eiginleikana án truflana.

## <a name="what-you-need-to-know"></a>Þetta þarftu að vita

- Fyrirbyggjandi gæðauppfærslur eru gerðar mánaðarlega.
- Microsoft notar fyrirbyggjandi gæðauppfærslur í öll umhverfi í sandkassa sem keyra þjónustuuppfærslu sem var [í notkun](./public-preview-releases.md#targeted-release-schedule-dates-subject-to-change) þegar fyrirbyggjandi gæðauppfærslur voru búnar til.
- Undantekningar fyrir fyrirbyggjandi gæðauppfærslum verða leyfðar fyrir viðskiptavini undir stjórn Bandaríska matvæla- og lyfjaeftirlitinu (FDA).
- Microsoft er að ákvarða hvernig fyrirbyggjandi gæðauppfærslum verður háttað í stýrðum umhverfum og fyrir viðskiptavini ríkja og stjórnvalda í skýjum.
- Tilkynningar sem tengjast fyrirbyggjandi gæðauppfærslum eru birtar [Microsoft 365 í Skilaboðamiðstöðinni](https://admin.microsoft.com/AdminPortal/) og á borða í Microsoft Dynamics Lifecycle Services-verki viðskiptavinar.
- Fimm dögum áður en fyrirbyggjandi gæðauppfærsla er notuð í umhverfi fá viðskiptavinir tilkynningu um að uppfærslan muni eiga sér stað.
- Viðskiptavinir geta ekki hætt við eða frestað fyrirbyggjandi gæðauppfærslum.
- Fyrirbyggjandi gæðauppfærslur eru settar upp á meðan svæðisbundnu, [áætluðu viðhaldstímabili](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) stendur.
- Gæðauppfærslur eru hannaðar með það fyrir augum að lítil hætta sé á vandamálum eða afturför og þetta er stutt af gögnum frá Microsoft.
- Microsoft mælir með markvissri prófun vegna tiltekinna vandamála eða tiltekinna bráðabóta sem tengjast fyrirbyggjandi gæðauppfærslu.

## <a name="focus-on-quality-updates"></a>Áhersla á gæðauppfærslur

Eins og er bjóðum við upp á sjö [þjónustuuppfærslur](public-preview-releases.md) á ári. Til dæmis er útgáfa 10.0.29 þjónustuuppfærsla. Þar til nýlega voru átta uppfærslur á ári. Hins vegar létum við eina uppfærslu falla niður vegna athugasemda viðskiptavina sem vildu forðast breytingar við lok almanaksársins.

Við munum ekki breyta uppfærslutakti þjónustunnar. Þess í stað er næsta skref í áætlun okkar um eina útgáfu að einblína á *gæðauppfærslum*. Gæðauppfærslur er samsett smíði á bráðabótum. Þær innihalda ekki nýja eiginleika. Allir viðskiptavinir okkar eru á milli þriggja eða fjögurra nýjustu þjónustuuppfærslna okkar. Hins vegar er hægt að nota tugi mismunandi útgáfa gæðauppfærslna fyrir hverja þjónustuuppfærslu innan hópsins, allt eftir því hvaða dagsetningar fólk notar. Í næsta skrefi munum við senda út fyrirbyggjandi gæðauppfærslur. Við notum nú þegar þetta líkan fyrir forrit okkar sem byggjast á Dataverse og höfum séð fyrirsjáanlegar niðurstöður varðandi aukin gæði og minni þjónustutilvik.

Auðvitað gæti fækkun galla dregið úr eða komið alveg í veg fyrir þörfina á gæðauppfærslum. Við höfum margvíslegar áætlanir um forútgáfur til að draga úr göllum sem krefjast gæðauppfærslna. Jafnvel þegar dregið er úr innihaldi gæðauppfærslu mun samræmi á milli viðskiptavina bæta stuðning við þjónustu, koma úrbætur til viðskiptavina hraðar og draga úr tíðni viðskiptavina sem lenda í vandamálum fyrir lausnir sem þegar eru til staðar.

## <a name="making-proactive-distribution-possible"></a>Að gera fyrirbyggjandi dreifingu mögulega

Fjölmargar framfarir hafa þegar verið gerðar virkar sem gera kleift að afhenda gæðauppfærslur á fyrirbyggjandi hátt:

- **Nánast enginn niðurtími á meðan uppfært er** – Til að ýta undir tíðari umhverfi er nauðsynlegt að dregið verði úr áhrifum á tiltækileika umhverfis til að standa við þjónustustigssamninga Dynamics 365 (SLA). Nánast enginn niðurtími á meðan uppfært er var upphaflega kynntur til sögunnar til að bæta mánaðarlegar lagfæringar stýrikerfisins með því að nota varakerfi klasa til að virkja uppfærða mynd og halda röskun í lágmarki. Verið er að endurbæta kerfið til að nota uppfærslur þannig að það verði enn minna truflandi og það mun bæði ná yfir lagfæringar á stýrikerfi og innleiðingu á gæðauppfærslu.

    Fyrir gagnvirka notendur gæti virk lota verið rofin og nýuppfærða umhverfið opnast þegar reynt er aftur. Með innleiðingu á [Forgangsbyggðri runuáætlunargerð](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) endurheimtir áætlunargerð og vinnsla runu og hefst aftur strax eftir uppfærsluna. Forgangsbyggð runuáætlunargerð verður til staðar fyrir viðskiptavini áður en þeir byrja að taka þátt í fyrirbyggjandi dreifingu gæðauppfærslna fyrir vinnsluumhverfi sitt.

- **Næturtími** – Næturtími er skilgreindur fyrir hvert Azure-svæði og nær engar uppfærslur valda niðurtíma á meðan næturtíma stendur.

## <a name="the-proactive-update-process"></a>Ferli fyrirbyggjandi uppfærslu

Útfærsla fyrirbyggjandi gæðauppfærslna mun fylgja öruggu innleiðingarferli (SDP). Sérkenni notkunar í sandkassaumhverfi munu þróast, en í upphafi verða gæðauppfærslur notaðar í sandkassaumhverfi. Eftir því sem hlutfall uppsettra sandkassa eykst mun innleiðing í vinnsluumhverfi hefjast. Hlustunarkerfi munu fylgjast með fjarmælingum kerfisins og Livesite atvikum og stöðvar útgáfu tiltekinnar útgáfu ef afturför greinist. Viðskiptavinir geta áfram fengið gæðauppfærslur á undan fyrirbyggjandi innleiðingu ef þeir vilja.

Núverandi gögn um útgáfustjórnun sýna að afturför verður í minna en 3 prósent af gæðauppfærslum. Með aukinni áherslu á að útrýma afturför og öruggu innleiðingarferli (SDP) verða hugsanleg áhrif af afturför umtalsvert minni en gæðaaukningin sem næst með því að koma endurbótum hraðar til viðskiptavina með víðtækum hætti.

## <a name="process-changes"></a>Breytingar á ferli

Verið er að innleiða breytingarferli á undan virkjun fyrirbyggjandi gæðauppfærslna:

- **Skema** – Verkfæri tryggja að smíði gæðauppfærslu feli aðeins í sér breytingar á skema sem hægt er að nota á meðan þjónusta er nettengd. Þessi aðferð viðheldur möguleikanum á að nota uppfærsluna með nánast engum niðurtíma.
- **Aukið eftirlit með breytingum** – Sem stendur er nú þegar viðbótarskref í ferlinu til að samþykkja breytingar sem á að innifela í gæðauppfærslu. Eftirlit í viðbótarskrefinu verður aukin til að draga úr líkum á afturför. Skipting á breytingum er ekki leyfð í uppfærslum og aukið eftirlit með breytingum hjálpar til við að tryggja að við uppfyllum þetta markmið.
- **Sýnileiki** – Tilkynningar eru sendar um stjórnendamiðstöðina, Lifecycle Services og aðrar tiltækar rásir fyrir væntanlegar fyrirbyggjandi gæðauppfærslur. Auk þess munu þjónustudeildir og atvikafulltrúar hafa sýnileika þar sem gæðauppfærslur hafa verið settar upp á fyrirbyggjandi hátt.

    > [!NOTE]
    > Starfsfólk Microsoft samskiptamiðstöðvarinnar rannsakar stöðugt niðurbrot á verkfærum fyrir tölvupóst sem kemur í veg fyrir að tilkynningar í tölvupósti berist. Haltu áfram að fylgjast með Microsoft 365 Skilaboðamiðstöðinni til að fá skilaboð um innleiðingar og tilkynningar.

- **Aukið öryggi með forútgáfu** – Forútgáfa verður notuð til að vakta breytingar á kóða þar sem það á við í villuleiðréttingu gæðauppfærslna eða til að nota núverandi eiginleika forútgáfu sem á við um endurbæturnar. Ef nauðsynlegt er að endurheimta eða slökkva á breytingunni eftir að hún hefur verið tekin í fyrirbyggjandi notkun, er hægt að gera það í gegnum forútgáfukerfið til að koma í veg fyrir frekari bilanir.
- **Merking samstillingar sandkassa** – Innan við 20 prósent viðskiptavina í dag eru með marga sandkassa og halda einum sandkassa í notkun þar sem útgáfan passar við framleiðsluna, til að aðstoða við úrræðaleit. Ef viðskiptavinur notar sandkassa til að prófa nýrri útgáfu en hann framleiðir mun sá sandkassi fá gæðauppfærslur á nýrri útgáfu.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Hvernig er áætlun fyrir útgáfu gæðauppfærslur?

Gert er ráð fyrir að dreifing fyrirbyggjandi gæðauppfærslna fyrir sandkassaumhverfi hefjist í lok september eða október 2022 fyrir viðskiptavini almennra Azure-skýja. Prófunarumhverfi byrja einnig að fá fyrirbyggjandi uppfærslur á þeim tíma. Í september verður hverjum viðskiptavini send tilkynning til að upplýsa hann um fyrirætlaða áætlun fyrir umhverfi þeirra. Undantekningar frá uppfærða fyrirbyggjandi dreifingarferlinu verða aðeins leyfðar fyrir viðskiptavini sem er stjórnað af Matvæla- og lyfjaeftirliti Bandaríkjanna (FDA). Við erum enn að vinna í því hvernig reglubundnu umhverfi og viðskiptavinum ríkja og stjórnvalda verður háttað.

Á næsta sex mánaða tímabili munum við smám saman auka hlutfall sandkassaumhverfis sem fær fyrirbyggjandi uppfærslur, þar til öll tilgreind umhverfi eru innifalin og halda áfram og uppfæra vinnsluumhverfi. Á tímabilinu munum við fylgjast með til að tryggja að uppsetningarferlið sé hnökralaust og að við séum að ná markmiði okkar með innihald sem valdi engum truflunum.

Vegna þess að viðskiptavinir munu fá minna og minna innihald væntum við þess að uppfærsluferlið verði einfaldara. Við munum breyta tíðni uppsetningu uppfærslunnar þegar sýnt hefur verið fram á að hægt sé að ferlið án truflana. Þetta ferli virkar nú þegar fyrir Dataverse verkvanginn okkar og forrit og skilar væntanlegum umbótum á gæðum þjónustunnar. Við viljum sem fyrst taka sömu skref áfram og fyrir forritum fjármála- og reksturs.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Hvenær hefjast gæðauppfærslur fyrir framleiðsluumhverfi?
Sem stendur eru gæðauppfærslur aðeins á sandkössum. Við munum uppfæra þetta rými með upphafsdegi fyrir vinnsluumhverfi þegar við höfum áreiðanlegri gögn og tölulegar upplýsingar um fyrirbyggjandi uppfærslur fyrir sandkassa til að meta hvort allt sé til reiðu til framleiðslu.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Hver er áætlunin fyrir fyrirbyggjandi gæðauppfærslur á sandkassa?
Upplýsingar um næturtíma fyrir hvert svæði er að finna í [Hvað er áætlað viðhaldstímabil eftir svæðum?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10028"></a>Útgáfa fyrirbyggjandi gæðauppfærslu: 10.0.28
**Útgáfa forrits: 10.0.1265.89**  
**Samsvarandi nýjasta grein í þekkingargrunni: 745340**

| Stöð | Svæði | Lokin áætlun| Væntanleg áætlun fyrir Sandbox
|---|---|---|---|
| Stöð 1 | Mið-Kanada, Austur-Kanada, Mið-Frakkland, Mið-Indland, Austur-Noregur, Vestur-Sviss | 15. september til 18. september 2022, 19. september til 22. september 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 2 | Suður-Frakkland, Suður-Indland, Vestur-Noregur, Norður-Sviss, Suður-Afríka, Austur-Ástralía, Suður-Bretland, Norður-Sameinuðu arabísku furstadæmin, Austur-Japan, Suðaustur-Ástralía, Suðaustur-Asía | 25. til 28. september 2022 og 7. til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 3 | Austur-Asía, Vestur-Bretland, Vestur-Japan, Suður-Brasilía, Vestur-Evrópa, Austur-Bandaríkin, Mið-Sameinuðu arabísku furstadæmin | 26. september til 29. september 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 4 | Norður-Evrópa, Mið-Bandaríkin, Vestur-Bandaríkin | 28. september til 1. október 2022 og 7. október til 10. október 2022 | 25. október til 28. október 2022 |
| Stöð 5 | DoD, Government Community Cloud, Kína | Ekki áætlað | Ekki áætlað |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Útgáfa fyrirbyggjandi gæðauppfærslu: 10.0.29
**Útgáfa forrits: 10.0.1326.70**  
**Samsvarandi nýjasta grein í þekkingargrunni: 750332**

| Stöð | Svæði | Lokin áætlun | Væntanleg áætlun fyrir Sandbox|
|---|---|---|---|
| Stöð 1 | Mið-Kanada, Austur-Kanada, Mið-Frakkland, Mið-Indland, Austur-Noregur, Vestur-Sviss | 14. október til 17. október 2022, 2. nóvember til 5. nóvember 2022 | 13. nóvember til 16. nóvember 2022 |
| Stöð 2 | Suður-Frakkland, Suður-Indland, Vestur-Noregur, Norður-Sviss, Suður-Afríka, Austur-Ástralía, Suður-Bretland, Norður-Sameinuðu arabísku furstadæmin, Austur-Japan, Suðaustur-Ástralía, Suðaustur-Asía | 15. október til 18. október 2022, 2. nóvember til 5. nóvember 2022 | 13. nóvember til 16. nóvember 2022 |
| Stöð 3 | Austur-Asía, Vestur-Bretland, Vestur-Japan, Suður-Brasilía, Vestur-Evrópa, Austur-Bandaríkin, Mið-Sameinuðu arabísku furstadæmin | 16. október til 19. október 2022, 2. nóvember til 5. nóvember 2022 | 13. nóvember til 16. nóvember 2022 |
| Stöð 4 | Norður-Evrópa, Mið-Bandaríkin, Vestur-Bandaríkin | 17. október til 20. október 2022, 2. nóvember til 5. nóvember 2022 | 15. nóvember til 18. nóvember 2022 |
| Stöð 5 | DoD, Government Community Cloud, Kína | Ekki áætlað | Ekki áætlað |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Útgáfa fyrirbyggjandi gæðauppfærslu: 10.0.30
**Útgáfa forrits: 10.0.1362.77**
**Samsvarandi nýjasta grein í þekkingargrunni: 767597.**

| Stöð | Svæði | Væntanleg áætlun fyrir Sandbox |
|---|---|---|
| Stöð 1 | Mið-Kanada, Austur-Kanada, Mið-Frakkland, Mið-Indland, Austur-Noregur, Vestur-Sviss | 1. desember til 4. desember 2022 |
| Stöð 2 | Suður-Frakkland, Suður-Indland, Vestur-Noregur, Norður-Sviss, Suður-Afríka, Austur-Ástralía, Suður-Bretland, Norður-Sameinuðu arabísku furstadæmin, Austur-Japan, Suðaustur-Ástralía, Suðaustur-Asía | 2. desember til 5. desember 2022 |
| Stöð 3 | Austur-Asía, Vestur-Bretland, Vestur-Japan, Suður-Brasilía, Norður-Evrópa, Austur-Bandaríkin, Mið-Sameinuðu arabísku furstadæmin | 3. desember til 6. desember 2022 |
| Stöð 4 | Vestur-Evrópa, Mið-Bandaríkin, Vestur-Bandaríkin | 4. desember til 7. desember 2022 |
| Stöð 5 | DoD, Government Community Cloud, Kína | Ekki áætlað |

> [!IMPORTANT] 
> Með fimm daga fyrirvara uppfærir Microsoft framangreinda áætlun og sendir tilkynningu fyrir sett umhverfa sem áætlað er að fái þessar gæðauppfærslur. Undanfarandi áætlun á aðeins við um umhverfi sem hefur verið tilkynnt um væntanlega uppfærslu. Upplýsingar um næturtíma fyrir hvert svæði er að finna í [Hvað er áætlað viðhaldstímabil eftir svæðum?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Fyrir hvern svæðishóp eða *-stöð*, þar sem áætlað er að gæðauppfærsla verði sett upp, sýnir áætlunin tímabil sem nær yfir allt að fjóra daga. Gæðauppfærslur hefjast á sandkassaumhverfum eingöngu. Síðan, eftir því sem hlutfall uppsettra sandkassa eykst mun innleiðing í vinnsluumhverfi hefjast með því að senda viðskiptavinum tilkynningar með fyrirvara.
> 
> Gæðauppfærslur munu alltaf eiga sér stað hver á eftir annarri sem gerir okkur kleift að miða á tiltekna hópa umhverfa í hverri áætlun og ljúka öllum umhverfum fyrir lok fjórða dags fyrir stöð. Þetta þýðir samt ekki að uppfærsla á umhverfi taki fjóra daga. Það þýðir bara að við getum ekki ákveðið fyrirfram hvaða umhverfishópar verður uppfært á tilteknum degi innan fjögurra daga bilsins. Allar uppfærslur verða gerðar á næturtíma og niðurtími verður nánast enginn. Uppfærslum lýkur endanlega að næturlagi á tilgreindu svæði.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hvernig er næturtíma háttað fyrir viðskiptavini sem eru með tilvik forritum fjármála- og reksturs en eru virkir á mörgum tímabeltum? 
Engar sérstakar áætlanir eru utan næturtíma þar sem tilvik forritum fjármála- og reksturs er til, þar sem við áætlum að setja upp gæðauppfærslur með [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean) til að valda sem minnstum röskunum.

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Hver er núverandi uppfærslutaktur fyrirbyggjandi gæðauppfærslur?
Fyrirbyggjandi gæðauppfærslur eru eins og er sendar einu sinni í mánuði fyrir hverja studda útgáfu af þjónustuuppfærslu. Aðeins er verið að senda eina uppfærslu á mánuði fyrir valin sandkassaumhverfi nema viðskiptavinir færi sig yfir í nýja þjónustuuppfærslu. Ef svo er getur verið að viðkomandi fengið fyrirfram ákveðna fyrirbyggjandi gæðauppfærslu sem hluta af núverandi þjálfun fyrir nýju þjónustuuppfærsluna. Eftir að útgáfu er lokið á heimsvísu árið 2023 mun tíðni þessara uppfærslna aukast. Þú munt alltaf fá að minnsta kosti eins mánaðar fyrirvara í hvert sinn sem breyting verður á sendingartaktinum.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hvernig mun Microsoft tryggja gæði þessara uppfærslna?
Microsoft leggur sig fram um að útgáfan sé nógu skilvirk til að koma litlu innihaldi til skila til að halda staðfestingarkostnaðinum lágum. Allar lagfæringar í gæðauppfærslu fara í gegnum nákvæmt og öruggt uppsetningarferli sem stuðlar að auknum gæðum og áreiðanleika og dregur um leið á áhrifum á viðskiptavini. Uppsetning mun gerast í þrepum í sandkassaumhverfi fyrst og síðan framleiðslu í kjölfarið. Með sviðsettum uppsetningum er hægt að fylgjast með því hvort frekari uppsetning sé örugg. Við stöðvum útgáfuna ef vandamál greinast hjá hverjum hópi viðskiptavina og tryggjum að við hvert skref í útgáfunni sé nægur tími fyrir vandamál að koma fram. Fyrir allar væntanlegar gæðauppfærslur munum við auka sýnileika áætlunarinnar með uppfærslum á opinberum gögnum og tölvupóstum svo að viðskiptavinir geti skipulagt sig fram í tímann.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Geta viðskiptavinir seinkað, breytt áætlun eða gert hlé á gæðauppfærslu?
Nr. Meginmarkmið gæðauppfærslna er að tryggja að grundvallaratriði eins og öryggi, persónuvernd, áreiðanleiki, framboð og afköst séu stöðugt að batna fyrir viðskiptavini okkar. Með því að seinka eða gera hlé á uppfærslu er öryggi, framboð og áreiðanleiki í hættu.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Hvernig veit ég hvaða breytingar voru gerðar á innihaldi gæðauppfærslu?
Eftirfarandi skref eru tímabundin lausn þar sem við vinnum áfram að því að veita betri lausn til að auðkenna lista yfir breytingar á innihaldi gæðauppfærslu. 

Notaðu KB nr. 745340 fyrir þjálfun 10.0.28 Gæðauppfærsla og tengda uppfærslu forritsins 10.0.1265.89.

1. Opnaðu síðuna **Umhverfisupplýsingar** fyrir sandkassann þinn í Lifecycle Services. 
2. Í hlutanum **Tiltækar uppfærslur** skal velja **Skoða uppfærslu** til að skoða nýjustu útgáfu gæðauppfærslu. 
3. Flytja út smíðina í CSV- eða Microsoft Excel-skrá.
4. Í útfluttu skránni skaltu flokka upplýsingar í tímaröð (elst fyrst) og leita svo að KB númerinu 745340 í dálkinum **Uppfæra auðkenni**. Nú ætti að vera hægt að sjá lista yfir breytingar fyrir KB.
 
> [!NOTE]
> Flytja þarf út CSV- eða Excel-skrá áður en umhverfið er uppfært. Annars er hægt að nota umhverfi með svipaða stillingu sem er ekki með uppfærsluna uppsetta og fylgja skrefunum hér að ofan.

[![Dæmi um umhverfi með gæðauppfærslu.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Hvert er ferlið ef alvarlegt vandamál kemur í ljós eftir gæðauppfærslu?
Afgerandi vandamál eða afturför eru eitt eða fleiri tilvik sem valda því að margir viðskiptavinir fá verri upplifun af einni eða fleiri þjónustu okkar. Slík vandamál geta valdið ófyrirsjáanlegum niðurtíma, þar með talið ótiltækileika, skertum afköstum og truflunum á þjónustustjórnun. Ef viðskiptavinur verður fyrir víðtækum áhrifum vegna slíkrar afturfarar útgáfu á gæðauppfærslu þar til við getum átt í samskiptum og leyst vandamálið. Venjulega inniheldur næsta gæðauppfærsla með nauðsynlegum lagfæringum til að útgáfan geti haldið áfram.

Ef eitt umhverfi viðskiptavinar verður fyrir áhrifum skaltu hafa samband við notendaþjónustu Microsoft til að opna beiðni. Á grundvelli fenginna staðreynda stöðvum við útgáfu gæðauppfærslu i öllum öðrum umhverfum í því verkefni þar til vandamálið hefur verið lagfært.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Geta viðskiptavinir enn handvirkt notað uppfærslum bráðabóta frá Lifecycle Services?
Já. Til að tryggja áframhaldandi jafnræði með því hvernig bráðabætur virka er enn hægt að nota uppfærslur bráðabóta í umhverfi viðskiptavina í Lifecycle Services. Hins vegar er mikilvægt að hafa í huga að bráðabætur sem eru notuð í gæðauppfærslu fara í gegnum staðlað, öruggt uppsetningarferli áður en uppfærslan er sett upp. Þetta dregur úr hættu á afturför vegna meiri gæða. Mælt er með því að þú veljir gæðauppfærslu í stað þess að nota bráðabætur handvirkt til að auka áreiðanleika.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Geta viðskiptavinir sett upp útgáfu gæðauppfærslu á undan áætlun?
Já. Þú getur sett upp gæðauppfærslu á fyrirbyggjandi hátt. Microsoft mun sleppa uppfærslunni ef núverandi útgáfa smíðar umhverfisins er jöfn eða hærri en umrædd gæðauppfærsla.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Ef umhverfi er með mánaðarlega þjónustuuppfærslu á áætlun innan viku fær það samt gæðauppfærslu?
- Gæðauppfærslur eru ekki notaðar fyrir vinnsluumhverfi ef væntanleg þjónustuuppfærsla er á áætlun innan við viku frá því að áætlað er að gæðauppfærslan eigi sér stað.
- Ef sandkassaumhverfi er með sömu eða hærri útgáfu smíðar en væntanleg gæðauppfærsla verður því sleppt.
- Ef vinnsluumhverfi er með sömu eða hærri útgáfu smíðar en væntanleg gæðauppfærsla verður því sleppt.
- Ef sandkassi er með sömu eða hærri útgáfu smíðar vegna gæðauppfærslu eða handvirkrar uppfærslu á framleiðslunni mun framleiðslan samt fá áætlaða útgáfu af mánaðarlegri þjónustuuppfærslu. Ef þú vilt ekki að áætlað vinnsluumhverfi sé uppfært í útgáfu þjónustuuppfærslu geturðu gert hlé á þjónustuuppfærslu frá Lifecycle Services. 
- Við mælum með því að þú nýtir nýjustu smíði gæðauppfærslu prófa breytingarnar þínar fyrir væntanlega þjónustuuppfærslu til að fá betri stöðugleika og niðurstöður.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Ef umhverfi er með áætlaða aðgerð á næstunni og gæðauppfærslu á sama viðhaldstímabili, fær það samt gæðauppfærslu?
Ef einhver árekstur verður við fyrirfram áætlaða aðgerð, til dæmis endurheimt tímapunkts (PITR), verður áætlun gæðauppfærslu breytt í næsta tiltæka viðhaldstímabil innan fjögurra daga tímabilsins. Nánari upplýsingar um áætlunina er að finna [Hver er áætlunin fyrir fyrirbyggjandi gæðauppfærslur?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Er hægt að færa umhverfi aftur í fyrra horf ef upp koma vandamál eftir að gæðauppfærsla er notuð?
Eftir að gæðauppfærsla er notuð er ekki undir neinum kringumstæðum hægt að endurheimta. Aðeins eru í boði lagfæringar fyrir seinni útgáfur til að leysa vandamál.

## <a name="what-about-fda-regulation-and-gpx"></a>Hvað með reglugerð Matvæla- og lyfjaeftirlits Bandaríkjanna (FDA) og GPX?
Áætlun fyrir viðskiptavini sem falla undir samþykki og reglugerðir Matvæla- og lyfjaeftirliti Bandaríkjanna (FDA) er enn í þróun. Þú getur búist við að fleiri uppfærslur birtist hér bráðum. Sem stendur eru allir slíkir viðskiptavinir undanþegnir gæðauppfærslum. Opnaðu [Microsoft Azure framboð á GPX](/azure/compliance/offerings/offering-gxp) til að ganga úr skugga um að viðskiptavinur falli undir reglugerð Matvæla- og lyfjaeftirlit Bandaríkjanna (FDA).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Hvaða útgáfur af þjónustuuppfærslum eru studdar fyrir þessar gæðauppfærslur?
Viðskiptavinir með allar studdar útgáfur af þjónustuuppfærslum eru gjaldgengir fyrir gæðauppfærslum. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Uppsetning forritum fjármála- og reksturs með smásöluíhlutum krefst yfirleitt viðbótarvinnu auk þess að þurfa að setja aftur upp MPOS. Hvernig munu þessar gæðauppfærslur hafa áhrif á Retail SDK? 
Þar sem bráðabótin sjálft breytist ekki í innihaldi gæðauppfærslu, gerum við ekki ráð fyrir neinum frekari áhrifum sem tengjast smásöluíhlutum eins og stendur.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Verða einhver áhrif á umhverfum í skýi (CHE)? 
Umhverfi í skýi (CHE) er utan sviðs fyrir gæðauppfærslur vegna þess að það er utan verksviðs Microsoft.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Eru einhver samþættingarmál með Microsoft Dataverse? 
Ekki er vitað um nein samþættingarvandamál vegna gæðauppfærslna við Dataverse.

