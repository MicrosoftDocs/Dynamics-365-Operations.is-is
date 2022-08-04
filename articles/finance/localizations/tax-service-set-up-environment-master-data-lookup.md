---
title: Virkja uppflettingu aðalgagna fyrir skattaútreikningsstillingar
description: Þessi grein útskýrir hvernig á að setja upp og virkja skattaútreikning aðalgagnaleitarvirkni.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3642bb88d5b0570014513b64eef5fdab6d1ee9d3
ms.sourcegitcommit: 5b721f6fc1ba4350b5bd0eae457f71d80246db42
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/20/2022
ms.locfileid: "9181125"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Virkja uppflettingu aðalgagna fyrir skattaútreikningsstillingar 

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp og virkja skattaútreikning aðalgagnaleitarvirkni. Fellilisti er tiltækur til að velja gildi í skattreikningsskilgreiningu fyrir reiti eins og **Lögaðili**, **söluaðila**, **·**, og **Afhendingartími**. Þessi gildi koma frá tengdum Microsoft Dynamics 365 Fjármálaumhverfi með því að nota Microsoft Dataverse gagnagjafa.

> [!NOTE] 
> Uppflettivirkni skattaútreiknings aðalgagna er valfrjáls virkni. Þú getur sleppt eftirfarandi skrefum ef þú slekkur á **Skattþjónusta Dataverse stuðningur við gagnaveitur** lögun í Regulatory Configuration Service (RCS). Hins vegar, í því tilviki, verður fellilistinn ekki tiltækur í skattaútreikningsstillingunum.

Ljúktu við eftirfarandi skrefum til að virkja fellilistann í eiginleikaútgáfustillingu Skattaútreiknings.

1. [Virkja Microsoft Power Platform sameining og opna Dataverse umhverfi.](#enable)
2. [Settu upp fjármála- og rekstrar sýndareiningar.](#install)
3. [Skráðu þig í Azure Active Directory (Azure AD) umsókn.](#register)
4. [Veittu forritaheimildir í fjármála- og rekstrarforritum.](#grant)
5. [Stilltu gagnagjafa sýndaraðila.](#configure)
6. [Virkja Dataverse sýndareiningar.](#virtual)
7. [Settu upp tengda forritið fyrir skattaútreikning.](#set-up)
8. [Flytja inn og setja upp Dataverse Uppsetning líkanakortlagningar.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a> Virkja Microsoft Power Platform sameining og opna Dataverse umhverfi

Samþætting fjármála- og rekstrarappa við Microsoft Power Platform hægt að virkja þegar þú býrð til nýtt fjármála- og rekstrarumhverfi í Microsoft Dynamics Lífsferilsþjónusta (LCS). Frekari upplýsingar er að finna í [Microsoft Power Platform samþætting - Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Þegar þú hefur lokið, nafn a Microsoft Power Platform umhverfi mun birtast í **Power Platform Samþætting** kafla.

1. Í LCS, í fjármála- og rekstrarumhverfi þínu, í **Power Platform Samþætting** kafla, finndu og gerðu athugasemd við **Nafn umhverfisins** gildi fyrir tengt umhverfi.

    [![Umhverfisheiti gildi.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Í [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com/environments), á **Umhverfi** flipann, veldu umhverfið sem passar við **Nafn umhverfisins** verðmæti sem þú skrifaðir niður.
3. Á **Upplýsingar** síðu, finndu **Umhverfisslóð** verðmæti Dataverse umhverfi. Skráðu þetta gildi, því þú þarft það inn [Skref 7. Settu upp tengda forritið fyrir skattaútreikning](#set-up).
4. Gakktu úr skugga um að þú getir opnað Dataverse umhverfi í vafranum þínum með því að velja **Umhverfisslóð** gildi.

    [![Dataverse umhverfissíðu.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Haltu Dataverse umhverfi opið í vafranum þínum. Þú munt þurfa það inn [Skref 5. Stilltu gagnagjafa sýndaraðila](#configure).

Fyrir frekari upplýsingar, sjá [Virkjaðu Microsoft Power Platform samþættingu](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a> Settu upp fjármála- og rekstrar sýndareiningar

The Dataverse lausn fyrir fjármál og rekstur sýndareiningar verður að vera uppsett frá Microsoft AppSource sýndareiningalausn.

1. Í AppSource, Finndu [Fjármál og rekstur sýndaraðili](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Veldu **Náðu í það núna**.
3. Í **Veldu umhverfi** reit, sláðu inn **Nafn umhverfisins** gildi sem þú skráðir áðan.
4. Veldu gátreitina og veldu síðan **Settu upp**.

Þegar uppsetningunni er lokið geturðu fundið **Fjármál og rekstur sýndaraðili** app í [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com/), undir **Auðlindir** \> **Dynamics 365 forrit**.

Fyrir frekari upplýsingar, sjá [Að fá sýndaraðilalausnina](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a> Skráðu þig í Azure AD umsókn

Þú verður að skrá þig í Azure AD umsókn á sama leigjanda og fjármála- og rekstraröppin, svo hægt sé að hringja í þau Dataverse.

1. Í [Azure gátt](https://portal.azure.com), fara til **Azure Active Directory\> App skráningar**.
2. Veldu **Ný skráning**, og sláðu inn eftirfarandi upplýsingar:

    - **Nafn** – Sláðu inn einstakt nafn.
    - **Tegund reiknings** - Koma inn **Einhver Azure AD Skrá** (eins leigjandi eða fjölleigjandi).
    - **Beina URI** – Skildu þennan reit eftir auðan.

3. Veldu **Skrá**.
4. Munið gildi **Kenni forrits (biðlari)** því það þarf að nota það síðar.

    [![Azure AD Auðkenni umsóknar (viðskiptavinar).](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Búðu til samhverfan lykil fyrir forritið.
6. Í nýja forritinu skaltu velja **Vottorð og leyndarmál**.
7. Veljið **Nýtt leyniorð biðlara**.
8. Sláðu inn lýsingu, veldu fyrningardagsetningu og veldu síðan **Vista**. Lykill verður búinn til og sýndur. Afritaðu gildið til síðari nota.

Fyrir frekari upplýsingar, sjá [Skráðu þig Azure AD umsókn](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a> Veittu forritaheimildir í fjármála- og rekstrarforritum

Dataverse notar Azure AD forrit sem þú bjóst til til að kalla fjármála- og rekstrarforrit. Þess vegna verður forritið að vera treyst af fjármála- og rekstrarforritum og tengt notandareikningi sem hefur viðeigandi réttindi. Í fjármála- og rekstraröppunum verður þú að búa til sérstakan þjónustunotanda sem hefur réttindi **aðeins** til virkni sýndareiningarinnar. Þessi þjónustunotandi má ekki hafa önnur réttindi. Eftir að þú hefur lokið þessu skrefi, hvaða forrit sem hefur leyndarmálið Azure AD forritið sem þú bjóst til mun geta hringt í umhverfi fjármála- og rekstrarappa og fengið aðgang að virkni sýndaraðila.

1. Í þínu umhverfi, farðu til **Kerfisstjórn** \> **Notendur** \> **Notendur**.
2. Veldu **Nýtt** til að bæta við nýjum notanda og sláðu inn eftirfarandi upplýsingar:

    - **notandanafn** - Koma inn **gagnaverssamþætting** eða annað gildi.
    - **Notandanafn** - Koma inn **samþætting gagnavers** eða annað gildi.
    - **Veitandi** – Stilltu þennan reit á **NonAAD**.
    - **Tölvupóstur** - Koma inn **gagnaverssamþætting** eða annað gildi. (Gildið þarf ekki að vera gildur tölvupóstreikningur.)

3. Úthlutaðu **CDS sýndareiningarforrit** öryggishlutverki fyrir notandann.
4. Fjarlægðu öll önnur hlutverk, þar á meðal **Kerfisnotandi**.
5. Fara til **Kerfisstjórn** \> **Uppsetning** \> **Azure Active Directory umsóknir** að skrá Dataverse. 
6. Bættu við röð og síðan í **Auðkenni viðskiptavinar** reit, sláðu inn **Auðkenni umsóknar (viðskiptavinar).** gildi sem þú skráðir áðan.
7. Færið inn lýsandi nafn í reitinn **Heiti**. Til dæmis, slá inn **Dataverse Samþætting**.
8. Í **notandanafn** reit, sláðu inn notandakennið sem þú bjóst til áður.

Fyrir frekari upplýsingar, sjá [Veittu forritaheimildir í Finance and Operations forritum](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Skilgreining gagnagjafa sýndareiningar

Þú verður að veita Dataverse með fjármála- og rekstrarforritinu til að tengjast.

1. Þinn Dataverse umhverfi ætti samt að vera opið í vafranum þínum frá [Skref 1. Virkja Microsoft Power Platform sameining og opna Dataverse umhverfi](#enable). Veldu stillingarhnappinn (gírtáknið) efst til hægri og veldu síðan **Ítarlegar stillingar**.

    [![Að opna Ítarlegar stillingar í Dataverse umhverfi.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Á **Stillingar** fellivalmynd, veldu **Stjórnsýsla**.

    [![Stjórnsýsla.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Veldu **Gagnaheimildir sýndaraðila**.

    [![Gagnaheimildir sýndaraðila.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Veldu gagnagjafann sem er nefndur **Fjármál og rekstur**.

    [![Uppspretta fjármál og rekstrargagna.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Sláðu inn eftirfarandi upplýsingar úr fyrri skrefum:

    - **Markaðsslóð** - Sláðu inn slóðina þar sem þú getur fengið aðgang að fjármála- og rekstraröppum.
    - **OAuth vefslóð** - Koma inn `https://login.windows.net/`.
    - **Auðkenni leigjanda** - Tilgreindu leigjanda þinn. Þetta gildi getur verið lénið á netfangi fyrirtækisins (eins og contoso.com).
    - **AAD umsókn auðkenni** – Sláðu inn **Auðkenni umsóknar (viðskiptavinar).** verðmæti sem skapast áður.
    - **AAD umsóknarleyndarmál** – Sláðu inn leyndarmálið sem var búið til áður.
    - **AAD auðlind** - Koma inn **00000015-0000-0000-c000-000000000000**. Þetta gildi er Azure AD forrit sem táknar fjármála- og rekstrarforrit. Það ætti alltaf að vera þetta sama gildi.

6. Vista breytingarnar.
7. Lokaðu síðunni til að fara aftur á **Stjórnsýsla** síðu, þar sem þú byrjar [Skref 6. Virkja Dataverse sýndareiningar](#virtual).

    [![Lokar einingunni til að breyta.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Fyrir frekari upplýsingar, sjá [Stilltu gagnagjafa sýndaraðila](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a> Virkja Dataverse sýndareiningar

Sýnileiki sýndareininganna úr fjármála- og rekstraröppum verður að vera stilltur á **Já** áður en hægt er að neyta þeirra með Tax Calculation stillingum.

> [!NOTE]
> Þú getur sleppt þessu skrefi með því að virkja sýndareiningar tengdar skattútreikningi með einum smelli inn [Skref 8. Settu upp tengda forritið fyrir skattútreikning](#import). Hins vegar mælum við með því að þú kveikir handvirkt á að minnsta kosti eina sýndareiningu til að gefa til kynna að tengingin milli fjármála- og rekstrarappa og Dataverse er vel við lýði.

1. Í þínum Dataverse umhverfi, á **Stjórnsýsla** síðu, veldu síuhnappinn (trektartákn) í efra hægra horninu.

    [![Síuhnappur.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Í **Ítarleg uppgötvun** glugga, í **Leitaðu að** reit, veldu **Tiltækar fjármála- og rekstrareiningar**.
3. Bættu við eftirfarandi reglu: **Nafn** –**Inniheldur** –**CompanyInfoEntity**. Veldu síðan **Niðurstöður**.

    [![Ítarlegri leitargluggi.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Veldu **CompanyInfoEntity** í leitarniðurstöðum, veldu **Sýnilegt** gátreitinn og veldu síðan **Vista**.

    [![Stilla sýnileika einingarinnar.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Endurtaktu fyrri skref fyrir eftirfarandi einingar sem vísað er til í skattaútreikningsstillingunum:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeading
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Aðeins er hægt að sækja fyrstu 5.000 færslur aðila Dataverse og gert aðgengilegt í fellilistanum fyrir uppsetningu Skattreiknings.

Frekari upplýsingar er að finna í [Virkja Microsoft Dataverse sýndareiningar](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a> Settu upp tengda forritið fyrir skattaútreikning

1. Í RCS, opnaðu **Eiginleikastjórnun** vinnusvæði og virkjaðu eftirfarandi eiginleika:

    - Stuðningur við Dataverse gagnagjafa rafrænnar skýrslugerðar
    - Stuðningur við gagnagjafa skattþjónustu Dataverse
    - Altækir eiginleikar

2. Fara til **Rafræn skýrslugerð**, og síðan, í **Tengdir tenglar** kafla, veldu **Tengd forrit**.

    [![Tengd forrit.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

3. Veldu **Nýtt** til að bæta við færslu og sláðu inn eftirfarandi upplýsingar.

    - **Heiti** - Sláðu inn nafn.
    - **Tegund** – Veldu **Dataverse**.
    - **Umsókn** - Sláðu inn þinn Dataverse umhverfisins **Umhverfisslóð** gildi, sem þú skráðir í [Skref 1. Virkja Microsoft Power Platform samþættingu og opnaðu þitt Dataverse umhverfi](#enable).
    - **Leigjandi** - Sláðu inn leigjanda þinn.
    - **Sérsniðin vefslóð** - Sláðu inn þinn Dataverse URL og bæta við **/api/data/v9.1** til þess.

4. Veldu **Athugaðu tenginguna**, og síðan, í glugganum sem birtist, veldu **Smelltu hér til að tengjast valið fjarforrit**.

    [![Athugar tenginguna.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
5. Gakktu úr skugga um að þú fáir "Árangur!" Skilaboð sem gefa til kynna að tengingunni hafi tekist.

    [![Skilaboð um árangur.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a> Flytja inn og setja upp Dataverse Uppsetning líkanakortlagningar

Microsoft býður upp á sjálfgefnar líkanakortastillingar fyrir aðila, allt frá fjármála- og rekstrarforritum til skattaútreikninga.

1. Í RCS, farðu til **Rafræn skýrslugerð**.
2. Í **Stillingarveitur** kafla, á flísum fyrir **Microsoft** veitir, veldu **Geymslur**.

    [![Geymslur.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Veldu **Alþjóðleg stillingargeymsla** taka upp og veldu síðan **Opið**.
4. Undir **Skattagagnalíkan** \> **Skattreikningsgagnalíkan**, veldu **Dataverse Módelkortlagning** uppsetningu.
5. Á **Útgáfur** Flýtiflipa, veldu útgáfu sem passar við útgáfu fjármála- og rekstrarforrita og veldu síðan **Flytja inn**.

    [![Að flytja inn Dataverse Uppsetning líkanakortlagningar.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > The **Dataverse Módelkortlagning** stillingar virka aðeins á hæstu innfluttu útgáfunni. Þess vegna ættir þú ekki að flytja inn útgáfu af **Dataverse Módelkortlagning** stillingar sem er hærri en útgáfan af uppsetningu skattaútreiknings sem þú ætlar að innleiða. Til dæmis, ef þú ætlar að innleiða útgáfu 40.50.225 af skattaútreikningsstillingunum, ættir þú aðeins að flytja inn útgáfu 40.50.13 af **Dataverse Módelkortlagning** uppsetningu. Þú ættir ekki að flytja inn útgáfu 40.54.14. Annars verður misræmi í gagnalíkani í uppsetningunni.

6. Fara aftur til **Rafræn skýrslugerð**, og veldu **Skattstillingar** flísar.
7. Veldu innflutt **Dataverse Módelkortlagning** stillingar og veldu síðan **Breyta**.
8. Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.
9. Í **Tengt forrit** reit skaltu velja tengda forritið sem þú setur upp í [Skref 7. Settu upp tengda forritið fyrir skattútreikning](#set-up).
10. Stilltu **Stilltu sýnileika sýndarborðs** valmöguleika til **Já** til að stilla alla sýndareiningar tengdar skattútreikningi á sýnilegar.

Þú hefur nú lokið uppsetningu fyrir aðalgagnaleitarvirkni. Fellilisti fyrir reiti eins og **Lögaðili**, **söluaðila**, **·**, og **Afhendingartími** frá Dynamics 365 Finance verður nú virkt í **Útgáfa skattreiknings eiginleika** uppsetningu.

[![Fellilisti lögaðila.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
