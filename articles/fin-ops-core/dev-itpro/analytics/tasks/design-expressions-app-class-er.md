---
title: Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka
description: Þessi grein lýsir hvernig á að endurnýta núverandi forritaskrár í grunnstillingu rafrænnar skýrslugerðar (ER) með því að kalla á nauðsynlegar aðferðir við forritaflokka.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267843"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir hvernig á að endurnýta núverandi forritsrök í skilgreiningum [rafrænnar skýrslugerðar (ER)](../general-electronic-reporting.md) með því að kalla á nauðsynlegar aðferðir við forritaflokka í ER-segðum. Gildi frumbreyta fyrir kallflokka er hægt að skilgreina dýnamískt á keyrslutíma. Til dæmis er hægt að byggja gildi upplýsingum í þáttunarskjalinu til að tryggja réttmæti þess.

Til dæmis, í þessari grein, munt þú hanna ferli sem þáttar bankayfirlit á innleið fyrir uppfærslu forritsgagna. Þú færð bankayfirlit á innleið sem textaskrár (.txt) sem innihalda IBAN-kóða (International Bank Account Number). Sem hluti af innflutningsaðferð bankayfirlits þarft þú að sannreyna réttmæti þessa IBAN-kóða með því að nota rök sem er nú þegar í boði.

## <a name="prerequisites"></a>Forkröfur

Ferlið í þessari grein er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkinu **Kerfisstjóra** eða **Þróunaraðila rafrænnar skýrslugerðar**.

Hægt að klára ferlin með því að nota hvaða gagnasafn sem er.

Til að ljúka verður þú að hlaða niður og vista eftirfarandi skrá: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Í þessari grein muntu stofna nauðsynlegar ER-skilgreiningar fyrir sýnifyrirtækið, Litware, Inc. Af þessum sökum þarf að fylgja þessum skrefum áður en ferlunum í þessari grein er lokið.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningasíða staðfæringar**, skaltu staðfesta að skilgreiningaveitan fyrir sýnifyrirtækið **Litware, Inc.** sé skráð og að það sé merkt sem Virkt. Ef þú sérð skilgreiningarveituna ekki skaltu fylgja skrefunum í [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Flytja inn nýja grunnstillingu líkans í Rafræn skýrslugerð

1. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn fyrir skilgreiningarveituna **Microsoft**.
2. Veldu **Geymslur**.
3. Á síðunni **Staðfæringargeymslur** skaltu velja **Sýna síur**.
4. Til að velja skrá yfir færslu altækrar geymslu skal bæta við síureitnum **Heiti**.
5. Í reitinn **Heiti** skal færa inn **Altækt**. Veldu síðan síuvirknitáknið **inniheldur** .
6. Veljið **Bæta við**.
7. Smellið á **[Opna](../er-download-configurations-global-repo.md#open-configurations-repository)** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar fyrir valda gagnageymslu.
8. Á síðunni **Gagnageymsla skilgreiningar**, í skilgreiningartrénu, skal velja **Greiðslulíkan**.
9. Á flýtiflipanum **Útgáfur**, ef hnappurinn **Innflutningur** er tiltækur, skal velja hann og velja svo **Já**.

    Ef hnappurinn **Innflutningur** er ekki tiltækur hefur þú þegar flutt inn valda útgáfu af skilgreiningu rafrænnar skýrslugerðar **Greiðslulíkan**.

10. Lokaðu síðunni **Gagnageymslusíða skilgreiningar** og lokaðu síðan **Staðfæringargeymslur**.

## <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð

Bæta við nýju sniði fyrir rafræna skýrslugerð til að þátta bankayfirlit á innleið á TXT-sniði.

1. Á síðunni **Skilgreiningar staðfæringar** skal velja reitinn **Skilgreiningar skýrslugerðar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan**.
3. Veljið **Stofna skilgreiningu**. 
4. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í svæðinu **Nýtt** skal færa inn **Snið byggir á gagnalíkani PaymentModel**,
    2. Í reitnum **Heiti** skal færa inn **Innflutningssnið bankayfirlits (dæmi)**.
    3. Í reitnum **Styður gagnainnflutning** velurðu **Já**.
    4. Veljið **Stofna skilgreiningu** til að stofna skilgreininguna.

## <a name="design-the-er-format-configuration--format"></a>Veljið grunnstillingu rafrænnar skýrslugerðar - Snið

Hanna snið rafrænnar skýrslugerðar fyrir væntanlegt skipulag ytri skráar á TXT-sniði.

1. Fyrir sniðskilgreiningu **Innflutningssnið bankayfirlits (dæmi)** sem þú bættir við velur þú **Hönnuður**.
2. Á síðunni **Sniðshönnuður**, í sniðstrénu vinstra megin, skal velja **Bæta við rót**.
3. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu skal velja **Texti\\Röð** til að bæta við sniðsíhlutnum **Röð**.
    2. Í reitinn **Heiti** skal færa inn **Rót**.
    3. Í reitnum **Sérstafir** skal velja **Ný lína - Windows (CR LF)**. Byggt á þessari stillingu telst sérhver lína í þáttunarskrá aðskilin færsla.
    4. Veldu **Í lagi**.

4. Veljið **Bæta við**.
5. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu skal velja **Texti\\Röð**.
    2. Í reitinn **Heiti** skal færa inn **Línur**.
    3. Í reitnum **Margfeldi** skaltu velja **Einn margir**. Byggt á þessari stillingu verður að minnsta kosti ein lína til staðar í þáttunarskránni.
    4. Veldu **Í lagi**.

6. Í trénu skal velja **Rót\\Línur** og svo velja **Bæta við röð**.
7. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **Reitir**.
    2. Í **Margfeldi** reitnum skal velja **Nákvæmlega eitt**.
    3. Veldu **Í lagi**.

8. Í trénu skal velja **Rót\\Línur\\Reitir** og svo velja **Bæta við**.
9. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í trénu skal velja **Texti\\Strengur**.
    2. Í reitinn **Heiti** skal færa inn **IBAN**.
    3.. Veldu **Í lagi**.

10. Veldu **Vista**.

Skilgreiningin er nú uppsett þannig að hver lína í þáttunarskránni inniheldur aðeins IBAN-kóðann.

![Sniðskilgreining Innflutningssnið bankayfirlits (dæmi) á síðu Sniðhönnuðar.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Veljið skilgreiningu rafrænnar skýrslugerðar – vörpun í gagnalíkan

Hanna vörpun ER-sniðs sem notar upplýsingar úr þáttunarskránni til að fylla út gagnalíkan.

1. Á síðunni **Sniðshönnuður**, í aðgerðarúðunni, skal velja **Varpa sniði á líkan**.
2. Á síðunni **Líkanavörpun á gagnagjafa**, á aðgerðasvæðinu, skal velja **Nýtt**.
3. Í reitnum **Skilgreining** er valið **BankToCustomerDebitCreditNotificationInitiation**.
4. Í reitnum **Heiti** skal færa inn **Vörpun í gagnalíkan**.
5. Veldu **Vista**.
6. Veljið **Hönnuður**.
7. Á síðunni **Hönnuður líkanavörpunar**, í trénu **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Klasi**.
8. Í hlutanum **Gagnagjafar** skal velja **Bæta við rót** til að bæta við gagnagjafa sem kallar á fyrirliggjandi forritsrök fyrir staðfestingu IBAN-númera.
9. Í svarglugganum sem kemur upp skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **Skoða\_Kóðar**.
    2. Í reitnum **Flokkur** slærðu inn eða velur **ISO7064**.
    3. Veldu **Í lagi**.

10. Í trénu **Gerðir gagnagjafa** skal fylgja þessum skrefum:

    1. Stækka gagnagjafa **sniðsins**.
    2. Víkkið út **format\\Root: Sequence(Root)**.
    3. Víkka út **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    4. Víkka út **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)**.

11. Í **Gagnalíkan** skal fylgja þessum skrefum:

    1. Stækka reitinn **Greiðslur** í gagnalíkaninu.
    2. Stækka **Greiðslur\\Lánveitandalykill(CreditorAccount)**.
    3. Stækka **Greiðslur\\Lánveitandalykill(CreditorAccount)\\Auðkenning**.
    4. Stækka **Greiðslur\\Lánveitandalykill(CreditorAccount)\\Auðkenning\\IBAN**.

12. Fylgdu þessum skrefum til að binda þætti skilgreinds sniðs við reiti gangalíkans:

    1. Veldu **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    2. Veljið **Greiðslur**.
    3. Veldu **Binda**. Byggt á þessari stillingu telst sérhver lína í þáttunarskrá ein greiðsla.
    4. Veljið **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)\\IBAN: String(IBAN)**.
    5. Veldu **Greiðslur\\Lánveitandalykill(CreditorAccount)\\Auðkenning\\IBAN**.
    6. Veldu **Binda**. Byggt á þessari stillingu verður reiturinn **IBAN** fyrir gagnalíkanið fylltur út með gildinu úr þáttunarskránni.

    ![Tenging sniðsíhlutar við gagnalíkansreiti á síðunni Hönnuður líkanavörpunar.](../media/design-expressions-app-class-er-02.png)

13. Í flipanum **Staðfestingar** skal fylgja þessum skrefum til að bæta við reglu [staðfestingar](../general-electronic-reporting-formula-designer.md#Validation) sem sýnir villuboð fyrir einhverja línu í þáttunarskránni sem inniheldur ógilt IBAN-númer:

    1. Veldu **Nýtt** og veldu síðan **Breyta skilyrði**.
    2. Á síðunni **Formúluhönnuður**, í trénu **Gagnagjafi**, skal stækka gagnagjafann **Athuga\_kóða** sem stendur fyrir forritsklasa **ISO7064** til að skoða tiltækar aðgerðir þessa klasa.
    3. Veldu **Athuga\_kóða\\verifyMOD1271\_36**.
    4. Veldu **Bæta við gagnagjafa**.
    5. Í reitnum **Formúla** skal færa inn eftirfarandi [segð](../general-electronic-reporting-formula-designer.md#Binding): **Skoða\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. Veljið **Vista** og lokið síðan skjámyndinni.
    7. Velja **Breyta skilaboðum**.
    8. Á síðunni **Formúluhönnuður** í reitnum **Formúla** skal slá inn **CONCATENATE("Invalid IBAN code has been found:&nbsp;", format.Root.Rows.Fields.IBAN)**.
    9. Veljið **Vista** og lokið síðan skjámyndinni.

    Byggt á þessum stillingum mun skilyrði staðfestingar skila *[ÓSATT](../er-formula-supported-data-types-primitive.md#boolean)* fyrir öll ógild IBAN-númer með því að kalla á fyrirliggjandi **verifyMOD1271\_36** aðferð forritsklasans **ISO7064**. Athugaðu að gildi IBAN-kóðans er skilgreint gagnvirkt á keyrslutíma sem frumbreyta köllunaraðferðarinnar, byggt á innihaldi textaþáttunarskráarinnar.

    ![Villuleitarregla á hönnunarsíðu líkanavörpunar.](../media/design-expressions-app-class-er-03.png)

14. Veldu **Vista**.
15. Lokið síðunni **Hönnuður líkanavörpunar** og lokið svo síðunni **Líkanavörpun á gagnagjafa**.

## <a name="run-the-format-mapping"></a>Keyra vörpun sniðs

Til að prófa, skal keyra vörpun sniðs með skránni SampleIncomingMessage.txt sem þú sóttir. Myndað úttak inniheldur gögn sem verða flutt inn úr valinni TXT-skrá og fyllt út í sérstillt gagnalíkan í rauninnflutningi.

1. Á síðunni **Vörpun líkans í gagnagjafa** skal velja **Keyra**.
2. Á síðunni **Rafrænar skýrslufæribreytur** skal velja **Vafra**, fara í skrána **SampleIncomingMessage.txt** sem var sótt og velja hana.
3. Veldu **Í lagi**.
4. Athugaðu að síðan **Líkanavörpun á gagnagjafa** sýnir villuboð um ógilt IBAN-númer.

    ![Niðurstöður keyrslu sniðsvörpunar á síðunni Líkanavörpun á gagnagjafa.](../media/design-expressions-app-class-er-04.png)

5. Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan. Taktu eftir að aðeins var unnið úr þremur línum í innfluttu textaskránni án villna. IBAN-kóðinn á línu 4 er ekki gildur og var sleppt.

    ![XML-úttak.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
