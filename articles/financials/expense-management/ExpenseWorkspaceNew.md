---
title: Kostnaðarskýrslur endurhugsaðar
description: Þetta efnisatriði veitir upplýsingar um endurhannaða og endurhugsaða upplifun fyrir færslu kostnaðarskýrslu í Microsoft Dynamics 365 for Finance and Operations. Nýja upplifunin einfaldar ferlið við að ljúka kostnaðarskýrslum og dregur úr tímanum sem það tekur.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 320984fc6be231c941df17abb7246e92f6aa4b9a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841058"
---
# <a name="expense-reports-reimagined"></a>Kostnaðarskýrslur endurhugsaðar

[!include[banner](../includes/banner.md)]

Færsla kostnaðarskýrslu hefur verið endurhönnuð til að einfalda ferlið við að ljúka kostnaðarskýrslum og dregur úr tímanum sem það tekur. Hér eru helstu þættir nýju kostnaðarupplifunar:

- Nýtt vinnusvæði útgjaldastýringar sem gerir þér kleift að fá aðgang að útgjöldum fulltrúa.
- Ný upplifun fyrir samsvörun kvittunar til að sýna betur kvittanir á hausstigi og til að einfalda ferlið við að hengja kvittanir við kostnaðarlínur.
- Nýtt skrifvarið hnitanet sem gerir þér kleift að skoða mun fleiri kostnaðarlínur og viðbótardálka gagna. Nú er hægt að sjá allar sundurliðaðar og skiptar línur, ásamt kostnaði yfireiningar.
- Einfaldað svæði fyrir breytingar á kostnaði.
- Endurhönnuð skilaboð fyrir villur, aðvaranir og reglur til að tryggja að rétt samhengi sé til staðar til að skilja hvert vandamálið er og hvernig skuli leysa það. Microsoft hefur fjarlægt mörg skilaboð sem birtust áður en notendur höfðu tækifæri til að ljúka verkum sínum og takast á við vandann, t.d. ólokin sundurliðin á skilaboði.
- Ný síða til að tilgreina hvaða reiti fyrirtækið þarf, hvaða reitir eru valkvæðir og hvaða reiti á ekki að sækja. Þessi síða auðveldar að draga úr fjölda reita sem notendur þurfa að stilla.
- Nýtt útlit og yfirbragð á kostnaðarskýrslum þannig að skýrslurnar líta ekki lengur út eins og þær séu hannaðar með bókhaldara í huga.

Til að kveikja á nýju upplifuninni skal nota vinnusvæðið **Stjórnun eiginleika** til að kveikja á eiginleikanum **Kostnaðarskýrslur endurhugsaðar**. Þegar kveikt er á þessum eiginleika gerast eftirfarandi aðgerðir:

- Núverandi vinnusvæði kostnaðar er skipt út fyrir nýja vinnusvæðið.
- Nýtt valmyndaratriði fyrir sýnileika kostnaðarreits er bætt við.
- Engin fyrirliggjandi valmyndaratriði fyrir kostnaðarskýrslur (núverandi síða) eða reitir kostnaðarskýrslu eru fjarlægðir.
- Verkflæði og allar samþykktir leiða þig ennþá að núverandi síðu fyrir kostnaðarskýrslur.

## <a name="getting-started-video-for-new-users"></a>Kynningarmyndband fyrir nýja notendur

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Myndbandið [Kostnaðarumhverfi í Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (sýnt hér að ofan) er innifalið í [Spilunarlista Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er tiltækt í YouTube.

## <a name="new-features"></a>Nýjar aðgerðir

| Nýr eiginleiki | Lýsing |
|---|----|
| Sýnileiki kostnaðarreita | Ný uppsetningarsíða leyfir þér að tilgreina hvaða reiti skuli gera óvirka fyrir fyrirtæki, hvaða reitir eiga að vera áskildir og hvaða reitum mælt er með. |
| Áskildir reitir | Ný einföld skilgreining leyfir þér að gera suma reiti áskilda án þess að þurfa að nota reglurammann. |
| Valfrjáls svæði | Bætt er við annarri síðu fyrir valfrjálsa reiti. Með þessum hætti finnst starfsfólki ekki eins og það þurfi að stilla reitina, en reitirnir eru samt mjög aðgengilegir. |
| Bæta við ótengdum kvittunum | Hæfnin til að bæta ótengdum kvittunum við kostnaðarskýrslu er sýnilegri úr vinnusvæðinu og á kostnaðarskýrslunni. |
| Endurbætt skilaboð | Betri sýnileiki er á kostnaðarlínum sem eru með aðvörunum eða villum. |
| Fækkun skilaboða í skilaboðastikunni| Fjölda Infolog-skilaboða var fækkað og reynt var að koma í veg fyrir að tvítekin skilaboð birtust í mörgum tilfellum. |
| Algengar aðgerðir flokkaðar saman | Viðmótið var gert snyrtilegra með því að bæta við nýjum aðgerðarhnappi fyrir flestar af algengustu aðgerðum á línustigi og með því að bæta við þrípunktahnappi (...) fyrir haus og aðrar sjaldgæfari aðgerðir. |
| Nýtt vinnusvæði til að auka sýnileika | Nýtt vinnusvæði sameinar eiginleika og tengla sem gera notendum kleift að flakka á milli svæða. |
| Bæta við fyrirliggjandi kostnaði og kvittunum við stofnun kostnaðar | Þegar kostnaðarskýrslur eru stofnaðar er hægt að bæta við öllum eða völdum kostnaði og kvittunum. |
| Útreikningur gengis | Útreikning gengis er bætt við til að gera þér kleift að reikna út gengið fyrir færslur í mörgum gjaldmiðlum fyrir útlagðan kostnað. |
| Vista og bæta við nýjum kostnaðarlínum | Hnapparnir **Vista** og **Nýr** eru tiltækir þegar nýr kostnaður er sleginn inn til að auðvelda þér að færa kostnaðarlínur inn á fljótlegan hátt. |
| Aukinn sýnileiki inn í skiptar og sundurliðaðar línur | Sundurliðuðum og skiptum línum er bætt beint inn á lista yfir kostnað, til að auka sýnileika og auðvelda þér að ákvarða hvort reglur í villum eða aðrar villur séu til staðar. |
| Sýna kvittanir við sundurliðun | Hægt er að sýna kvittanir við sundurliðun. |

Upphafleg útgáfa leggur áherslu á atburðarásir fyrir kostnaðarfærslur. Allar atburðarásir sem tengjast yfirferð eða samþykkt á kostnaðarskýrslu halda áfram að nota núverandi síðu fyrir kostnaðarfærslu.

Eftirfarandi eiginleikar eru til staðar á núverandi síðu en eru ekki enn til staðar á nýju síðunni. Þessir eiginleikar verða kynntir aftur til sögunnar í næstu útgáfum:

- Samþykktir
- Samþykktir á viðskiptaskuldum og getan til að breyta bókhaldinu
- Margir aðgangsstaðir
- Samþætting ferðabeiðni
- Gagnaeining fyrir sýnileika kostnaðarreits
- Færsla fyrir kostnað dagpeninga
- Verkflæði á línustigi
- Stuðningur fyrir bráðabirgðasamþykktaraðila
- Ítarleg sundurliðun
