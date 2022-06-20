---
title: Samþykktarverkflæði birgðabókar
description: Þessi grein lýsir því hvernig á að setja upp og nota verkflæði fyrir samþykki birgðabókar fyrir ýmsar gerðir af efnislegum birgðafærslum. Verkflæði birgðabókar tryggja að aðeins er hægt að bóka samþykktar birgðabækur í færslum.
author: yufeihuang
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ebb12562a9f06f2efc3b5a373d7ad0f98bc3505e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873986"
---
# <a name="inventory-journal-approval-workflows"></a>Samþykktarverkflæði birgðabókar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp og nota samþykkisvinnuflæði birgðabókar fyrir ýmsar gerðir birgðafærslur, svo sem útgáfur og kvittanir, birgðahreyfingar, efnisseðla (uppskriftir) og afstemmingu efnislegra birgða. Verkflæði birgðabókar tryggja að aðeins er hægt að bóka samþykktar birgðabækur í færslum.

> [!NOTE]
> Samþykktarverkflæði birgðabókar á aðeins við um færslur sem skráðar eru með birgðastjórnunareiningunni. Þau vinna ekki með birgðabækur sem ræsast í einingu vöruhúsakerfis.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Kveikið á eiginleika samþykktarverkflæði birgðabókar

Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta notað [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) síðu til að athuga stöðu eiginleika og virkja eða slökkva á honum ef þörf krefur. Hérna er eiginleikinn skráður sem:

- **Eining:** *Birgða- og vöruhúsakerfi*
- **Heiti eiginleika:** *Samþykktarverkflæði birgðabókar*

## <a name="create-your-inventory-journal-approval-workflows"></a>Búið til samþykktarverkflæði birgðabókar

Til að setja upp þennan eiginleika þarf að stofna verkflæði fyrir allar gerðir birgðabókar sem á að stýra. Vegna þess að mismunandi gerðir birgðabókar geta haft mismunandi samþykktarstigveldi og verkflæðisskref, er hægt að skilgreina stök verkflæði fyrir hverja birgðabókargerð.

Verkflæði styðja útgáfustýringu og hvert þeirra er með auðkenni verkflæðis og virka útgáfu. Hægt er að velja að virkja hverja nýja útgáfu verkflæðis strax við stofnun eða hafa hana óvirka. Ef þörf er á mismunandi verkflæðum fyrir sömu færslubókargerðina, skal stofna mörg verkflæði fyrir þá færslubókargerð, og úthluta síðan hverju þeirra til annars færslubókarheitis sem notar þessa gerð.

Til að stofna samþykktarverkflæði birgðabókar:

1. Opnið **Birgðastjórnun \> Uppsetning\> Verkflæði birgðastjórnunar**.
1. Veljið **Nýtt** á aðgerðasvæðinu.
1. Veljið gerð birgðabókar þar sem setja á upp verkflæði:
    - **Birgðatalningarbók**
    - **Færslubók eignarhaldsbreytingar birgða**
    - **Birgðahreyfingabók**
    - **Birgðaflutningabók**
    - **Talningarbók birgða**
    - **Uppskriftabók birgða**
    - **Birgðaleiðréttingabók**

    ![Svarglugga fyrir stofnun verkflæðis.](media/journal-workflow-create-workflow.png "Svarglugginn „Stofna verkflæði“")

1. Forrit verkflæðisritils ræsist í tækinu þínu. (Þú gætir verið beðinn um að samþykkja þessa aðgerð.) Notaðu hana til að hanna verkflæðið þitt eftir þörfum. Frekari upplýsingar um hvernig á að nota verkflæðisritilinn er að finna í [Yfirlit verkflæðiskerfis](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Þegar búið er að vista og loka forriti verkflæðisritilsins verður að velja hvort virkja eigi þessa verkflæðisútgáfu eða halda henni óvirkri.

> [!NOTE]
> Verkflæði bjóða upp á útgáfustýringu, sem þýðir að hægt er að skoða lista yfir útgáfur sem búið er að stofna og velja hver þeirra á að vera virk. Til að skoða lista yfir fáanlegar útgáfur og velja hverja þeirra á að virkja skal velja verkflæði sem er skráð á síðunni **Verkflæði birgðastjórnunar**. Á aðgerðasvæðinu skal opna flipann **Verkflæði** og velja **Útgáfur**. Aðeins ein útgáfa getur verið virk í einu fyrir hvert auðkenni verkflæðis.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Úthluta samþykktarverkflæðum á heiti birgðabóka

Næsta skref er að úthluta verkflæði birgðabókar á hvert birgðabókarheiti. Fyrir hverja birgðabókargerð er hægt að setja upp mörg birgðabókarheiti.

Að tengja verkflæði birgðabókar við birgðabókarheiti:

1. Farið í **Birgðastjórnun \> Uppsetning \> Færslubókarheiti \> Birgðir**.
1. Veljið heiti færslubókar úr listadálknum til að opna stillingasíðuna.
1. Í flýtiflipanum **Almennt** skal stilla **Samþykktarverkflæði** á **Já**. Ef beðið er um að samþykkja aðgerðina skal velja **Já**.

    ![Úthluta verkflæði á heiti færslubókar.](media/journal-workflow-journal-name.png "Úthluta verkflæði á færslubókarheiti")

1. Opnið fellilistann **Verkflæði** og veljið viðeigandi verkflæði. Listinn sýnir hvert virkt verkflæði sem stofnað hefur verið með því að nota forrit verkflæðisritilsins.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Stofna birgðabók og senda hana í samþykki

Þegar búið er að tengja birgðabókarheiti við samsvarandi samþykktarverkflæði birgðabókar, er hægt að stofna nýjar birgðabækur sem nota þetta heiti og senda svo þessar færslubækur í samþykki með því að nota þetta verkflæði. Ekki verður hægt að bóka birgðabókina fyrr en hún hefur verið samþykkt af samþykktaraðilum sem hafa verið skilgreindir í verkflæðinu.

1. Á yfirlitssvæðinu skal útvíkka **Birgðastjórnun \> Færslubókarfærslur \> Vörur** og síðan velja birgðabókargerð.
1. Veljið **Ný** til að stofna nýja færslubók af valinni gerð.
1. Svarglugginn **Stofna birgðabók** opnast. Fyllið út skjámyndina eftir þörfum og veljið svo **Í lagi** til að vista færslubókina.
1. Ljúka skal færslubókinni eftir þörfum.
1. Þegar búið er að stofna eða opna birgðabók með samþykktarverkflæði sem tengist henni, verður hnappurinn **Verkflæði** virkur á aðgerðasvæðinu. Þegar notandi er reiðubúinn að senda færslubókina í samþykki skal velja hnappinn **Verkflæði** til að opna fellilistaglugga og velja síðan **Senda inn**. Samþykktarbeiðnin fer þá á viðeigandi samþykktaraðila, sem fær tilkynningu með tilkynningaraðferðinni sem skilgreind er fyrir verkflæðið.

    ![Senda færslubók til samþykktar.](media/journal-workflow-inventory-journal.png "Að senda færslubók til samþykktar")

Til að afturkalla samþykktarbeiðni, skal opna viðeigandi færslubók og velja hnappinn **Verkflæði** og síðan velja **Afturkalla**. Þetta endurstillir verkflæðið.

Þegar færslubókin hefur verið samþykkt verður hægt að bóka hana. Til að bóka færslubókina skal velja **Bóka** á aðgerðasvæðinu. Ef hnappurinn **Bóka** er ekki virkur hefur færslubókin ekki verið samþykkt enn sem komið er.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Svara beiðni um samþykki birgðabókar

Ef notandi er samþykktaraðili ætti hann að fá skilaboð í hvert skipti sem þörf er á samþykki (eins og það er skilgreint í viðkomandi verkflæði). Þá er hægt að samþykkja eða hafna beiðni um samþykki færslubókar með því að gera eftirfarandi:

1. Á yfirlitssvæðinu skal útvíkka **Birgðastjórnun \> Færslubókarfærslur \> Vörur** og síðan velja birgðabókargerð.
1. Opnið viðeigandi færslu færslubókar og farið yfir hana.
1. Veljið hnappinn **Verkflæði** á aðgerðasvæðinu til að opna fellilistaglugga. Velja eitt af eftirfarandi:
    - **Samþykkja** - Til að samþykkja beiðnina.
    - **Hafna** - Til að hafna beiðninni.
    - **Meira \> Óska eftir breytingu** - Til að senda skilaboð til umsækjanda og biðja hann um að breyta einhverju ákveðnu og síðan senda aftur til baka.
    - **Meira \> Úthluta** - Til að úthluta samþykkinu á annan notanda.
    - **Meira \> Afturkalla** - Til að afturkalla samþykktarbeiðnina (endurstillir verkflæðið).
    - **Meira \> Verkflæðissaga** - Til að skoða sögu samþykktarverkflæðisins fram að þessu.

## <a name="review-the-approval-history"></a>Yfirfara samþykktarsöguna

Eins og með aðrar gerðir verkflæðis, er hægt að nota síðuna **Verkflæðissaga** til að skoða sögu samþykktarverkflæðisins fyrir hvaða færslubók sem er.

Að yfirfara verkflæðissögu færslubókar:

1. Á yfirlitssvæðinu skal útvíkka **Birgðastjórnun \> Færslubókarfærslur \> Vörur** og síðan velja birgðabókargerð.
1. Opnið viðeigandi færslubók.
1. Veljið hnappinn **Verkflæði** á aðgerðasvæðinu til að opna fellilistaglugga. Veldu **Verkflæðissaga**. Frekari upplýsingar er að finna á [Skoða verkflæðissögu](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]