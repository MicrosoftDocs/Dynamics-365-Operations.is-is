---
title: Kortaðu rásir á netviðskiptasíður
description: Þetta efni lýsir nokkrum af algengari atburðarásum fyrir kortlagningu rása í Microsoft Dynamics 365 Commerce sem hægt er að framreikna fyrir flestar aðrar viðskiptakröfur.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ce272d63b4a37f99661333a02434708205ea19a
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743606"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kortaðu rásir á netviðskiptasíður

Þetta efni lýsir nokkrum af algengari atburðarásum fyrir kortlagningu rása í Microsoft Dynamics 365 Commerce sem hægt er að framreikna fyrir flestar aðrar viðskiptakröfur.

Dynamics 365 Commerce styður margar viðskiptasviðsmyndir fyrir kortlagningu [rásir á netinu](#channels) sem hafa stillt sett af vörum, verði og afslætti til [rafræn viðskipti síða](#e-commerce-sites) upplifun fyrir viðskiptavini.

Þetta efni nær yfir eftirfarandi aðstæður:

- **Rás á einu tungumáli sem hefur eina upplifun af rafrænum viðskiptum.** Til dæmis gæti þessi atburðarás falið í sér eina vörumerkjasíðu sem er stillt fyrir bandarískan enskan markað.
- **Fjöltungumálarás sem hefur eina staðbundna upplifun á vefsvæði.** Til dæmis gæti þessi atburðarás falið í sér eina vörumerkjasíðu sem er stillt fyrir Kanada með stuðningi á frönsku og ensku. Í þessari atburðarás hafa notendur sem velja mismunandi tungumál sömu síðuupplifun, en hún er staðfærð á valið tungumál hvers notanda.
- **Fjöltungumálarás sem hefur mismunandi upplifun á síðuna á hverju tungumáli.** Til dæmis gæti þessi atburðarás falið í sér eina vörumerkjasíðu sem er stillt fyrir Kanada með stuðningi á frönsku og ensku. Í þessari atburðarás er einstök síðaupplifun fyrir hvert tungumál.
- **Margar rásir (eitt tungumál og/eða fjöltungumál) sem hafa eina staðbundna upplifun á vefsvæði.** Til dæmis gæti þessi atburðarás falið í sér eina vörumerkjasíðu sem er stillt fyrir Ástralíu og Nýja Sjáland. Í þessari atburðarás deila bæði löndin sömu síðuupplifun á ensku, en hvert land er stillt með mismunandi vörur, gjaldmiðil, verð, afslætti og sendingaraðferðir.
- **Margar rásir (eitt tungumál og/eða fjöltungumál) sem hafa mismunandi upplifun á vefnum á hverja rás.** Til dæmis gæti þessi atburðarás falið í sér eina vörumerkjasíðu sem er stillt fyrir Ástralíu, Kanada og Þýskaland á mörgum tungumálum. Í þessari atburðarás hefur hvert land einstaka vefupplifun sem er stillt með mismunandi vörum, gjaldmiðli, verði, afslætti og sendingarmáta.

## <a name="channels"></a>Rásir

Rás (einnig þekkt sem netverslun eða netrás) táknar netverslun sem er notuð til að kortleggja vörur, verð, afslætti, tungumál, greiðslumáta, afhendingarmáta, uppfyllingarmiðstöðvar og aðra þætti netupplifunar sem verður í boði fyrir viðskiptavini þína í rafrænum viðskiptum. Rásir eru búnar til og stjórnað í höfuðstöðvum Commerce og kortlagðar á eina [lögaðili](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Lögaðilinn er venjulega staðsettur í einu landi sem krefst skattskýrslu fyrir rásina og hægt er að stilla hann með aðeins einum gjaldmiðli.

Fyrir frekari upplýsingar um rásir, sjá [Rásaryfirlit](channels-overview.md). Fyrir frekari upplýsingar um hvernig á að búa til netrás, sjá [Settu upp netrás](channel-setup-online.md).

Eftirfarandi dæmi frá höfuðstöðvum Commerce sýnir sjálfgefnar netrásir sem eru notaðar með Dynamics 365 Commerce ef kynningargagnavalkosturinn er valinn.

![Sjálfgefnar kynningargagnarásir í höfuðstöðvum Commerce.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>Netverslunarsíður

Rafræn viðskiptasíða inniheldur safn af síðum sem viðskiptavinir nota til að skoða og versla. Netverslunarsíðum er stjórnað í Commerce site builder.

Fyrir frekari upplýsingar um hvernig á að búa til og hafa umsjón með vefsvæðum í vefsvæðisgerð, sjá [Yfirlit yfir netverslunarsíður](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Algengar aðstæður fyrir kortlagningu rása

Dynamics 365 Commerce styður mikið úrval af rásakortlagningaratburðarás. Atburðarás rásakortlagningar sem á eftir fylgja eru aðeins undirmengi allra mögulegra rásakortunaratburðarása. Þau eru ætluð sem leiðarvísir til að hjálpa þér að skipuleggja allar einstöku viðskiptaaðstæður sem þú hefur. Hin tilbúna Adventure Works íþróttavöruverslun sem fylgir Dynamics 365 Commerce kynningargögn eru notuð sem dæmi fyrir hverja atburðarás.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Rás á einu tungumáli sem hefur eina upplifun af rafrænum viðskiptum

Í einföldustu atburðarásinni hefur ein rás eitt tungumál til að selja á einum markaði. Dæmi um þessa atburðarás er Adventure Works netverslun sem er sett upp fyrir enska markaðinn í Bandaríkjunum eingöngu.

Eftirfarandi dæmi sýnir rásaruppsetningu í höfuðstöðvum Commerce. Í þessari uppsetningu styður netrásin aðeins eitt tungumál (**en-okkur**), einn gjaldmiðill (**USD**), og einn rekstrareining (**usrt**) sem er notað til skattskýrslu.

![Gildi lögaðila, gjaldmiðils og tungumáls fyrir Adventure Works vefverslunina auðkennd í höfuðstöðvum Commerce.](media/channel-mapping-3.png)

Hægt er að kortleggja eina netrásina á eina netverslunarsíðu í vefsvæðisgerðinni. Fyrir upplýsingar um hvernig á að búa til nýja síðu og kortleggja hana á rás, sjáðu [Kortaðu rás á síðu í Site builder](#map-a-channel-to-a-site-in-site-builder) kafla þessa efnis.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Fjöltungumálarás sem hefur eina staðbundna upplifun á vefsvæði

Í þessari atburðarás styður ein rás fleiri en eitt tungumál. Þess vegna er hægt að staðfæra vöruheiti, lýsingar og eiginleika í höfuðstöðvum Commerce. Til að veita fullkomna staðbundna upplifun á vefsvæðinu er einnig hægt að staðsetja markaðsefni á síðunni í Commerce site builder.

Takmörkun þessarar atburðarásar er að hægt er að stilla eina rás með aðeins einum gjaldmiðli, einum lögaðila og einu setti af vörum og verði. Þessi uppsetning virkar best fyrir lönd sem hafa einn gjaldmiðil og mörg tungumál (til dæmis Kanada, sem hefur ensku og frönsku), einn lögaðila og eitt sett af vörum og verðum.

Hægt er að stilla hvert tungumál á rás með sínu eigin lén. Til dæmis, the`www.adventure-works.ca` lén er hægt að stilla fyrir Kanada ensku útgáfuna, og`www.adventure-works-fr.ca` lén er hægt að stilla fyrir frönsku útgáfuna í Kanada. Að öðrum kosti er hægt að stilla mismunandi tungumál á rás á einu léni og þá er hægt að nota mismunandi slóð fyrir hvert tungumál. Til dæmis, the`www.adventure-works.ca` lén er hægt að stilla fyrir Kanada ensku útgáfuna og síðan`www.adventure-works.ca/fr` slóð er hægt að nota fyrir frönsku útgáfuna í Kanada. [Geo uppgötvun](geo-detection-redirection.md) Einnig er hægt að virkja til að vísa notanda sjálfkrafa á rétta síðu, byggt á staðsetningu notandans.

Fyrir upplýsingar um hvernig á að gera viðskiptavinum kleift að skipta handvirkt á milli tungumála, sjá [Bættu við og stilltu vefvalseininguna](#add-and-configure-the-site-picker-module) kafla þessa efnis. Fyrir upplýsingar um hvernig á að sérsníða staðfærðar síður og brot, sjáðu [Hafa umsjón með efni vefsvæðis sem hefur margar rásir og tungumál](#manage-site-content-that-has-multiple-channels-and-languages) kafla.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Fjöltungumálarás sem hefur mismunandi vefupplifun á hverju tungumáli

Þú gætir frekar kosið atburðarás þar sem ein rás styður fleiri en eitt tungumál, en allt önnur upplifun vefsvæðis er sýnd fyrir hvert tungumál. Ráðlagð aðferð til að útfæra þessa atburðarás er að nota [síðuafbrigði](#implement-page-variants-for-each-language) á einni síðu.

Önnur aðferð er að búa til nýja e-verslunarsíðu fyrir hvert tungumál í vefsvæðisgerðinni og kortleggja síðan hverja síðu á eina netrás og tungumál. Niðurstaðan verður ein netrás sem er kortlögð á margar netviðskiptasíður, eina fyrir hvert tungumál. Þessi aðferð á mörgum stöðum krefst auka stjórnunarúrræða, vegna þess að það verða fleiri en ein síða til að stjórna í vefsmiðjum.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Margar rásir (eitt tungumál og/eða fjöltungumál) sem hafa eina staðbundna upplifun af vefsvæði

Vörumerkjasíða gæti þurft margar netrásir á hverju svæði til að styðja mismunandi gjaldmiðil, vörusett og verðsett fyrir hverja rás á einni síðu. Til dæmis gæti Adventure Works síða verið með netrás fyrir kanadíska markaðinn sem hefur mörg tungumál, rás fyrir bandaríska markaðinn sem hefur eitt tungumál og rás fyrir þýska markaðinn sem hefur eitt tungumál. Í þessari atburðarás verður hver netrás stillt fyrir svæðissértækan lögaðila og hún getur haft sama vörusafn og aðrar rásir hafa, undirmengi þessara vara eða annað vörusett. Hver rás mun einnig hafa sín verð í svæðisgjaldmiðli, sköttum, afslætti og sendingarmáta.

Í þessari atburðarás er hægt að stilla hvern markað með eigin lén. Til dæmis, the`www.adventure-works.com` lén er hægt að stilla fyrir Bandaríkjamarkað og`www.adventure-works.de` lén er hægt að stilla fyrir þýska markaðinn. Að öðrum kosti er hægt að stilla hvern markað til að nota aðra leið. Til dæmis, the`www.adventure-works.com` lén er hægt að stilla fyrir Bandaríkjamarkað, og þá`www.adventure-works.com/de` slóð er hægt að nota fyrir þýska markaðinn. [Geo uppgötvun](geo-detection-redirection.md) Einnig er hægt að virkja til að vísa notendum sjálfkrafa á rétta síðu, byggt á svæði þeirra.

Þú gætir líka viljað að vefsvæðið þitt bjóði upp á fellilista sem gerir notendum kleift að skipta handvirkt yfir á ákveðinn markað. Fyrir frekari upplýsingar, sjá [Bættu við og stilltu vefvalseininguna](#add-and-configure-the-site-picker-module) kafla þessa efnis.

Fyrir upplýsingar um hvernig á að stilla margar rásir á einni síðu, sjáðu [Stilltu margar rásir á netverslunarsíðu](#configure-multiple-channels-on-an-e-commerce-site) kafla.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Margar rásir (eitt tungumál og/eða fjöltungumál) sem hafa mismunandi upplifun af vef á hverri rás

Þú gætir viljað hafa margar rásir fyrir eitt vörumerki á mismunandi svæðum og þú gætir viljað að hvert svæði hafi mismunandi upplifun á vefnum. Það eru tvær aðferðir til að útfæra þessa atburðarás:

- Notaðu [síðuafbrigði](#implement-page-variants-for-each-language).
- Stilltu aðra síðu fyrir hverja netrás í vefsvæðisgerðinni og kortaðu síðan hverja síðu yfir á aðra netrás og tungumál. Þessi aðferð krefst auka stjórnunarauðlinda, vegna þess að það verða fleiri en ein síða til að stjórna í vefsvæðisgerðinni.

## <a name="cross-channel-sharing"></a>Deiling yfir rásir

Deiling milli rása er gagnleg þegar margar rásir á einu svæði geta deilt efni. Til dæmis getur smásali sem er með mörg vörumerki og netverslanir sem flokkað er undir einu svæði deilt sumu efni á milli sumra eða allra netverslananna. Samnýtt efni getur innihaldið síður fyrir skilmála og skilyrði, greiðsluskilmála, sendingaraðferðir og algengar spurningar (FAQ). Fyrir frekari upplýsingar, sjá [Virkjaðu og notaðu deilingu yfir rásir](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Kortaðu rás á síðu í Site builder

Það eru margar aðferðir til að búa til og stilla síður til að nota mismunandi netrásir.

### <a name="create-a-new-site"></a>Stofna nýtt svæði

Þú getur búið til glænýja síðu í Site builder með því að fara á **Síður** listasíðu og velja **Ný síða**. Þá, í **Ný síða** valmynd sem birtist geturðu valið sjálfgefna netrás og tungumál fyrir síðuna, eins og sýnt er á eftirfarandi sýnishorni.

![Að búa til nýja rás í Site Builder.](media/channel-mapping-4.png)

Síðan sem þú býrð til á þennan hátt verður tóm og mun ekki innihalda neinar síður (til dæmis heimasíða, flokkasíður og vörusíður).

Frekari upplýsingar eru í [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Búðu til nýja síðu með því að nota afritunaraðgerðina

Í stað þess að búa til glænýja, tóma síðu eins og lýst er í fyrri hlutanum, er betra að byrja með afrit af einni af upphafssíðunum sem eru til staðar í Commerce einingasafninu, eins og Fabrikam eða Adventure Works síðuna.

Til að afrita núverandi síðu, farðu á **Síður** listasíðu í vefsíðugerð og veldu **Afritaðu síðuna**. Þá, í **Afritaðu síðuna** valmynd sem birtist geturðu valið upprunasíðuna og tilgreint nafn áfangastaðarins.

Á þessum tímapunkti geturðu ekki enn valið sjálfgefna netrás og tungumál fyrir síðuna. Hins vegar geturðu stillt þessa eiginleika eftir að afritunaraðgerðinni hefur verið lokið. Þegar þú velur fyrst síðuna á **Síður** listasíða í Site Builder, the **Settu upp síðuna þína** svargluggi birtist þar sem þú getur valið sjálfgefna rás og tungumál.

Fyrir frekari upplýsingar um afritunaraðgerðina, sjá [Afritaðu netverslunarsíðu](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Hafa umsjón með núverandi vefrás

Eftir að síða hefur verið stillt með rás geturðu stjórnað og uppfært rásina innan valinnar síðu í vefsmiði á **Vefstillingar \> Rásir**, eins og sýnt er á eftirfarandi dæmi.

![Umsjón með rásarkortlagningu í vefsvæðisgerð.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Styðja margar síður í einum leigjanda

Margar vörumerkjasíður geta verið samhliða einum leigjanda. Eftirfarandi dæmi sýnir þrjár mismunandi vörumerkjasíður (Adventure Works, Adventure Works Business og Fabrikam), sem hver um sig er kortlögð á aðra eina netrás.

![Veflisti í vefsíðugerð.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Stilltu eitt lén með slóðum fyrir margar síður

Hægt er að nota eitt lén fyrir margar síður og síðan er hægt að nota slóðir til að aðgreina síður eða tungumál. Til dæmis, the`www.mycompany.com` lénið er stillt fyrir tvær mismunandi netviðskiptasíður: eina fyrir Fabrikam og eina fyrir Adventure Works. Í þessu tilviki er sjálfgefin slóð (`www.mycompany.com`), einnig þekkt sem auða slóðin, er hægt að nota fyrir Fabrikam síðuna og aðra slóð (til dæmis,`www.mycompany.com/adventureworks`) er hægt að nota fyrir Adventure Works síðuna. Annar valkostur er að nota sérsniðna slóð (til dæmis,`www.mycompany.com/fabrikam`) í stað sjálfgefna leiðar fyrir Fabrikam síðuna líka.

Að öðrum kosti er hægt að nota annað lén fyrir hverja síðu (til dæmis,`www.adventure-works.com` og`www.fabrikam.com`). Síðan er hægt að nota slóðir fyrir mismunandi tungumál eða svæði (td.`www.adventure-works.com/fr-ca` fyrir Kanada franska).

## <a name="configure-multiple-languages-on-a-site"></a>Stilltu mörg tungumál á síðu

Hægt er að stilla tungumál fyrir netverslunarsíðuna í vefsíðugerð á **Vefstillingar \> Rásir**. Í eftirfarandi sýnishorni hefur hvert tungumál verið stillt með því að nota staðarvalið fyrir slóðina, þannig að hvert tungumál hefur einstaka vefslóð.

![Mörg tungumál stillt á síðu.](media/channel-mapping-10.png)

Til að bæta við nýju rástungumáli skaltu fara á **Vefstillingar \> Rásir**, og veldu rásartengilinn. Í glugganum sem birtist hægra megin velurðu **Bættu við svæði** til að velja rásina og staðsetninguna sem þú vilt bæta við. Tilgreindu síðan slóðina sem á að nota fyrir valda rás.

### <a name="add-and-configure-the-site-picker-module"></a>Bættu við og stilltu vefvalseininguna

Eftir að þú hefur stillt síðu með mörgum tungumálum og/eða rásum gætirðu viljað bæta tungumálavali við síðuhaus síðunnar, svo að notendur geti valið tungumál sitt eða land handvirkt. Einingasafnið [hausareining](author-header-module.md) hefur innbyggðan stuðning fyrir notendur til að velja tungumál með því að nota [vefvalseining](site-selector.md). Hægt er að bæta síðuvalseiningunni við hauseininguna í hausbrotinu.

Fyrir frekari upplýsingar um hvernig á að bæta við og stilla vefvalseininguna, sjá [Vefsíðuvalseining](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Innleiða síðuafbrigði fyrir hvert tungumál

Í þessari atburðarás er aðeins ein rás, en það eru mörg tungumál. Þú getur breytt útliti síðu miðað við valið tungumál með því að búa til síðuafbrigði fyrir hana. Þú getur síðan bætt staðbundnu efni við afbrigðið.

Þegar þú ert með síðu opna í Site builder, og þú velur hlekkinn efst til hægri sem sýnir núverandi rás og tungumál, birtist rás og tungumálaval, eins og sýnt er í eftirfarandi dæmi. Ef þú vilt hnekkja síðunni fyrir núverandi tungumál skaltu velja annan stað og velja síðan **Breyta**. Þú getur líka skipt um rás ef þú ert það [stjórna síðu sem hefur margar rásir og tungumál](#manage-site-content-that has-multiple-channels-and-languages).

![Breyting á tungumáli fyrir síðu í Site builder.](media/channel-mapping-14.png)

Ef afbrigðið fyrir valda síðu eða brot hefur ekki enn verið búið til færðu viðvörunarskilaboð, eins og sýnt er á eftirfarandi dæmi. Í þessu tilviki skaltu velja **Búðu til síðuafbrigði** tengilinn í skilaboðatextanum. Glugginn sem birtist býður upp á valkosti sem gera þér kleift að byrja á afriti af núverandi afbrigði eða búa til glænýja síðu úr sniðmáti.

![Biðja um að búa til síðuafbrigði í vefsvæðisgerð](media/channel-mapping-16.png)

Ef þú býrð ekki til afbrigði er upprunalega síðan birt og sýnir viðeigandi tungumál fyrir einingastrengi og vöruupplýsingar frá höfuðstöðvum Commerce. Hins vegar, ef texti eins og síðutitill eða annað markaðsefni hefur verið tilgreint beint í sjálfgefnum síðueiningum, verða strengirnir fyrir þann texta áfram á frummálinu.

Í stað þess að búa til hverja síðu og brot handvirkt er hægt að flytja hverja síðu og brot út í XML Localization Interchange File Format (XLIFF) skrá sem síðan er hægt að senda til staðsetningar. Eftir að hvert XLIFF hefur verið staðfært er hægt að flytja það inn sem staðfært síðuafbrigði. Til að flytja XLIFF skrá af síðu eða broti í vefsvæðisgerð, eða til að flytja inn XLIFF skrá inn á síðu eða brot, veldu **Staðfærsla** á skipanastikunni. Veldu síðan annað hvort **Flytja út XLIFF** eða **Flytja inn XLIFF**, eins og sýnt er á eftirfarandi dæmi.

![Flytja inn eða flytja út síðu eða brot á XLIFF sniði.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Hafa umsjón með efni vefsvæðis sem hefur margar rásir og tungumál

Vefsvæði sem hefur margar rásir og/eða tungumál geymir einstakt afbrigði af hverri síðu og brot fyrir hverja samsetningu rásar og tungumáls. Þessi hegðun gerir síðuafbrigðum kleift að innihalda staðbundin gögn en gefur þér einnig sveigjanleika til að breyta útliti og yfirbragði síðu fyrir tiltekið afbrigði.

Sjá upplýsingar um hvernig á að vinna með síðuafbrigði [Innleiða síðuafbrigði fyrir hvert tungumál](#implement-page-variants-for-each-language) kafla þessa efnis.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Stilltu margar rásir á netverslunarsíðu

Þú getur bætt rásum við netverslunarsíðu í vefsíðugerð með því að fara á **Vefstillingar \> Rásir** og velja **Bættu við rás**. Þá, í **Bættu við rás** valmynd sem birtist geturðu valið netrásina og sjálfgefið svæði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit rása](channels-overview.md)

[Setja upp netrás](channel-setup-online.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Setja upp landfræðilega greiningu og áframsendingu](geo-detection-redirection.md)

[Virkja og nota deilingu milli rása](cross-channel-sharing.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Afrita svæði fyrir rafræn viðskipti](copy-ecommerce-site.md)

[Vefsíðuvalseining](site-selector.md)
