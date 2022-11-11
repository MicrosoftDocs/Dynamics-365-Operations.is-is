---
title: Lén í Dynamics 365 Commerce
description: Þessi grein lýsir því hvernig lén eru meðhöndluð í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750681"
---
# <a name="domains-in-dynamics-365-commerce"></a>Lén í Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig lén eru meðhöndluð í Microsoft Dynamics 365 Commerce.

Lén eru vefföng sem eru notuð til að fara á Dynamics 365 Commerce-vefsvæði í netvafra. Þú sérð um stjórnun á léninu þínu með valdri DNS-veitu. Vísað er í lén í gegnum Dynamics 365 Commerce-vefsmið til að samræma hvernig svæði verður opnað þegar það er birt. Í þessari grein er farið yfir hvernig lén eru meðhöndluð og vísað í allan lífsferil þróunar og kynningar viðskiptasíðunnar.

> [!NOTE]
> Frá og með 6. maí 2022 er allt umhverfi búið til í Dynamics 365 Commerce verður útvegað með`.dynamics365commerce.ms` lén, sem kemur í stað fyrra mynsturs `.commerce.dynamics.com`. Núverandi umhverfi útvegað með`.commerce.dynamics.com` lénið mun halda áfram að virka.

## <a name="provisioning-and-supported-host-names"></a>Úthlutun og studd hýsilheiti

Þegar verið er að úthluta rafrænu viðskiptaumhverfi í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), er kassinn **Studd lénsheiti** í úthlutunarskjámynd rafrænna viðskipta notaður til að færa inn lén sem munu tengjast uppsettu viðskiptaumhverfi. Þessi lén verða DNS-heiti sem snúa að viðskiptavinum þar sem vefsvæði rafrænna viðskipta verða hýst. Að slá inn lén á þessu stigi byrjar ekki að beina umferð fyrir lénið í Dynamics 365 Commerce. Umferð fyrir lén verður aðeins vísað á Commerce-endastöð þegar CNAME-færsla DNS er uppfærð til að nota Commerce-endastöðina með léninu.

> [!NOTE]
> Hægt er að færa mörg lén inn í kassann **Studd hýsilheiti** með því að aðskilja þau með semíkommu.

Eftirfarandi mynd sýnir úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan. 

![Úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Hægt er að stofna þjónustubeiðni til að bæta öðrum lénum við umhverfi ef úthlutun hefur þegar átt sér stað. Til að stofna þjónustubeiðni í LCS skaltu í umhverfinu þínu fara í **Stuðningur \> Vandamál varðandi stuðning** og velja **Senda inn tilvik**.

## <a name="commerce-generated-urls"></a>Vefslóðir myndaðar af Commerce

Þegar rafrænu Dynamics 365 Commerce viðskiptaumhverfi er úthlutað, býr Commerce til vefslóð sem verður vinnuveffangið fyrir umhverfið. Vísað er í þessa vefslóð í tengli á rafræna viðskiptasvæðið í LCS þegar búið er að úthluta umhverfinu. Vefslóð sem Commerce myndar er á sniðinu `https://<e-commerce tenant name>.dynamics365commerce.ms`, þar sem biðlaraheiti rafrænna viðskipta er heitið sem fært er inn í LCS fyrir viðskiptaumhverfið.

Einnig er hægt að nota hýsilheiti fyrir framleiðslusvæði í sandkassaumhverfi. Þessi valkostur er tilvalinn þegar þú ætlar að afrita síðu úr sandkassaumhverfi til framleiðslu.

## <a name="site-setup"></a>Uppsetning svæðis

Þegar búið er að úthluta rafrænu viðskiptaumhverfi þarf að setja upp vefsvæðið í Commerce-vefsmið til að tengja vefsvæðið við virku vefslóðina.

Þegar fyrst er sett upp svæði í vefsmið birtist svarglugginn **Setja upp svæðið þitt**.

Eftirfarandi mynd sýnir svargluggann **Setja upp svæðið þitt** fyrir svæði sem heitir „sjálfgefið“ þegar þú ferð inn á svæðið í fyrsta skipti í vefsmiðnum.

![**Setja upp svæðið þitt** svargluggi.](./media/Domains_SetupyoursiteScreen.png)

Glugginn **Velja lén** gerir þér kleift að tengja eitt af studdu hýsilheitunum, sem gefin er upp fyrir svæðið þitt í LCS, við svæðið þitt í vefsmiðnum.

Gluggann **Slóð** er hægt að skilja eftir auðan, eða bæta aukalegum streng við slóðina sem kemur fram í virku vefslóðinni þinni. Ef glugginn **Slóð** er skilinn eftir auður, tengir það grunnvefslóðina sem Commerce myndar við svæðið sem verið er að setja upp í vefsmiðnum. Slóðir verða að vera einkvæmar fyrir hvert svæðis-/lénapar. Innan svæðis og léns sem valið er, getur aðeins eitt svæði í umhverfinu notað auðu slóðina eða verið tengt við einkvæman streng slóðar. Öllum strengjum sem bætt er við reitinn **Slóð** við uppsetningu svæðis verða undirslóðir grunnvefslóðar sem Commerce myndar og notaðar til að komast inn á svæðið í vafra.

> [!NOTE]
> Slóðin er einnig þekkt sem **Samsvörun við slóð** þegar rás er bætt við skilgreiningarhlutann **Stillingar svæðis \> Rásir** í vefsmiðnum.

Ef þú ert til dæmis með svæði í vefsmiðnum sem heitir „fabrikam“ í biðlaraheiti rafrænna viðskipta „xyz“ og ef þú setur upp svæðið með auðri slóð, þá myndir þú opna birt efni vefsvæðisins í vafra með því að fara beint í grunnvefslóð sem Commerce býr til:

`https://xyz.dynamics365commerce.ms`

Að öðrum kosti, ef þú bættir við slóðinni „fabrikam“ við sömu uppsetningu vefsvæðisins, myndir þú opna birt efni vefsvæðisins í vafra með því að nota eftirfarandi vefslóð:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Síður og vefslóðir

Þegar búið er að setja upp svæðið með slóð, munu allar vefslóðir sem tengjast síðunum byggja ofan á virku vefslóðinni (Commerce-myndaða vefslóðin eða Commerce-myndaða vefslóðin ásamt slóðinni) fyrir svæðið. Að búa til nýja vefslóð í vefsmiðnum (**Vefslóðir /> +Nýtt**) með því að velja síðu í listanum í svarglugganum **Ný vefslóð** og færa inn vefslóðina fyrir þessa síðu mun tengja vefslóðina við völdu síðuna. Gildi vefslóðarinnar bætist þá við virka vefslóð svæðisins til að opna síðuna og er merkt sem `./<URL path>` í vefslóðarlistanum á síðunni **Vefslóðir** í vefsmiðnum.

Eftirfarandi mynd sýnir svargluggann **Ný vefslóð** í vefsmiðnum með auðkennt dæmi um vefslóð. 

![**Ný vefslóð** svargluggi í vefsmið.](./media/Domains_PageSetup2a.png)

Eftirfarandi mynd sýnir síðuna **Vefslóðir** í vefsmiðnum með auðkenndu dæmi um vefslóð í listanum.

![Keyra valkost notendaflæðis í stefnuflæði.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Lén í vefsmiðnum

Gildi studdra hýsilheita eru í boði til að tengja sem lén þegar svæði er sett upp. Þegar þú velur stutt hýsingarnafnsgildi sem lén muntu sjá valið lén sem vísað er til í vefsmiðjunni. Þetta lén er aðeins tilvísun innan viðskiptaumhverfisins, umferð í beinni fyrir það lén verður ekki enn framsend til Dynamics 365 Commerce.

Þegar unnið er með svæði í vefsmið, ef þú ert með tvö svæði sett upp með tveimur mismunandi lénum, geturðu bætt eigindinni **?domain=** við virku vefslóðina til að opna efni birta vefsvæðisins í vafra.

Til dæmis hefur umhverfi „xyz“ verið úthlutað og tvö svæði hafa verið búin til og tengd í vefsmiðnum: eitt með lénið `www.fabrikam.com` og hitt með lénið `www.constoso.com`. Hvort svæði var sett upp með auðri slóð. Síðan var hægt að komast inn á þessi svæði í vafra eins og meðfylgjandi með því að nota eigindina **?domain=**:
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Þegar lénsfyrirspurnarstrengur er ekki gefinn upp í umhverfi með mörg lén, notar Commerce fyrsta lénið sem þú gafst upp. Til dæmis, ef slóðin „fabrikam“ var gefin upp fyrst við uppsetningu vefsvæðið, væri hægt að nota vefslóðina `https://xyz.dynamics365commerce.ms` til að opna efni birta vefsvæðisins fyrir `www.fabrikam.com`.

Þú getur líka bætt við sérsniðnum lénum. Til að gera það, á umhverfisstjórnunarsíðunni fyrir verkefnið, undir **rafræn viðskipti** undirfyrirsögn, veldu **+ Bættu við sérsniðnu léni**. Rennistikan sýnir núverandi sérsniðin lén og gefur möguleika á að bæta við nýju sérsniðnu léni.

## <a name="update-which-commerce-scale-unit-is-used"></a>Uppfærðu hvaða Commerce Scale Unit er notuð

Commerce Scale Unit (CSU) sem Commerce notar er venjulega valin þegar umhverfi er upphaflega búið til. Commerce gerir þér kleift að breyta hvaða CSU-tilvik umhverfið þitt notar, sem gerir þér kleift að viðhalda arkitektúrnum þínum betur með sjálfsafgreiðsluvirkni og dregur úr þörfinni á að hafa samband við þjónustudeild. Til að uppfæra CSU tilvikið þitt skaltu fara á viðskiptastjórnunarsíðu umhverfisins þíns fyrir verkefnið og velja síðan **Uppfærðu mælikvarðaeiningu**. Nota **Ný verslunarkvarðaeining** renna til að velja nýtt CSU tilvik af listanum yfir CSU sem eru tiltækar fyrir umhverfið þitt.

## <a name="traffic-forwarding-in-production"></a>Framsend umferð í framleiðslu

Hægt er að líkja eftir mörgum lénum með því að nota færibreytur fyrir fyrirspurnarstreng léns á endastöð commerce.dynamics.com. En þegar nauðsynlegt er að fara í framleiðslu í rauntíma þarf að framsenda umferðina fyrir sérsniðna lénið á endastöðina `<e-commerce tenant name>.dynamics365commerce.ms`.

The`<e-commerce tenant name>.dynamics365commerce.ms` endapunktur styður ekki sérsniðið lén Secure Sockets Layers (SSL), svo þú verður að setja upp sérsniðin lén með því að nota útidyraþjónustu eða efnisafhendingarnet (CDN). 

Til að setja upp sérsniðin lén með því að nota Front Door-þjónustu eða CDN, eru tveir möguleikar í boði:

- Settu upp útidyraþjónustu eins og Azure Front Door til að sinna framendaumferð og tengjast viðskiptaumhverfinu þínu, sem veitir meiri stjórn á léns- og vottorðastjórnun og nákvæmari öryggisstefnu.

- Notaðu Azure Front Door tilvikið sem fylgir Commerce, sem krefst samhæfingar aðgerða við Dynamics 365 Commerce teymi til að sannprófa lén og fá SSL vottorð fyrir framleiðslulénið þitt.

> [!NOTE]
> Ef þú ert að nota utanaðkomandi CDN eða útidyraþjónustu skaltu ganga úr skugga um að beiðnin lendi á Commerce pallinum með hýsingarheitinu sem Commerce hefur gefið upp, en með X-Forwarded-Host (XFH) hausnum \<custom-domain\>. Til dæmis, ef Commerce endapunkturinn þinn er`xyz.dynamics365commerce.ms` og sérsniðna lénið er`www.fabrikam.com`, hýsingarhaus framsendu beiðninnar ætti að vera`xyz.dynamics365commerce.ms` og XFH hausinn ætti að vera `www.fabrikam.com`.

Frekari upplýsingar um hvernig setja á upp CDN-þjónustu beint má finna í [Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md).

Til að nota tilvik Azure Front Door sem Commerce útvegar, þarf að stofna þjónustubeiðni fyrir CDN-uppsetningaraðstoð úr innleiðingarteymi Commerce. 

- Þú þarft að gefa upp nafn fyrirtækis þíns, framleiðslulén, auðkenni umhverfisins og heiti leigjanda fyrir rafræn viðskipti framleiðslu. 
- Þú þarft að staðfesta hvort þessi þjónustubeiðni er fyrir núverandi lén (notað fyrir virka síðu) eða nýtt lén. 
- Fyrir nýtt lén er hægt að ná í sannprófun á léni og SSL-vottorð í einu skrefi. 
- Fyrir lén sem þjónar núverandi vefsíðu þarf margra þrepa ferli til að koma á lénsstaðfestingu og SSL vottorði. Þetta ferli er með þjónustustigssamning sjö virkra daga til að gera lén virkt í rauntíma, því að í því felast mörg skref í ákveðinni röð.

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

Azure Front Door tilvikið sem fylgir Commerce styður ekki apex lén (rótarlén sem innihalda ekki undirlén). Apex lén þurfa IP tölu til að leysa og Commerce Azure Front Door tilvikið er aðeins til með sýndarendapunktum. Til að nota apex lén hefurðu eftirfarandi valkosti:

- **Valkostur 1** - Notið DNS-veitu til að framsenda apex-lénið á „www“ lén. Fabrikam.com framsendir til dæmis `www.fabrikam.com` þar sem `www.fabrikam.com` er CNAME-færslan sem bendir á tilvik Azure Front Door sem Commerce hýsir.

- **Valkostur 2** - Ef DNS veitandinn þinn styður ALIAS færslur geturðu bent apex léninu á Azure Front Door endapunktinn, sem tryggir að IP breytingin frá endapunktinum endurspeglast. Þú verður að hýsa Azure Front Door tilvikið sjálfur.
  
- **Valkostur 3** - Ef DNS veitandinn þinn styður ekki ALIAS færslur, þá verður þú að breyta DNS þjónustuveitunni þinni í Azure DNS og hýsa bæði Azure DNS og Azure Front Door tilvikið sjálfur.

> [!NOTE]
> Ef verið er að nota Azure Front Door þarf einnig að setja upp Azure-DNS í sömu áskriftinni. Apex-lénið sem hýst er á Azure DNS getur bent á Azure Front Door sem samnefnd færsla. Þetta er eina hjáleiðin, þar sem apex-lén verða alltaf að benda á IP-tölu.
  
Ef þú hefur einhverjar spurningar varðandi Apex lén, vinsamlegast hafðu samband [Stuðningur Microsoft](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Frekari upplýsingar

  [Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

  [Setja upp netverslunarrás](./channel-setup-online.md)

  [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

  [Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

  [Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

  [Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

  [Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

  [Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

  [Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

  [Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

  [Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
