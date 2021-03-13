---
title: Lén í Dynamics 365 Commerce
description: Þetta efnisatriði lýsir því hvernig lén eru afgreidd í Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: d855f2164e4ee0f0cdb220787eb96217523137e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010248"
---
# <a name="domains-in-dynamics-365-commerce"></a>Lén í Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig lén eru afgreidd í Microsoft Dynamics 365 Commerce.

Lén eru vefföng sem eru notuð til að fara á Dynamics 365 Commerce-vefsvæði í netvafra. Þú sérð um stjórnun á léninu þínu með valdri DNS-veitu. Vísað er í lén í gegnum Dynamics 365 Commerce-vefsmið til að samræma hvernig svæði verður opnað þegar það er birt. Þetta efnisatriði fer yfir hvernig lén eru meðhöndluð og vísað í gegnum feril þróunar og útgáfu Commerce-svæðis.

## <a name="provisioning-and-supported-host-names"></a>Úthlutun og studd hýsilheiti

Þegar verið er að úthluta rafrænu viðskiptaumhverfi í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), er kassinn **Studd lénsheiti** í úthlutunarskjámynd rafrænna viðskipta notaður til að færa inn lén sem munu tengjast uppsettu viðskiptaumhverfi. Þessi lén verða DNS-heiti sem snúa að viðskiptavinum þar sem vefsvæði rafrænna viðskipta verða hýst. Að færa inn lén á þessu stigi setur ekki af stað umferð inn á lénið á Dynamics 365 Commerce. Umferð fyrir lén verður aðeins vísað á Commerce-endastöð þegar CNAME-færsla DNS er uppfærð til að nota Commerce-endastöðina með léninu.

> [!NOTE]
> Hægt er að færa mörg lén inn í kassann **Studd hýsilheiti** með því að aðskilja þau með semíkommu.

Eftirfarandi mynd sýnir úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan. 

![Úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan](./media/Domains_ProvisioningeCommerceScreen.png)

Hægt er að stofna þjónustubeiðni til að bæta öðrum lénum við umhverfi ef úthlutun hefur þegar átt sér stað. Til að stofna þjónustubeiðni í LCS skaltu í umhverfinu þínu fara í **Stuðningur \> Vandamál varðandi stuðning** og velja **Senda inn tilvik**.

## <a name="commerce-generated-urls"></a>Vefslóðir myndaðar af Commerce

Þegar rafrænu Dynamics 365 Commerce viðskiptaumhverfi er úthlutað, býr Commerce til vefslóð sem verður vinnuveffangið fyrir umhverfið. Vísað er í þessa vefslóð í tengli á rafræna viðskiptasvæðið í LCS þegar búið er að úthluta umhverfinu. Vefslóð sem Commerce myndar er á sniðinu `https://<e-commerce tenant name>.commerce.dynamics.com`, þar sem biðlaraheiti rafrænna viðskipta er heitið sem fært er inn í LCS fyrir viðskiptaumhverfið.

Einnig er hægt að nota hýsilheiti fyrir framleiðslusvæði í sandkassaumhverfi. Þessi möguleiki er tilvalinn þegar vefsvæði er afritað úr sandkassaumhverfi í framleiðslu.

## <a name="site-setup"></a>Uppsetning svæðis

Þegar búið er að úthluta rafrænu viðskiptaumhverfi þarf að setja upp vefsvæðið í Commerce-vefsmið til að tengja vefsvæðið við virku vefslóðina.

Þegar fyrst er sett upp svæði í vefsmið birtist svarglugginn **Setja upp svæðið þitt**.

Eftirfarandi mynd sýnir svargluggann **Setja upp svæðið þitt** fyrir svæði sem heitir „sjálfgefið“ þegar þú ferð inn á svæðið í fyrsta skipti í vefsmiðnum.

![**Setja upp svæðið þitt** svargluggi](./media/Domains_SetupyoursiteScreen.png)

Glugginn **Velja lén** gerir þér kleift að tengja eitt af studdu hýsilheitunum, sem gefin er upp fyrir svæðið þitt í LCS, við svæðið þitt í vefsmiðnum.

Gluggann **Slóð** er hægt að skilja eftir auðan, eða bæta aukalegum streng við slóðina sem kemur fram í virku vefslóðinni þinni. Ef glugginn **Slóð** er skilinn eftir auður, tengir það grunnvefslóðina sem Commerce myndar við svæðið sem verið er að setja upp í vefsmiðnum. Slóðir verða að vera einkvæmar fyrir hvert svæðis-/lénapar. Innan svæðis og léns sem valið er, getur aðeins eitt svæði í umhverfinu notað auðu slóðina eða verið tengt við einkvæman streng slóðar. Öllum strengjum sem bætt er við reitinn **Slóð** við uppsetningu svæðis verða undirslóðir grunnvefslóðar sem Commerce myndar og notaðar til að komast inn á svæðið í vafra.

> [!NOTE]
> Slóðin er einnig þekkt sem **Samsvörun við slóð** þegar rás er bætt við skilgreiningarhlutann **Stillingar svæðis \> Rásir** í vefsmiðnum.

Ef þú ert til dæmis með svæði í vefsmiðnum sem heitir „fabrikam“ í biðlaraheiti rafrænna viðskipta „xyz“ og ef þú setur upp svæðið með auðri slóð, þá myndir þú opna birt efni vefsvæðisins í vafra með því að fara beint í grunnvefslóð sem Commerce býr til:

`https://xyz.commerce.dynamics.com`

Að öðrum kosti, ef þú bættir við slóðinni „fabrikam“ við sömu uppsetningu vefsvæðisins, myndir þú opna birt efni vefsvæðisins í vafra með því að nota eftirfarandi vefslóð:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Síður og vefslóðir

Þegar búið er að setja upp svæðið með slóð, munu allar vefslóðir sem tengjast síðunum byggja ofan á virku vefslóðinni (Commerce-myndaða vefslóðin eða Commerce-myndaða vefslóðin ásamt slóðinni) fyrir svæðið. Að búa til nýja vefslóð í vefsmiðnum (**Vefslóðir /> +Nýtt**) með því að velja síðu í listanum í svarglugganum **Ný vefslóð** og færa inn vefslóðina fyrir þessa síðu mun tengja vefslóðina við völdu síðuna. Gildi vefslóðarinnar bætist þá við virka vefslóð svæðisins til að opna síðuna og er merkt sem `./<URL path>` í vefslóðarlistanum á síðunni **Vefslóðir** í vefsmiðnum.

Eftirfarandi mynd sýnir svargluggann **Ný vefslóð** í vefsmiðnum með auðkennt dæmi um vefslóð. 

![**Ný vefslóð** svargluggi í vefsmið](./media/Domains_PageSetup2a.png)

Eftirfarandi mynd sýnir síðuna **Vefslóðir** í vefsmiðnum með auðkenndu dæmi um vefslóð í listanum.

![Keyra valkost notendaflæðis í stefnuflæði](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Lén í vefsmiðnum

Gildi studdra hýsilheita eru í boði til að tengja sem lén þegar svæði er sett upp. Þegar gildi studds hýsilheitis er valið sem lénið, sérðu vísað í valið lén í gegnum vefsmiðinn. Þetta lén er aðeins tilvísun innan Commerce-umhverfisins, umferð í rauntíma fyrir þetta lén verður ekki framsent til Dynamics 365 Commerce sem stendur.

Þegar unnið er með svæði í vefsmið, ef þú ert með tvö svæði sett upp með tveimur mismunandi lénum, geturðu bætt eigindinni **?domain=** við virku vefslóðina til að opna efni birta vefsvæðisins í vafra.

Til dæmis hefur umhverfi „xyz“ verið úthlutað og tvö svæði hafa verið búin til og tengd í vefsmiðnum: eitt með lénið `www.fabrikam.com` og hitt með lénið `www.constoso.com`. Hvort svæði var sett upp með auðri slóð. Síðan var hægt að komast inn á þessi svæði í vafra eins og meðfylgjandi með því að nota eigindina **?domain=**:
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Þegar fyrirspurnarstrengur léns er ekki gefinn í umhverfi með mörgum lénum, notar Commerce fyrsta lénið sem gefið er upp. Til dæmis, ef slóðin „fabrikam“ var gefin upp fyrst við uppsetningu vefsvæðið, væri hægt að nota vefslóðina `https://xyz.commerce.dynamics.com` til að opna efni birta vefsvæðisins fyrir `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Framsend umferð í framleiðslu

Hægt er að líkja eftir mörgum lénum með því að nota færibreytur fyrir fyrirspurnarstreng léns á endastöð commerce.dynamics.com. En þegar nauðsynlegt er að fara í framleiðslu í rauntíma þarf að framsenda umferðina fyrir sérsniðna lénið á endastöðina `<e-commerce tenant name>.commerce.dynamics.com`.

Endastöð `<e-commerce tenant name>.commerce.dynamics.com` styður ekki sérsniðin SSL og þarf því setja upp sérsniðin lén með því að nota Front Door-þjónustu eða efnisbirtingarnet (CDN). 

Til að setja upp sérsniðin lén með því að nota Front Door-þjónustu eða CDN, eru tveir möguleikar í boði:

- Setjið upp Front Door-þjónustu á borð við Azure til að meðhöndla umferð framvinnslu og tengjast viðskiptaumhverfinu þínu. Þetta veitir meiri stjórn á léni og vottorðastjórnun og nákvæmari öryggisstefnur.
- Notið tilvik Azure Front Door sem Commerce útvegar. Þetta krefst þess að samhæfa aðgerð við Dynamics 365 Commerce-teymið fyrir sannprófun léns og að fá SSL-vottorð fyrir framleiðslulénið.

Frekari upplýsingar um hvernig setja á upp CDN-þjónustu beint má finna í [Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md).

Til að nota tilvik Azure Front Door sem Commerce útvegar, þarf að stofna þjónustubeiðni fyrir CDN-uppsetningaraðstoð úr innleiðingarteymi Commerce. 

- Þú þarft að gefa upp heiti fyrirtækisins, framleiðslulénið, umhverfiskennið og biðlaraheiti rafrænna viðskipta framleiðslu. 
- Þú þarft að staðfesta ef þetta er lén sem er til staðar (notað fyrir virkt vefsvæði) eða nýtt lén. 
- Fyrir nýtt lén er hægt að ná í sannprófun á léni og SSL-vottorð í einu skrefi. 
- Fyrir lén sem þjónar fyrirliggjandi vefsvæði, er ferli í mörgum skrefum nauðsynlegt til að framkvæma sannprófun léns og fá SSL-vottorð. Þetta ferli er með þjónustustigssamning sjö virkra daga til að gera lén virkt í rauntíma, því að í því felast mörg skref í ákveðinni röð.

Til að stofna þjónustubeiðni í LCS skaltu í umhverfinu þínu fara í **Stuðningur \> Vandamál varðandi stuðning** og velja **Senda inn tilvik**.

> [!NOTE]
> Sérsniðin lén með SSL eru aðeins studd í vinnsluumhverfum. Fyrir önnur umhverfi en vinnsluumhverfi, t.d. sandkassa og samþykkisprófun notanda, skal nota vefslóðina sem Commerce myndar til að opna birt efni í vafra.

## <a name="ssl-certificate-process"></a>Ferli SSL-vottorðs

Þegar þjónustubeiðni er skráð, mun Commerce-teymið samræma eftirfarandi skref með þér.

Fyrir ný lén:
- Commerce-teymið mun setja upp tilvik Azure Front Door (hýst af Commerce).
- Commerce-teymið útvegar síðan CNAME-færsluna sem bendir á sérsniðna lénið þitt.
- Þegar CNAME-færslan hefur verið uppfærð, getur tilvik Azure Front Door sem Commerce hýsir sannprófað eignarhald lénsins og fengið SSL-vottorðið.

Fyrir núverandi/virk lén:
- Commerce-teymið biður þig um að bæta við `afdverify.<custom-domain>`-CNAME-færslu sem DNS-veita lénsins á að fá.
- Þegar því er lokið bætir Commerce-teymið léninu við tilvik Azure Front Door og útvega frekari DNS TXT-færslur sem bæta á við DNS fyrir lénið.
- Þegar TXT-færslunum er lokið, lýkur Commerce-teymið við uppfærslur Azure Front Door fyrir lénið sem mun setja upp SSL-vottorðið.

## <a name="apex-domains"></a>Apex-lén

Tilvik Azure Front Door styður ekki apex-lén (rótarlén sem innihalda ekki undirlén). Apex-lén þurfa IP-tölu til að leysa úr og tilvik Commerce Front Door er til með eingöngu sýndarendastöðvum. Til að nota apex-lén eru tveir möguleikar í boði:

- **Valkostur 1** - Notið DNS-veitu til að framsenda apex-lénið á „www“ lén. Fabrikam.com framsendir til dæmis `www.fabrikam.com` þar sem `www.fabrikam.com` er CNAME-færslan sem bendir á tilvik Azure Front Door sem Commerce hýsir.

- **Valkostur 2** - Setjið upp CDN-/front door-tilvik á eigin spýtum til að hýsa apex-lénið.

> [!NOTE]
> Ef verið er að nota Azure Front Door þarf einnig að setja upp Azure-DNS í sömu áskriftinni. Apex-lénið sem hýst er á Azure DNS getur bent á Azure Front Door sem samnefnd færsla. Þetta er eina hjáleiðin, þar sem apex-lén verða alltaf að benda á IP-tölu.

  ## <a name="additional-resources"></a>Frekari upplýsingar

  [Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

  [Setja upp netverslunarrás](online-stores.md)

  [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

  [Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

  [Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

  [Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

  [Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

  [Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

  [Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

  [Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

  [Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
