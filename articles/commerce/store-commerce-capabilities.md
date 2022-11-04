---
title: Store Commerce app getu
description: Þessi grein lýsir virkninni sem er í boði í Store Commerce appinu fyrir Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: d713cc0e9537ae20ffddee6e77779a16e74bd779
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/27/2022
ms.locfileid: "9728028"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce app getu

[!include [banner](includes/banner.md)]

Store Commerce appið er nútíma upplifun af sölustað (POS) fyrir Microsoft Dynamics 365 Commerce. Það gerir fyrirtækjum kleift að vinna úr færslum í verslun og stjórna bakvinnsluaðgerðum eins og birgðum og pöntunarvinnslu. Forritið gerir fyrirtækjum einnig kleift að stjórna viðskiptasamskiptum með tryggð og viðskiptavina. 

Keyrt af Commerce Scale Unit (CSU), Store Commerce appið býður upp á fullkomna allsherjarlausn. Til dæmis getur viðskiptavinur keypt vöru á netinu og sótt hana í nálægri verslun og haldið þannig áfram verslunarferð sinni yfir rásir án þess að tapa neinum gögnum. 

Þessi grein veitir yfirlit yfir möguleika Store Commerce appsins.

## <a name="platform"></a>Kerfi

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Omni-rás | Dynamics 365 Commerce býður upp á alhliða alhliða lausn sem sameinar bakskrifstofu, verslun, símaver og stafræna upplifun. | [Yfirlit](index.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Viðskipti án framvinnslu | Commerce Scale Unit hýsir höfuðlausu viðskiptavélina. Höfuðlausa viðskiptavélin þjónar sem miðpunktur allra viðskiptarökfræði og knýr fullkomna allsherjarlausn. | <p>[Yfirlit yfir arkitektúr](commerce-architecture.md)</p><p>[Höfuðlaus arkitektúr](dev-itpro/retail-server-architecture.md)</p> | [Tæknispjall](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Höfuðstöðvar viðskipta bjóða upp á bakskrifstofugetu sem gerir kleift að stilla vörur, starfsmenn, viðskiptaferla, verðlagningu og aðra virkni sem er nauðsynleg fyrir fyrirtækið. | [Yfirlit yfir arkitektúr](commerce-architecture.md) | |
| Sölustaður (POS) | Store Commerce appið er POS upplifunin fyrir Dynamics 365 Commerce. Það býður upp á eiginleikaríka og alhliða POS-getu sem hjálpa söluaðilum, gjaldkerum og stjórnendum að veita framúrskarandi þjónustu við viðskiptavini. Að auki býður það upp á nokkra dreifingarvalkosti fyrir smásala, hjálpar til við að bæta árangur og býður upp á bætta líftímastjórnun (ALM). | [Verslun verslun app](dev-itpro/store-commerce.md) | <p>[Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Myndband](https://youtu.be/7B332XH_zfs)</p><p>[Flutningur frá MPOS til Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Uppsetning skýs | Hægt er að nota mörg tilvik af Commerce Scale Units fyrir álagsdreifingu og landfræðilega nálægð. | [Uppsetning skýs](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Starfsmenn á staðnum | Með því að nota staðbundna viðskiptagagnauppfærslu geta Commerce-viðskiptavinir haft meira eignarhald og stjórnun á Dynamics 365 umhverfi. | [Uppsetning á staðnum](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Tækjastjórnun

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Margir formþættir | Store Commerce appið er stutt á mörgum formþáttum tækja, svo sem tölvum, spjaldtölvum og fartækjum. Móttækilegt notendaviðmótið (UI) gerir útlitinu kleift að breyta stærð sjálfkrafa og aðlaga að skjástærðinni. | [Sjónrænar stillingar](pos-screen-layouts.md) | |
| Þverpallur | Store Commerce appið er stutt á vefnum, Windows, iOS og Android pallar. | [Pallar](dev-itpro/hybridapp.md) | |
| Vörumerki | Skjáhönnuðurinn gerir þér kleift að sérsníða skjáskipulag til að mæta viðskiptakröfum þínum. Að auki er hægt að búa til þemu, útlit, liti og myndir út frá hlutverkum starfsmanna og síðan er hægt að deila þeim á milli notenda til að tryggja samræmi vörumerkis og auðvelda notkun. | [Sjónrænar stillingar](pos-screen-layouts.md) | [Myndband](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Grannfræði | Mismunandi staðfræði í verslunum er studd, byggt á framboði á neti. | <p>[Grannfræði](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografík](dev-itpro/retail-in-store-topology.md)</p> | |
| Fjöltækjastjórnun | Auðvelt er að stjórna mörgum tækjum í verslunum frá höfuðstöðvum Commerce. | [Virkjun](set-up-activation-accounts-validate-devices-hq.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Starfsmannahald

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Skráðu þig inn | Hver starfsmaður verslunarinnar getur haft sérstaka innskráningu. Innskráningargerðir innihalda notendanafn, strikamerki, segulröndalesara (MSR), líffræðileg tölfræði og Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Lengri innskráningu](extended-logon.md)</p> | |
| Aðgangsheimildir | Mismunandi heimildir eru studdar fyrir starfsmenn, svo sem heimild til að búa til pantanir og heimild til að breyta pöntunum. | [Aðgangsheimildir](tasks/create-pos-permission-groups.md) | |
| Tíma- og mætingarstjórnun | Hægt er að stjórna mætingu með því að nota tímaklukkuaðgerðina. Hægt er að vinna mætingargögn í launaskrá með því að nota Dynamics 365 Human Resources app. | [Tímastjórnun](retail-time-attendance.md) | |
| Söluþóknun | Sölu getur verið rekið af sölufulltrúa til að reikna út þóknun eða aðra hvata. | [Þóknun](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Smásala

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Stjórnun vöruúrvals | Vörustjórar geta flokkað vörur þannig að þær séu til sölu í ákveðinni rás og á tilteknu tímabili. | [Úrval](assortments.md) | |
| Vörulistar | Vörustjórar geta stjórnað vörulistum til að auðkenna vörurnar sem þú vilt bjóða með vörulistasértækri verðlagningu. | [Vörulistar](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Vöru- og flokkastjórnun | Í höfuðstöðvum viðskipta geta sölustjórar búið til vörur sem hafa afbrigði, eiginleika, mælieiningu og svo framvegis. Þeir geta einnig skilgreint flokkastigveldi til að skipuleggja vörur. | [Afurð](retail-hierarchies.md) | |
| Búnt | Vörustjórar geta flokkað vörur þannig að þær séu seldar sem búnt eða sett. | [Sett](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Upplýsingakóðar | Notaðu upplýsingakóða til að biðja gjaldkera um að slá inn upplýsingar við mismunandi aðgerðir á POS, eins og vörusölu, vöruskilum eða vali viðskiptavina. | [Upplýsingakóðar](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Tengd atriði | Notaðu tengda hluti til að selja vörur þegar hlut er bætt við færslu. | [Tengd atriði](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Ábyrgðir | Hægt er að selja aukna ábyrgð ásamt vörum. | [Ábyrgð](extended-warranty.md) | |
| Prentun merkimiða | Hægt er að búa til merkimiða sem innihalda vöruupplýsingar eins og lotunúmer, raðnúmer og fyrningardagsetningu. | [Prentun merkimiða](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Aðstoð við sölu

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Finna afurð | Skoðaðu vörur eftir flokkum. | [Afurðarstigveldi](retail-hierarchies.md) | |
| Afurðaleit | Leitaðu að vörum eftir nafni og fínstilltu leit með því að nota vörueiginleika eins og vörumerki, verð og efni. Þessi möguleiki er knúinn af Azure Cognitive Search. | [Skýknún leit](cloud-powered-search-overview.md) | |
| Síðan Upplýsingar um afurð | Ríkar vöruupplýsingarsíður geta innihaldið myndir, lýsingu, vörueiginleika og ráðlagðar vörur. Tilmælin eru knúin áfram af meðmælaþjónustunni. | | |
| Vara bera saman | Berðu saman margar vörur og hjálpaðu viðskiptavinum að velja eina og bæta henni við viðskipti. | | |
| Endalaus gangur | Flettu auðveldlega upp birgðum í öðrum verslunum og búðu til pantanir. | [Birgðauppfletting](pos-inventory-lookup-operation.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Ráðleggingar | Auka- og krossselja vörur með því að nota meðmælaþjónustuna. Þessi þjónusta notar einkaleyfisbundna tækni til að leggja til ráðleggingar, byggðar á innkaupaþróun og eiginleikum eins og nýkomnum, svipuðu útliti og metsölu. Þessar ráðleggingar eru fáanlegar á vöruupplýsingasíðum, the **Upplýsingar um viðskiptavini** síðu, og **Viðskipti** síðu. | [Ráðleggingar](product-recommendations.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Viðskiptavinasamband

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Umsjón viðskiptavina | Búðu til, breyttu og stjórnaðu viðskiptavinareikningum. Hægt er að stjórna reikningum viðskiptavina í ósamstilltri stillingu til að forðast vinnslu í rauntíma. | [Stjórnun](customer-mgmt-stores.md) | |
| Eigindir viðskiptavinar | Viðskiptavinaeiginleikaramminn gerir kleift að fanga viðbótar viðskiptavinatengd gögn út frá viðskiptakröfum. | [Eigindir](dev-itpro/customer-attributes.md) | |
| Upplýsingar síðu viðskiptavina | Ríkuleg upplýsingasíða um viðskiptavini veitir allsherjarsýn yfir samskipti viðskiptavinarins á öllum rásum. Þessi samskipti fela í sér kaup, óskalista og vildarpunkta. | | |
| Viðskiptavinaleit í skýinu | Leitaðu að viðskiptavinum eftir nafni, símanúmeri, netfangi, vildarkorti, heimilisfangi og svo framvegis. | [Skýknún leit](pos-search-improvements.md#customer-search) | |
| Tryggð og umbun | Viðskiptavinir geta tekið þátt í vildarkerfum og unnið sér inn og innleyst vildarpunkta á milli rása. | [Vild](set-up-customer-loyalty-program.md) | |
| Biðlaraþjónusta | Hafa umsjón með lykilviðskiptavinum með því að nota viðskiptavinabók og fylgjast með athöfnum og athugasemdum á viðskiptavinasniðinu. Dynamics 365 Customer Insights samþætting við skulum verslunarstarfsmenn fá vísbendingar um næstbestu aðgerðina fyrir hvern viðskiptavin. | [Biðlaraþjónusta](clienteling-overview.md#activities-and-notes) | |

## <a name="pricing-and-discounts"></a>Verðlagning og afslættir

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Viðskiptasamningar | Verðlagsstjórar geta notað viðskiptasamninga til að skilgreina sérverð, byggt á langtímasamningum fyrir tiltekna viðskiptavini. | [Verð](price-management.md)| [Myndband](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Sölusamningar | Verðlagsstjórar geta notað sölusamninga til að skilgreina samningsbundið verð í viðskiptasviðum (B2B). | [Verð](price-management.md) | |
| Verðleiðréttingar | Verðlagsstjórar geta notað verðleiðréttingarmöguleikann til að búa til, fylgjast með og stjórna verðlækkunum fyrir vörur sínar með tímanum. | [Verðleiðréttingar](price-adjustments-discounts.md) | |
| Afslættir | Verðlagsstjórar geta sett upp nokkrar tegundir af afslætti til að keyra ýmsar kynningar. Þessir afslættir fela í sér einfalda afslætti, magnafslátt, viðmiðunarafslátt, blanda afslætti, tilboðsbundinn afslátt og sendingarafslátt. | [Afslættir](retail-discounts-overview.md) | |
| Afsláttarmiðar | Verðstjórar geta sett upp afsláttarmiða eða strikamerki, tengt þá við afslætti og dreift þeim til viðskiptavina. Söluaðilar geta bætt afsláttarmiðum við sölufærslur eða fjarlægt þá. | [Afsláttarmiðar](coupons.md) | |
| Verðflokkar | Verðlagsstjórar geta notað verðflokkahæfileikann til að skilgreina samhengisverð, byggt á rásum, vörulistum, tengingum eða vildarkerfum. | [Verð](price-management.md) | |
| Kynningar í boði | Söluaðilar geta auðveldlega flett upp tiltækum kynningum á vörum í verslun, vörum sem hefur verið bætt við færslu og svo framvegis. | [Verðlagningaraðgerðir](pos-pricing-functions.md) | |
| Verðkannanir | Söluaðilar geta fljótt athugað virk söluverð á vörum í versluninni. | [Verðlagningaraðgerðir](pos-pricing-functions.md) | |
| Verðhnekking | Söluaðilar sem hafa nauðsynlegar heimildir geta hnekkt kerfisstillt eða reiknað verð. | [Verðlagningaraðgerðir](pos-pricing-functions.md) | |
| Handvirkir afslættir | Söluaðilar sem hafa nauðsynlegar heimildir geta beitt handvirkum afslætti á sölufærslur eða sölulínur. | [Verðlagningaraðgerðir](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Rafrænar greiðslur

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Kredit og debet | Store Commerce appið styður helstu kredit- og debetkortagreiðslur í gegnum Adyen Payment Gateway og pöntunaruppfyllingu í gegnum PayPal. Payments SDK gerir ráð fyrir ytri gáttartengingum sem eru studdar af samþættingum óháðra hugbúnaðarframleiðenda (ISV). | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Greiðslur](payment-methods.md)</p> | <p>[Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Stuðningur við stafrænt veski | Store Commerce appið styður greiðslur með greiðslumáta með stafrænum veski sem nota ekki BIN (Bank Identification Number) svið eins og hefðbundin kredit- og debetkort gera. Hægt er að kortleggja greiðslumáta við stafrænar veskisgreiðslur eins og Adyen. | [Veski](wallets.md) | |
| Stuðningur við gjafakort | Bankaauðkennisnúmer Dynamics 365 gjafakort, Stored Value Solutions (SVS) og Givex gjafakort. Gjafakort er hægt að kaupa og innleysa í pöntun. | [Gjafakort](dev-itpro/gift-card.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Svikavörn | Dynamics 365 Fraud Protection hjálpa þér að koma í veg fyrir sviksamlega starfsemi og finna staði þar sem svik gætu verið óséð. | [Svikavörn](dev-itpro/dfp.md) | [Myndband](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Skattar og gjöld

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Skattar | Store Commerce appið styður margar tegundir af óbeinum sköttum, svo sem söluskatti, virðisaukaskatti (VSK), vöru- og þjónustuskatti (GST), einingartengdum gjöldum og staðgreiðslu. | [Skattar](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Gjöld | Hægt er að stilla gjöld á línustigi, á hausstigi, sem sjálfvirk gjöld, eftir rás, og svo framvegis. | [Gjöld](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Afgreiðsla og uppfylling pantana

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Stofnun pöntunar | Hægt er að búa til pöntun fyrir sendingu eða til afhendingar í nærliggjandi verslun. Hægt er að útvega tíma til að sækja. | [Yfirlit](customer-orders-overview.md) | |
| Breyting á pöntun | Hægt er að breyta pöntun, skila henni, hætta við og svo framvegis. | <p>[Hætta við](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Vöruskil](pos-returns.md)</p> | |
| Leita á | Leitaðu að og síaðu pantanir með því að nota pöntunarsértækar upplýsingar. | [Leita á](enhancedorderrecall.md) | |
| Eigindir pöntunar | Pantunareiginleikaramminn gerir kleift að fanga frekari pöntunartengdar upplýsingar byggðar á viðskiptakröfum. | [Eigindir](dev-itpro/order-attributes.md) | |
| Bein afhending | Hægt er að merkja vörur fyrir beina afhendingu frá seljanda á heimilisfang viðskiptavinar. Bein sending er einnig þekkt sem sendingarkostnaður. | [Bein afhending](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Tilboð | Starfsmenn verslunarinnar geta búið til tilboð fyrir viðskiptavini og tilgreint sérstakt verð, handvirka afslætti og gildistíma tilboðsins. | [Tilboð](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Uppfylling | Verslanir geta valið, pakkað og sent pantanir. Hægt er að bæta fylgiseðli við þá pakka sem eru tilbúnir til sendingar. | [Uppfylling](order-fulfillment-overview.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021) |
| Dreifingarstjórnun pöntunar | Store Commerce appið styður snjalla pöntunaruppfyllingu hagræðingar þar sem hægt er að stilla viðskiptaáætlanir út frá eðli fyrirtækisins, tegund viðskiptavinar, uppruna pöntunar og afhendingaraðferð pöntunar. | [DOM](dom.md) | |

## <a name="inventory-management"></a>Birgðir

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Dreifing frá lager | Hagræða dreifingu á tiltækum birgðum frá dreifingarmiðstöð til margra verslana eða vöruhúsa. | [Dreifing frá lager](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Dreifing frá dreifingarstöð | Hagræða dreifingu birgða á komandi innkaupapantunum til margra verslana eða vöruhúsa. | [Dreifing frá dreifingarstöð](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Birgðir á innleið | Taktu á móti birgðum frá lánardrottni í gegnum innkaupapöntun, eða frá öðru vöruhúsi með flutningspöntun. Stofna innkaupapöntun á innleið eða flytja pöntunarbeiðni. | [Á innleið](pos-inbound-inventory-operation.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Birgðir á útleið | Sendu birgðir til annars vöruhúss með flutningspöntun og búðu til beiðni um flutningspöntun á útleið. | [Á útleið](pos-outbound-inventory-operation.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Birgðauppfletting | Athugaðu tiltækar birgðir fyrir vörur í verslunum og vöruhúsum og athugaðu birgðahald sem er tiltækt til að lofa (ATP) á framtíðardagsetningum. | [Birgðauppfletting](pos-inventory-lookup-operation.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Leiðrétting birgða | Breyttu birgðum inn í eða út úr vöruhúsi verslunar til að uppfylla sérstakar viðskiptakröfur án þess að nota sölu, kvittun eða endurtalningu. | [Leiðrétting birgða](work-with-store-inventory.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Birgðatalning | Telja efnislegar birgðir og stilla bókhaldsbirgðir kerfisins til að passa við þær. | [Talning](work-with-store-inventory.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Birgðahreyfing | Færa birgðir á milli staða í verslun. | [Hreyfing](work-with-store-inventory.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |

## <a name="financials"></a>Fjármál

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Reiðufjárstjórnun | Store Commerce appið styður stjórnun á reiðufé og öðrum tilgreindum tilboðum í versluninni. Að auki er hægt að virkja vaktaafstemmingu í versluninni fyrir háþróaða peningastjórnunarmöguleika. | [Innlausn](cash-mgmt.md) | |
| Ársreikningur og afstemming | Handbært fé og færslur fyrir verslun eru skráðar í höfuðstöðvum Commerce í gegnum bókunarferli yfirlits. | [Uppgjör](retail-statements.md) | |
| Tekju- og gjaldaviðskipti | Vinnið úr smápeningum í versluninni og skráið tekjur sem koma ekki á hefðbundinn hátt, eins og týndir peningar, hlutdeild tekna af kaffihúsi í anddyrinu og teppahreinsun. | [Uppgjör](retail-statements.md) | |
| Reikningsgreiðslur | Handtaka greiðslur á móti reikningum. | [Reikningur](payinvoice.md) | |

## <a name="employee-productivity"></a>Framleiðni starfsmanna

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Verkstjórnun | Búðu til verkefnalista og verkefni og úthlutaðu þeim til verslana og starfsmanna. Fylgstu með stöðu verkefna þvert á verslanir. Óaðfinnanlegur samþætting við Microsoft Teams er gefið. | <p>[Verkefnastjórnun](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Myndband](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Vélbúnaður og jaðarbúnaður

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Tengdu jaðartæki | Tengdu jaðartæki eins og prentara, peningaskúffur, skanna og greiðslutæki við POS útstöð. | [Jaðarbúnaður](retail-peripherals-overview.md) ||
| Deildu jaðartækjum | Hægt er að deila kvittunarprenturum, peningaskúffum og greiðslutækjum á milli margra útstöðva með því að tengja þá við sameiginlega vélbúnaðarstöð. | <p>[Vélbúnaðarstöð](retail-peripherals-overview.md) ||
| POS og jaðarhermir | Jaðarhermirinn styður prófun á atburðarásum sem venjulega krefjast líkamlegra POS jaðartækja. Það felur einnig í sér POS hermi sem hægt er að nota til að prófa samhæfni líkamlegra jaðartækja án þess að þurfa að nota POS viðskiptavininn. | [Hermir](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Móttökur

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Prentaðu kvittanir | Kvittanir af ýmsu tagi, svo sem sölukvittanir, kreditkortakvittanir, gjafakvittanir og reikningar, er hægt að prenta sjálfgefið eða eftir staðfestingu gjaldkera við útskráningu. Einnig er hægt að endurprenta þær úr tímaritinu. | [Til prentunar](receipt-templates-printing.md) | |
| Kvittanir með tölvupósti | Hægt er að senda kvittanir í tölvupósti frá POS eftir að greiðslu er lokið. | [Tölvupóstur](email-receipts.md) | |
| Hönnunarkvittanir | Hægt er að sérsníða verslunarkvittanir þannig að þær sýni gögn og útlit sem eru viðeigandi fyrir söluaðila og færslugerð. Einnig er hægt að framlengja kvittanir þannig að þær sýni sérsniðin gögn sem smásali þarfnast. | [Hönnun](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Ótengdur stuðningur

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Ótengt án truflunar | Óaðfinnanlegur án nettengingar gerir þér kleift að halda áfram að eiga viðskipti jafnvel þegar nettenging er takmörkuð eða ekki tiltæk. Útilokun gagna hjálpar þér að minnka gagnastærð ótengdu gagnagrunnanna og hámarka afköst. | [Ótengt](pos-operations.md) | |
| Árangursmiðað skipti | Skiptu yfir í offline þegar frammistöðurýrnun greinist. | [Ótengt](dev-itpro/implementation-considerations-offline.md) | [Myndband](https://youtu.be/sQU-2pgHToI) |
| Ótengdur mælaborð | The **Ótengdur staða** mælaborð sýnir ónettengda stöðu, villur og upplýsingar um gögnin fyrir hvert tæki. Þess vegna er auðvelt að stjórna stöðu margra tækja. | [Ótengt](dev-itpro/implementation-considerations-offline.md) | [Myndband](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Stækkunarhæfni

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Commerce Headquarters | Hægt er að aðlaga lausnir fyrir höfuðstöðvar viðskipta með því að bæta við eða breyta viðskiptaferlum. Höfuðstöðvar viðskipta styðja notkun lýsigagna og kóðadrifið framlengingarlíkan til að bæta við sérsniðnum virkni. Það er auðvelt að samþætta það í ytri lausnir. | [Yfirlit](dev-itpro/extend-customer-cdx-package.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Höfuðlaus viðskipti | Hægt er að nota Extensible Omni-channel API ramma til að sérsníða og bæta við viðskiptarökfræði. Forritaskil sem hafa beiðnameðferðaraðila og framlengingarmynstur fyrir og eftir kveikju. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK inniheldur kóðann, kóðasýni, sniðmát og verkfæri sem þarf til að framlengja eða sérsníða Dynamics 365 Commerce virkni. SDK er birt í mismunandi geymslum (repos) í GitHub, allt eftir viðbótahlutunum. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Sölustaður | Store Commerce appið er hægt að útvíkka sjálfstætt með því að nota POS framlengingareiginleika Commerce SDK. Ramminn styður aðlögun notendaupplifunar (UX), verkflæðis og viðskiptarökfræði. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Tæknispjall](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Skýrslugerð

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Söluskýrslur | Söluskýrslur eftir starfsfólki, skrá, greiðslutegund, skilum, vöru og svo framvegis eru aðgengilegar verslunarstjórum. Stjórnendur geta skoðað þessar skýrslur og notað þær til að úthluta þóknun og bera kennsl á vöruþróun. | | |

## <a name="diagnostics"></a>Greining

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Rekstrarleg innsýn | Heilsuáreiðanleiki og frammistöðumælingar í verslun eru fáanlegar hjá viðskiptavininum Application Insights Áskrift. Ítarlegri viðvörunar- og eftirlitsgetu er til staðar. | | |
| Ástandsskoðun | Hægt er að sannreyna framboð á jaðartækjum sem eru tengd við POS með því að keyra heilsuskoðunaraðgerðina. Síðan er hægt að laga og sannreyna einstök jaðarmál. | [Ástandsskoðun](pos-healthcheck.md) | [Myndband](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Staðfæring

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Fjölmarkaðsstuðningur | Markaðssértækir eiginleikar eins og fjárhagsleg samþætting, GST, háþróuð reikningagerð og fyrirframgreiðslur eru studdar út úr kassanum. Þessi hæfileiki nær yfir nokkra markaði í Evrópu, Ameríku, Rússlandi, Asíu, Sádi Arabíu og svo framvegis. | [Staðfæring](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Samræmi

| Geta | Lýsing | Fylgiskjöl | Viðbótarefni |
|---|---|---|---|
| Microsoft staðlar | Store Commerce appið uppfyllir staðla Microsoft fyrir öryggi, persónuvernd, aðgengi, almennu gagnaverndarreglugerðina (GDPR), gagnamörk Evrópusambandsins (ESB) og svo framvegis. | | |

