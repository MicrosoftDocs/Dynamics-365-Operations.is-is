---
title: Velja á milli Modern POS (MPOS) og Cloud POS
description: Þetta efnisatriði útskýrir grundvallarmuninn á milli Modern POS og Cloud POS. Það lýsir einnig ýmsum þáttum sem smásalar sem innleiða Dynamics 365 Commerce ættu að íhuga til að fá hjálp við að velja besta kostinn út frá kröfur þeirra.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d636e80ba853191516b970ff3f1dece02ee771ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206872"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Velja á milli Modern POS (MPOS) og Cloud POS

[!include [banner](includes/banner.md)]

Þetta efnisatriði gefur þeim sem innleiða viðbótarbakgrunn, ábendingar og leiðbeiningar um þá þætti sem þeir ættu að íhuga þegar þeir virkja Dynamics 365 Commerce. Með því að skoða og fylgja þessum leiðbeiningum sem hluta af virkjunarferlinu geta þeir sem innleiða forðast vandamál sem gætu haft áhrif á ánægju notanda eða afköst.

## <a name="insights"></a>Innsýn

Commerce veitir fjölbreytt úrval af virkjunar- og grannfræðikostum. Þess vegna geta smásalar valið þær einingar og grunnstillingar sem best mæta viðskipta- og tæknikröfum þeirra. Einn þáttur í virkjun sem krefst vandaðrar íhugunar er val á vettvangi og formþætti fyrir einingu sölustaðar (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Íhugunarefni tengd POS vettvangur og formþættir

Commerce styður eftirfarandi valkosti fyrir sölustað (POS):

- Modern POS (MPOS) fyrir Microsoft Windows
- MPOS fyrir Microsoft Windows síma
- MPOS fyrir Apple iPad eða Google Android spjaldtölvu
- Cloud POS (CPOS), sem styður Microsoft Edge, Internet Explorer og Google Chrome vafra

Í öllum tilvikum deilir POS (MPOS og CPOS) sama kjarnaforritakóða. Þetta atriði er mikilvægt af eftirfarandi ástæðum:

- Notendaviðmótið (UI) er sjálfkvæmt, án tillits til vettvangs eða formþáttar.
- Meirihluti virknieiginleikanna er sá sami, án tillits til vettvangs eða formþáttar. Þó er til staðar mikilvægur munur. Munurinn er skýrður í þessu efnisatriði.
- Í tiltekinni verslun er hægt að sameina POS afbrigði og þau verið í keyrslu samhliða. Til dæmis, fyrir helstu skrár sínar, smásali getur notað MPOS á tölvum sem keyra Windows. Hins vegar getur smásalinn bætt við þeim skrám með afgreiðslustöðvum eða farsímum sem tengjast vafra.
- Sérstillingar og viðbætur geta hæglega verið notaðar yfir vettvang og formþætti. Vegna þess að kjarnaforritskóðanum er deilt, er hægt að innleiða flestar sérstillingar einu sinni í staðinn fyrir mörgum sinnum.

### <a name="mpos-vs-cpos"></a>MPOS samanborið við CPOS

Þótt MPOS og CPOS séu að mestu þau sömu, þá eru nokkur mikilvæg munur sem þú verður að skilja.

#### <a name="mpos"></a>MPOS

MPOS á Windows, IOS eða Android tæki er forrit sem er pakkað, sett upp og þjónustað á því tæki.

- **Windows** - MPOS fyrir Windows forritið inniheldur alla forritakóðann og innfelldan Commerce-keyrslutíma (CRT). 
- **iOS/Android** – Á þessum vettvangi virkar forritið sem gestgjafi fyrir CPOS forritakóðann. Með öðrum orðum kemur forritakóðinn frá CPOS-þjóninum á Microsoft Azure eða Commerce Scale Unit. Frekari upplýsingar, sjá [Yfirlit Commerce Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Vegna þess að CPOS keyrir í vafra er forritið ekki uppsett á tækinu. Í staðinn fær vafrinn aðgang að forritskóðanum frá CPOS þjóninum. Þess vegna hefur CPOS ekki beinan aðgang að POS vélbúnaði eða getur unnið án nettengingar.

### <a name="store-deployment-considerations"></a>Íhugunarefni tengd virkjun í verslun

Til viðbótar við vettvang og formþátt, verða smásalar einnig að velja virkjunarvalkost í versluninni. Eftirfarandi tafla sýnir grunnstillingarnar sem eru tiltækar fyrir hvern POS valkost.

| POS forrit         | Commerce Scale Unit | Tiltæk utan nets |
|-------------------------|---------------|-------------------|
| MPOS fyrir Windows        | Cloud eða RSSU | Já               |
| MPOS fyrir iOS eða Android | Cloud eða RSSU | Nr                |
| Sölustaður í skýi               | Cloud eða RSSU | Nr                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Skalaeining viðskiptanna er hluti sem hýsir CRT. CRT inniheldur allan viðskiptagrunn sem POS notar, og það veitir aðgang að rás gagnagrunninum. Á meðan þeir eru nettengdir, nota allir POS viðskiptavinir í versluninni Commerce Scale Unit. Commerce Scale Unit er hægt að virkja annaðhvort í skýinu eða í versluninni.

#### <a name="offline-mode"></a>Ótengdur hamur

MPOS fyrir Windows styður ótengdan ham. Í ótengdum ham getur POS áfram unnið með sölu jafnvel þótt það sé aftengt frá Commerce Scale Unit. Síðan hægt að samstilla það með rásargagnagrunninum þegar tenging er endurheimt. MPOS notar eigið innleitt tilvik af CRT og notar tímabundið eigin staðbundna gagnaveitu (ótengdur SQL gagnagrunnur þjóns). Sjá [POS virkni án nettengingar](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality) til að fá nánari upplýsingar um virkni án nettengingar.

### <a name="pos-peripheralhardware-considerations"></a>POS jaðarbúnaður/vélbúnaður íhugunarefni

Söluaðilar verða einnig að íhuga hvernig POS mun fá aðgang að tækjum og jaðartæki, svo sem prentara, reiðuféskúffum og greiðslustöðvum. Aðeins MPOS fyrir Windows styður bein samskipti við þessi tæki. MPOS fyrir Windows Síma, IOS eða Android, og Cloud POS krefst vélbúnaðarstöðvar til að fá aðgang að þessum tækjum. Vélbúnaðarstöðvar geta verið tileinkaðar POS afgreiðslukassa eða deilt meðal afgreiðslukassa í verslun. Frekari upplýsingar um vélbúnaðarstöðvar, sjá [Grunnstilling og uppsetning Retail-vélbúnaðarstöðvar](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Umhugsunarefni fyrir innleiðingu

Íhugaðu eftirfarandi upplýsingar þegar þú skipuleggur POS innleiðingu þína í verslunum þínum:

- **Virknikröfur** - Grunnviðskiptaferli og færni eru þau sömu, óháð vettvangi, formþáttur eða grannfræði virkjunar. Þess vegna þurfa flestir smásalar ekki að íhuga virknikröfur þegar þeir skipuleggja innleiðingu sína.
- **Tengigeta** – Tiltækt net (víðnet \[WAN\] og staðarnet \[LAN\]) er stór þáttur sem krefst vandlegrar íhugunar. Allir ávinningur sem núll-fótspor, ský-hýsing lausn færir notanda í tengslum við kostnað og einfaldleika glatast ef kerfið er ekki í boði fyrir mikilvæg viðskiptaferli.

    Nema tengigeta fyrir tiltekið tæki sé mjög áreiðanleg og sterk, eða nema ákveðið langur óvirkur tími sé viðunandi fyrir smásalann, mælum við með einum af eftirtöldum valkostum:

    - Nota MPOS í Windows, og virkja ótengdan ham.
    - Dreifa viðskiptamælikvarðaeiningunni á staðnum.

    Þessir tveir valkostir útiloka ekki hvorn annan. Fyrir sem áreiðanlegasta grannfræði, geta smásalar virkjað staðbundið RSSU til að þurfa ekki að vera eins háðir nettengingu eða Azure framboði, og þeir geta einnig virkjað POS afgreiðslukassa þar sem ótengdur hamur er settur í gang ef vandamál koma upp varðandi staðbundinn þjón eða net.

- **Vélbúnaður tæki/jaðartæki** - Einn mikilvægur þáttur í Retail POS kerfi er hæfni þess til að nota POS jaðartæki eins og prentara, reiðufjárskúffur og greiðslustöðvar. Þó að allar tiltækar POS valkostir geti notað jaðartæki, styður aðeins MPOS fyrir Windows þau beint. Fyrir öll önnur forrit þarf eina eða fleiri vélbúnaðarstöðvar. Þrátt fyrir að þessi nálgun bætir sveigjanleika, verða fleiri einingar að vera uppsett, grunnstilltir og þjónustaðir.
- **Kerfisskilyrði** - Kerfisskilyrðin fyrir POS forritið eru mismunandi. Vertu viss um að athuga nýjustu upplýsingar áður en þú velur. Til dæmis, vegna þess að CPOS keyrir í vafra styður það fjölbreyttar stýrikerfi. Fyrir frekari upplýsingar um kerfisskilyrði, sjá [Kerfisskilyrði fyrir uppsetningu í skýi](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Uppsetning og þjónusta** - Flækjustig uppsetningar- og þjónustuskilyrði geta verið breytilegt eftir því hvaða forrit og uppsetning eru valin. Til dæmis, fyrir ský-hýst CPOS uppsetningu, þú þarft ekki að setja upp og uppfæra í hverju tæki. Þess vegna minnkar þessi aðferð flækjustig og kostnað mikið. Hins vegar, ef þú setur upp MPOS á hvert afgreiðslukassa og virkjar ótengdan ham, og setur einnig upp samnýttar vélbúnaðarstöðvar, eykur þú mjög fjölda endastöðva sem þarf að stjórna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]