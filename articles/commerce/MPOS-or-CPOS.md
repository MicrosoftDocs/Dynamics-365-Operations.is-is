---
title: Veldu á milli Store Commerce og sölukerfis í skýinu
description: Þessi grein útskýrir lykilmuninn á Store Commerce og Cloud POS og lýsir ýmsum þáttum sem smásalar sem innleiða Dynamics 365 Commerce ætti að íhuga að hjálpa þeim að velja besta valið fyrir kröfur þeirra.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26f6e94b13b3058ac42c4c7b83dcf7179bae18e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854007"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Veldu á milli Store Commerce og sölukerfis í skýinu

[!include [banner](includes/banner.md)]

Þessi grein útskýrir lykilmuninn á Store Commerce og Cloud POS og lýsir ýmsum þáttum sem smásalar sem innleiða Dynamics 365 Commerce ætti að íhuga að hjálpa þeim að velja besta valið fyrir kröfur þeirra. Það gefur einnig framkvæmdaaðilum viðbótarbakgrunn, ábendingar og leiðbeiningar um þætti sem þeir ættu að hafa í huga þegar þeir nota Dynamics 365 Commerce. Með því að skoða og fylgja þessum leiðbeiningum sem hluta af virkjunarferlinu geta þeir sem innleiða forðast vandamál sem gætu haft áhrif á ánægju notanda eða afköst.

## <a name="insights"></a>Innsýn

Commerce veitir fjölbreytt úrval af virkjunar- og grannfræðikostum. Þess vegna geta smásalar valið þær einingar og grunnstillingar sem best mæta viðskipta- og tæknikröfum þeirra. Einn þáttur í virkjun sem krefst vandaðrar íhugunar er val á vettvangi og formþætti fyrir einingu sölustaðar (POS).

### <a name="pos-platform-and-form-factor-considerations"></a>Íhugunarefni tengd POS vettvangur og formþættir

Commerce styður eftirfarandi valkosti fyrir sölustað (POS):

- Verslun Verslun fyrir Microsoft Windows
- Store Commerce fyrir iOS og Android
- Cloud POS (CPOS), sem styður Microsoft Edge og Google Chrome vafra
- Nútíma POS (MPOS) fyrir Microsoft Windows (MPOS verður úrelt í október 2023.) 

Í öllum tilvikum deilir POS (Store Commerce og CPOS) sama kjarnaforritakóða. Þetta atriði er mikilvægt af eftirfarandi ástæðum:

- Notendaviðmótið (UI) er sjálfkvæmt, án tillits til vettvangs eða formþáttar.
- Meirihluti virknieiginleikanna er sá sami, án tillits til vettvangs eða formþáttar. Þó er til staðar mikilvægur munur. Þessi munur kemur fram í þessari grein.
- Í hverri verslun er hægt að sameina POS-afbrigðin og geta keyrt samtímis. Til dæmis, fyrir aðalskrár sínar, getur smásali notað Store Commerce á tölvum sem keyra Windows. Hins vegar getur smásalinn bætt við þeim skrám með afgreiðslustöðvum eða farsímum sem tengjast vafra.
- Sérstillingar og viðbætur geta hæglega verið notaðar yfir vettvang og formþætti. Vegna þess að kjarnaforritskóðanum er deilt, er hægt að innleiða flestar sérstillingar einu sinni í staðinn fyrir mörgum sinnum.

### <a name="store-commerce-vs-cpos"></a>Verslun vs CPOS

Þó að Store Commerce og CPOS séu að mestu þau sömu, þá er nokkur mikilvægur munur sem þú verður að skilja.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce er skrifborðsforrit sem er sett upp og þjónustað á tæki.

- **Windows** - Store Commerce fyrir Windows forritið inniheldur allan forritskóðann,Commerce Runtime (CRT), og vélbúnaðarstöð (HWS).
- **iOS/Android** – Á þessum vettvangi virkar forritið sem gestgjafi fyrir CPOS forritakóðann. Með öðrum orðum, forritskóðinn kemur frá CPOS þjóninum sem er hýst á Commerce Scale Unit. Frekari upplýsingar, sjá [Yfirlit Commerce Scale Unit](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Vegna þess að CPOS keyrir í vafra er forritið ekki uppsett á tækinu. Í staðinn fær vafrinn aðgang að forritskóðanum frá CPOS þjóninum. Þess vegna hefur CPOS ekki beinan aðgang að POS vélbúnaði eða getur unnið án nettengingar.

### <a name="store-deployment-considerations"></a>Íhugunarefni tengd virkjun í verslun

Til viðbótar við vettvang og formþátt, verða smásalar einnig að velja virkjunarvalkost í versluninni. Eftirfarandi tafla sýnir grunnstillingarnar sem eru tiltækar fyrir hvern POS valkost.

| POS forrit            | Commerce Scale Unit | Tiltæk utan nets | Staðbundinn HWS stuðningur |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce fyrir Windows | Cloud eða RSSU       | Já               | Já               |
| Verslun Verslun fyrir Android | Cloud eða RSSU       | Nr.                | Já               |
| Store Commerce fyrir iOS     | Cloud eða RSSU       | Nr.                | Nr.                |
| Sölustaður í skýi                  | Cloud eða RSSU       | Nr.                | Nr.                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Skalaeining viðskiptanna er hluti sem hýsir CRT. CRT inniheldur allan viðskiptagrunn sem POS notar, og það veitir aðgang að rás gagnagrunninum. Á meðan þeir eru nettengdir, nota allir POS viðskiptavinir í versluninni Commerce Scale Unit. Commerce Scale Unit er hægt að virkja annaðhvort í skýinu eða í versluninni.

#### <a name="offline-mode"></a>Ótengdur hamur

Store Commerce fyrir Windows styður offline stillingu. Í ótengdum ham getur POS áfram unnið með sölu jafnvel þótt það sé aftengt frá Commerce Scale Unit. Síðan hægt að samstilla það með rásargagnagrunninum þegar tenging er endurheimt. Store Commerce notar sitt eigið innbyggða dæmi af CRT og notar tímabundið sinn eigin staðbundna gagnagjafa (offline SQL Server gagnagrunn). Sjá [POS virkni án nettengingar](pos-offline-functionality.md) til að fá nánari upplýsingar um virkni án nettengingar.

### <a name="pos-peripheralhardware-considerations"></a>POS jaðarbúnaður/vélbúnaður íhugunarefni

Söluaðilar verða einnig að íhuga hvernig POS mun fá aðgang að tækjum og jaðartæki, svo sem prentara, reiðuféskúffum og greiðslustöðvum. Vélbúnaðarstöðvar geta verið tileinkaðar POS afgreiðslukassa eða deilt meðal afgreiðslukassa í verslun.

| POS forrit            | Staðbundið HWS OPOS | Net jaðarbúnaðar | Sameiginlegur HWS stuðningur |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce fyrir Windows | Já            | Já                 | Já                |
| Verslun Verslun fyrir Android | Nr.             | Já                 | Já                |
| Store Commerce fyrir iOS     | Nr.             | Nr.                  | Já                |
| Sölustaður í skýi                  | Nr.             | Nr.                  | Já                |

Frekari upplýsingar um vélbúnaðarstöðvar, sjá [Grunnstilling og uppsetning Retail-vélbúnaðarstöðvar](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Umhugsunarefni fyrir innleiðingu

Íhugaðu eftirfarandi upplýsingar þegar þú skipuleggur POS innleiðingu þína í verslunum þínum:

- **Virknikröfur** - Grunnviðskiptaferli og færni eru þau sömu, óháð vettvangi, formþáttur eða grannfræði virkjunar. Þess vegna þurfa flestir smásalar ekki að íhuga virknikröfur þegar þeir skipuleggja innleiðingu sína.
- **Tengigeta** – Tiltækt net (víðnet \[WAN\] og staðarnet \[LAN\]) er stór þáttur sem krefst vandlegrar íhugunar. Allir ávinningur sem núll-fótspor, ský-hýsing lausn færir notanda í tengslum við kostnað og einfaldleika glatast ef kerfið er ekki í boði fyrir mikilvæg viðskiptaferli.

    Nema tengigeta fyrir tiltekið tæki sé mjög áreiðanleg og sterk, eða nema ákveðið langur óvirkur tími sé viðunandi fyrir smásalann, mælum við með einum af eftirtöldum valkostum:

    - Notaðu Store Commerce í Windows og virkjaðu offline stillingu.
    - Dreifa viðskiptamælikvarðaeiningunni á staðnum.

    Þessir tveir valkostir útiloka ekki hvorn annan. Fyrir sem áreiðanlegasta grannfræði, geta smásalar virkjað staðbundið RSSU til að þurfa ekki að vera eins háðir nettengingu eða Azure framboði, og þeir geta einnig virkjað POS afgreiðslukassa þar sem ótengdur hamur er settur í gang ef vandamál koma upp varðandi staðbundinn þjón eða net.

- **Vélbúnaður tæki/jaðartæki** - Einn mikilvægur þáttur í Retail POS kerfi er hæfni þess til að nota POS jaðartæki eins og prentara, reiðufjárskúffur og greiðslustöðvar. Þó að allir tiltækir POS valkostir geti notað jaðartæki, þá styður aðeins Store Commerce fyrir Windows þá beint. Fyrir öll önnur forrit þarf eina eða fleiri vélbúnaðarstöðvar. Þrátt fyrir að þessi nálgun bætir sveigjanleika, verða fleiri einingar að vera uppsett, grunnstilltir og þjónustaðir.
- **Kerfisskilyrði** - Kerfisskilyrðin fyrir POS forritið eru mismunandi. Vertu viss um að athuga nýjustu upplýsingar áður en þú velur. Til dæmis, vegna þess að CPOS keyrir í vafra styður það fjölbreyttar stýrikerfi. Fyrir frekari upplýsingar um kerfisskilyrði, sjá [Kerfisskilyrði fyrir uppsetningu í skýi](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Uppsetning og þjónusta** - Flækjustig uppsetningar- og þjónustuskilyrði geta verið breytilegt eftir því hvaða forrit og uppsetning eru valin. Til dæmis, fyrir ský-hýst CPOS uppsetningu, þú þarft ekki að setja upp og uppfæra í hverju tæki. Þess vegna minnkar þessi aðferð flækjustig og kostnað mikið. Hins vegar, ef þú setur upp Store Commerce á hverja skrá og virkjar ótengda stillingu, og þú setur einnig upp sameiginlegar vélbúnaðarstöðvar, fjölgar þú til muna fjölda endapunkta sem þarf að stjórna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
