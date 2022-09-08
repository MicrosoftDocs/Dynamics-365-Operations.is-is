---
title: Afsláttarmiðar
description: Þessi grein veitir yfirlit yfir möguleika sem tengjast afsláttarmiða í Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 2594848948b141015adfaa4ec27e2c2b4cc4dcd2
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410472"
---
# <a name="coupons"></a>Afsláttarmiðar

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein veitir yfirlit yfir möguleika sem tengjast afsláttarmiða í Microsoft Dynamics 365 Commerce.

Afsláttarmiðar eru kóðar og strikamerki sem eru notuð til að setja afslætti inn í færslur. Söluaðilar dreifa afsláttarmiðum til væntanlegra eða núverandi viðskiptavina til að hjálpa til við að bæta vörumerkjaþekkingu sína, auka viðskipti, halda viðskiptavinum sínum, auka sölu og að lokum auka tekjur. Afsláttarmiðar eru orðnir eitt af vinsælustu markaðstækjunum og eru ný viðmið í sölu á rafrænum viðskiptum.

Í Dynamics 365 Commerce, afsláttarmiðar eru tengdir afslætti og teljast til viðbótargildingar ofan á afslætti. Hver afsláttarmiði tengist einum afslætti og tengdi afslátturinn skilgreinir vörusafnið sem afsláttarmiðinn gildir fyrir.

Verðflokkar sem tengjast afslætti skilgreina hæf skilyrði sem hægt er að nota afsláttarmiða fyrir. Þau skilyrði innihalda viðskiptavinahópa og söluleiðir. Afsláttarmiðar veita einnig **Notkunarmörk** og **Viðskiptavinur krafist** eiginleika sem hægt er að nota til að stilla valfrjálsar notkunartakmarkanir.

Hver afsláttarmiði getur haft marga afsláttarmiða kóða og afsláttarmiða strikamerki, og hver kóða getur haft sitt eigið gildistímabil og stöðu. Ef staða kóða er stillt á **Óvirkt**, ekki er hægt að nota kóðann á neinni rás.

## <a name="set-up-a-coupon"></a>Settu upp afsláttarmiða

Áður en hægt er að setja upp afsláttarmiða verður að setja upp strikamerki og tvær númeraraðir afsláttarmiða.

Til að setja upp afsláttarmiða í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Fara til **Verslun og verslun \> Vörustjórnun \> Strikamerki og merkimiðar \> Grímupersónur**.
1. Veldu **Bæta við** að búa til grímu karakter af **Afsláttarkóði** tegund. Í **Karakter** reit geturðu valið hvaða ónotaða staf sem er.
1. Fara til **Verslun og verslun \> Vörustjórnun \> Strikamerki og merkimiðar \> Uppsetning strikamerkisgrímu**.
1. Veldu **Nýtt** til að búa til strikamerkisgrímu af **Afsláttarmiði** tegund.
1. Fara til **Verslun og verslun \> Vörustjórnun \> Strikamerki og merkimiðar \> Strikamerki uppsetning**.
1. Veldu **Nýtt** til að búa til strikamerki sem notar strikamerkisgrímuna sem þú bjóst til.
1. Fara til **Stjórn stofnunarinnar \> Númeraraðir**.
1. Búðu til tvær talnaraðir:

    1. Ein röð fyrir **Afsláttarmiðanúmer** tilvísun. Þessi röð skilgreinir einstakt auðkenni afsláttarmiða.
    1. Ein röð fyrir **Auðkenni afsláttarmiðakóða** tilvísun. Þessi röð skilgreinir einstakt auðkenni hvers afsláttarmiðakóða fyrir afsláttarmiða.

    Það verður að stilla reitinn **Gildissvið** á **Fyrirtæki** fyrir báðar númeraraðir. Í flestum tilfellum ættu báðar raðnúmerin að myndast sjálfkrafa.

1. Fara til **Viðskiptabreytur \> Verð og afslættir \> Afsláttarmiðar**.
1. Stilltu **Afsláttarnúmer strikamerki maska** reitnum við strikamerkið sem þú bjóst til áðan.
1. Fara til **Viðskiptabreytur \> Númeraraðir**.
1. Veldu númeraröðina sem þú bjóst til áðan fyrir **Afsláttarmiðanúmer** og **Auðkenni afsláttarmiðakóða** tilvísanir.

Til að setja upp afsláttarmiða verður þú að búa til afsláttinn og afsláttarmiðann sérstaklega og tengja þá síðan með því að velja afsláttinn í **Afsláttur** reit stillingar afsláttarmiða. Eftir að afsláttarmiði er tengdur við afslátt, þá **Staða**, **·**, og **Gildistími** reitir tengda afsláttarins verða skrifvarnir, vegna þess að gildin ráðast af stöðu afsláttarmiðans og gildistíma. Þegar staða afsláttarmiða er stillt á **Virkur**, staða tengda afsláttarins er sjálfkrafa uppfærð í **Virkt**. Sömuleiðis þegar staða afsláttarmiða er stillt á **Óvirkt**, staða tengdrar afsláttarstöðu er sjálfkrafa uppfærð í **Öryrkjar**.

## <a name="use-a-coupon"></a>Notaðu afsláttarmiða

Til að bæta afsláttarmiða við sölufærslu í Commerce sölustað (POS) er hægt að nota afsláttarmiða kóða eða afsláttarmiða strikamerki. Til að nota afsláttarmiða kóða skaltu velja **Bæta við afsláttarmiða kóða** aðgerð og sláðu síðan inn kóðann. Til að nota strikamerki afsláttarmiða geturðu annað hvort skannað strikamerkið með því að nota skannatæki eða slegið það inn með því að nota talnalyklaborðið á **Viðskipti** skjár.

Söluaðilar vilja stundum að gjaldkerar geti veitt viðskiptavinum fasta afslætti vegna friðunarástæðna eða vegna vörugalla, en þeir vilja ekki prenta afsláttarmiða og dreifa þeim til gjaldkera. Í þessu tilviki geturðu stillt **Sæktu um án afsláttarmiðakóða** valkostur fyrir afsláttarmiða til **Já**. POS gjaldkerar geta þá notað **Sækja afsláttarmiða** virka inni í **Skoða tiltæka afslætti** aðgerð til að bæta afsláttarmiða við færslu án þess að slá inn kóðann handvirkt. Ef margir afsláttarmiðakóðar eru til fyrir afsláttarmiða velur kerfið sjálfkrafa fyrsta virka kóðann og notar hann á færsluna.

Til að bæta afsláttarmiða við sölupöntun símaversins verður notandi símaver að velja **Afsláttarmiðar** á **Stjórna** flipanum í Aðgerðarrúðunni á sölupöntunarsíðunni.

Til að bæta afsláttarmiða við rafræn verslunarpöntun getur kaupandi slegið inn afsláttarmiðakóðann í **kynningarkóði** reit í innkaupakörfunni.

Eftir að afsláttarmiða er bætt við sölupöntun kveikir verðlagningarvélin strax endurútreikning fyrir alla pöntunina, óháð því hvort seinkaður útreikningur er virkur.

> [!NOTE]
> Í Commerce útgáfu 10.0.30 og eldri, eftir að notendur símavera hafa bætt afsláttarmiða við sölupöntun símaver, verða þeir að velja **Endurreikna** í **Reikna** hópur á **Selja** flipanum í aðgerðarrúðunni til að nota afsláttinn sem er tengdur þeim afsláttarmiða.

## <a name="coupon-usage-limit"></a>Notkunarmörk afsláttarmiða

Hægt er að stilla afsláttarmiða fyrir takmarkaða notkun. Notkunarmörkin er hægt að skilgreina á hvern viðskiptavin, á hverja rás eða á heimsvísu. Notkunarmörkum er framfylgt fyrir hvern afsláttarmiðakóða á afsláttarmiða. Til dæmis er hægt að nota einnota afsláttarmiða sem hefur tvo afsláttarmiða kóða tvisvar, einu sinni fyrir hvern afsláttarmiða kóða.

Hægt er að nota afsláttarmiða á milli sölurása. Hins vegar, fyrir símaver, er aðeins hægt að nota afsláttarmiða í takmarkaðri notkun þegar **Virkja pöntunarlok** stilling fyrir rás símaversins er virkjuð. Ef **Virkja pöntunarlok** stillingin er óvirk, aðeins er hægt að nota afsláttarmiða sem ekki eru í takmarkaðri notkun.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
