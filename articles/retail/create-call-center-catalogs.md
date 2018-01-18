---
title: "Stofna vörulista fyrir símaver"
description: "Þessi grein gefur yfirlit yfir ferli þess að búa til vörulista fyrir símaver."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29d005655856fd1eb0f1490c45e07649465539f2
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-call-center-catalog"></a>Stofna vörulista fyrir símaver

[!include[banner](includes/banner.md)]


Þessi grein gefur yfirlit yfir ferli þess að búa til vörulista fyrir símaver. 

Í  símaver, er hægt að nota vörulista til að auðkenna afurðirnar sem óskað er eftir að bjóða uppá í verslunum. Símaver nota yfirleitt prentaða vörulista. Hönnun og framleiðsla á prentuðum vörulista fer fram utan Microsoft Dynamics 365 for Retail. Hins vegar er hægt að stofna og geyma stafræna skjámynd vörulista með því að nota sömu form og eru notuð til að setja upp smásöluvörulista á netinu. Áður en hægt er að stofna vörulista verður að setja upp afurðaúrvali og úthluta þjónustumiðstöð í úrvali. Að bæta afurðir vörulista með því að velja vörur úr þessum úrvali. Eftir að afurðir hefur verið bætt við vörulista og vörulistinn er lokið, verður að villuleita vörulista til að staðfesta gögn. Vörulisti er því næst sendar til yfirferðar og samþykktar. Eftir að vörulisti er samþykktur er hægt að birta hann. Þegar vörulisti fyrir símaver er stofnaður er hægt að taka skyndimynd af vörulistagögnunum þegar°vörulistinn er gefinn út. Þessi virkni skyndimynd gerir kleift að fá aðgang að tiltekinni útgáfu vörulista, jafnvel þótt vörulistinn er síðar breytt og uppfært. Einnig er hægt að setja vörulista símavers upp til að taka með eftirfarandi valfrjálsar aðgerðir:

-   **Frumkóðar** - kóðar sem eru notaðir til að fylgjast með viðbrögðum viðskiptavina við tilteknum pósti verslun.
-   **Ókeypis vörur** – Vörur sem bætt er við pöntun viðskiptavinar án viðbótargjalda. Þessum vörum er sjálfkrafa bætt við pöntunina þegar frumkóði fyrir vörulistann er færður inn í pöntun.
-   **Forskriftir** – Texti sem starfsmaður í símaveri les fyrir viðskiptavini þegar sölupöntun er stofnuð. Forskriftir geta innihaldið kveðjur eða innkaupapöntun tillögur.
-   **Viðbótarsölu- eða krosssöluvörur** -Vörur sem eru birt sem tillaga þegar tiltekinni vöru er bætt við pöntunina.

Þessa valkosti verður að setja upp°áður en vörulistinn er samþykktur og°birtur.

## <a name="prerequisites"></a>Skilyrði
Ljúka þarf eftirfarandi verkum áður en hafist er handa:

-   Setja upp afurðir og úrval afurða.
-   Setja upp smásöluafurðir.
-   Setja upp vöruúrval.
-   Stofna símaver.
-   Setja upp símaver.
-   Bæta símaveri við stigveldi fyrirtækis.
-   Stofna eða breyta stigveldi fyrirtækis.

## <a name="create-a-catalog"></a>Stofna vörulista
Fyrst þarf að búa til vörulista, bæta við afurðum í vörulistann og fara yfir og uppfæra eigindir fyrir afurðirnar.

## <a name="validate-the-catalog"></a>Staðfesta vörulistann
Eftir að þú hefur lokið við að setja upp vörulista verður þú að staðfesta hann. Staðfestingarferlið°staðfestir að gögn sem þarf fyrir eigindi rásar og afurðareigindir eru heil og gild og að hægt sé að birta vörulistann.

## <a name="submit-the-catalog-for-review-and-approval"></a>Senda innkaupavörulistann til yfirferðar og samþykktar
Eftir að vörulista hefur verið samþykktur er hægt að senda vörulista til yfirferðar og samþykkis. Vörulista verður að samþykkja áður en hann er birtur. Hægt er að skilgreina verkflæði þannig að vörulistar séu annaðhvort sjálfkrafa samþykktir eða krefjist handvirkrar samþykktar.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Valfrjálst: Bæta við upprunakóðum, ókeypis afurðum og forskriftum
Einnig er hægt að bæta eftirfarandi atriðum vörulista símavers. Þessar vörur eru valfrjálsar.

-   Fyrirtæki sem útvega prentaða vörulista°geta notað°**Frumkóða** til að rekja svörun viðskiptavina fyrir tiltekna vörulista. Frumkóðar eru oft prentaðir á bakhlið vörulista og eru færðir inn í sölupöntun þegar viðskiptavinur gerir kaup. Til að bæta við upprunakóða í vörulista verður þú fyrst að stofna markhóp. Markhópur er yfirleitt varpað á póstlista í eigu eða leigu.
-   **Ókeypis vörur** eru kynningartilboðsvörur sem eru ókeypis við pöntun viðskiptavinar þegar vísað er í vörulistann.
-   **Forskriftir** er hægt að nota°til að leiðbeina°starfsmanni í samskiptum við viðskiptavini um efni vörulista eða um vöru í vörulista.

## <a name="publish-the-catalog"></a>Birta vörulistann
Með birtingu vörulista fyrir þjónustumiðstöð, ljúka upplýsingar afurða í vörulistanum. Útgáfa gefur einnig til kynna að vörulistinn er tilbúin til frekari aðgerða sem á að framkvæma. Til dæmis er hægt að stofna prentaða vörulista. Hægt er að birta vörulista handvirkt eða nota runuvinnslu til að birta samkvæmt áætlun. Áður en hægt er að birta vörulista, verður að vera að staðfesta og samþykkja vörulistann. Til að breyta vörulistanum eftir að hann er birtur er hægt að afturkalla vörulista og endurbirta hann síðan.




