---
title: Uppfæra í altæka aðila- og aðsetursbókarlíkanið
description: Í þessu efnisatriði er lýst hvernig á að uppfæra gögn tvöfaldrar skráningar í aðilalíkanið og líkan altækrar aðsetursbókar.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 95d272d9076f1ab25230e4efa98e321bdd618062
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407796"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Uppfæra í altæka aðila- og aðsetursbókarlíkanið

[!include [banner](../../includes/banner.md)]



The [Microsoft Azure Data Factory sniðmát](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) hjálpa þér að uppfæra eftirfarandi fyrirliggjandi gögn í tvískrift í aðila og alþjóðlegt heimilisfangabókarlíkan: gögn í **Reikningur**, **samband**, og **Seljandi** töflur og póstföng og netföng.

Eftirfarandi þrjú Data Factory sniðmát eru til staðar. Þeir hjálpa til við að samræma gögnin frá bæði Finance og Operations öppum og viðskiptavina þátttöku öppum.

- **[Partísniðmát](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Uppfærðu gögn í dual-write Party-GAB schema/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra **Partí** og **Hafðu samband** gögn sem tengjast **Reikningur**, **samband**, og **Seljandi** gögn.
- **[Sniðmát fyrir póstfang aðila](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Uppfæra gögn í tvískrifað Party-GAB skema/Uppfæra í póstfang aðila - GAB/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra póstföngin sem tengjast **Reikningur**, **samband**, og **Seljandi** gögn.
- **[Rafræn heimilisfang sniðmát aðila](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Uppfæra gögn í tvískrifað Party-GAB skema/Uppfæra í rafrænt heimilisfang aðila - GAB/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra rafræn heimilisföng sem tengjast **Reikningur**, **samband**, og **Seljandi** gögn.

Í lok ferlisins eru eftirfarandi skrár með kommum aðskilin gildi (.csv) búnar til.

| Skráarheiti | Notkun |
|---|---|
| FONewParty.csv | Þessi skrá hjálpar til við að búa til nýja **Partí** skrár í Finance and Operations appinu. |
| ImportFONewPostalAddressLocation.csv | Þessi skrá hjálpar til við að búa til nýja **Póstfang Staðsetning** skrár í Finance and Operations appinu. |
| ImportFONewPartyPostalAddress.csv | Þessi skrá hjálpar til við að búa til nýja **Póstfang aðila** skrár í Finance and Operations appinu. |
| ImportFONewPostalAddress.csv | Þessi skrá hjálpar til við að búa til nýja **Póstfang** skrár í Finance and Operations appinu. |
| ImportFONewElectronicAddress.csv | Þessi skrá hjálpar til við að búa til nýja **Rafræn heimilisfang** skrár í Finance and Operations appinu. |

Þetta efni útskýrir hvernig á að nota Data Factory sniðmát og uppfæra gögnin þín. Ef þú ert ekki með neinar sérstillingar geturðu notað sniðmátin eins og þau eru. Hins vegar, ef þú ert með sérstillingar fyrir **Reikningur**, **samband**, og **Seljandi** gögn, verður þú að breyta sniðmátunum eins og lýst er í þessu efni.

> [!IMPORTANT]
> Sérstakar leiðbeiningar eru um að keyra sniðmát fyrir póstfang aðila og rafræn heimilisfang aðila. Þú verður að keyra sniðmát aðila fyrst, síðan sniðmát póstfangs aðila og síðan sniðmát fyrir rafrænt heimilisfang aðila. Hvert sniðmát er hannað til að flytja inn í sérstakri gagnaverksmiðju.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur verða að vera til staðar áður en þú getur uppfært í aðila og alþjóðlegt heimilisfangabókarlíkan:

+ Þú verður að hafa [Azure áskrift](https://portal.azure.com/).
+ Þú verður að hafa aðgang að [sniðmátunum](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Þú verður að vera núverandi viðskiptavinur tvöfaldrar skráningar.

## <a name="prepare-for-the-upgrade"></a>Uppfærsla undirbúin

Uppfærsla krefst eftirfarandi undirbúnings:

+ **Full samstilling:** Bæði fjármála- og rekstrarumhverfið og viðskiptaumhverfið eru í fullkomlega samstilltu ástandi fyrir **Reikningur (viðskiptavinur)**, **samband**, og **Seljandi** borðum.
+ **Samþættingarlyklar:** The **Reikningur (viðskiptavinur)**, **samband**, og **Seljandi** töflur í forritum fyrir þátttöku viðskiptavina nota samþættingarlyklana sem eru út úr kassanum. Ef samþættingarlyklarnir voru sérstilltir þarf að sérstilla sniðmátið.
+ **Veislunúmer:** Allt **Reikningur (viðskiptavinur)**, **samband**, og **Seljandi** færslur sem verða uppfærðar hafa aðilanúmer. Færslur sem hafa ekki aðilanúmer verða hunsaðar. Ef þú vilt uppfæra þessar skrár skaltu bæta aðilanúmeri við þær áður en þú byrjar uppfærsluferlið.
+ **Kerfisbilun:** Meðan á uppfærsluferlinu stendur verður þú að taka bæði fjármála- og rekstrarumhverfið og umhverfi viðskiptavina án nettengingar.
+ **Skyndimynd:** Taktu skyndimynd af bæði Finance and Operations öppunum og öppunum fyrir þátttöku viðskiptavina. Þú getur síðan notað skyndimyndirnar til að endurheimta fyrra ástand ef þú þarft.

## <a name="deployment"></a>Nýting

1. Sækja sniðmát frá [Dynamics-365-FastTrack-Innleiðing-Eignir](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
3. Stofnið [tilfangaflokk](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Búið til [geymslureikning](/azure/storage/common/storage-account-create?tabs=azure-portal) í tilfangaflokknum sem var stofnaður.
5. Búa til [gagnaverksmiðju](/azure/data-factory/quickstart-create-data-factory-portal) í tilfangahópnum sem þú bjóst til.
6. Opnaðu gagnaverksmiðjuna og veldu **Höfundur & Monitor** flísar.
7. Í flipanum **Stjórna** skal velja **ARM-sniðmát**.
8. Veldu **Flytja inn ARM sniðmát** að flytja inn **Partí** sniðmát.
9. Flytjið sniðmátið inn í gagnasmiðjuna. Færið inn eftirfarandi gildi fyrir **Upplýsingar um verk** og **Upplýsingar um tilvik**.

    | Reitur | Gildi |
    |---|---|
    | Áskrift | Azure áskriftin |
    | Tilfangaflokkur | Gefðu upp sama tilfang og geymslureikningurinn er stofnaður undir. |
    | Svæði | Svæðið |
    | Heiti verksmiðju | Nafn verksmiðjunnar |
    | FO Linked Service_service Principal Key | Lykill forritsins |
    | Strengur Azure Blob Storage_connection | Azure Blob geymslutengingarstrengurinn |
    | Dynamics Crm Linked Service_password | Lykilorðið fyrir notandareikninginn sem þú tilgreinir sem notandanafn |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Upplýsingar (lén eða leigjanda auðkenni) um leigjanda sem umsókn þín býr undir |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Auðkenni viðskiptavinar forritsins |
    | Dynamics Crm Linked Service_properties_type Properties_username | Notandanafnið sem er notað til að tengjast Dynamics 365 |

    Frekari upplýsingar er hægt að finna í eftirfarandi efni:

    - [Úthluta sniðmáti forðastjóra á handvirkan hátt fyrir hvert umhverfi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Tengdir þjónustueiginleikar](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Afrita gögn með Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Eftir uppsetningu skal staðfesta gagnasöfnin, gagnaflæðið og tengda þjónustu gagnasmiðjunnar.

    ![Gagnasafn, gagnaflæði og tengd þjónusta.](media/data-factory-validate.png)

11. Fara til **Stjórna**. Undir **Tengingar** skal velja **Tengd þjónusta**. Veldu síðan **DynamicsCrmLinkedService**. Í **Breyta tengdri þjónustu (Dynamics CRM)** valmynd, sláðu inn eftirfarandi gildi.

    | Reitur | Gildi |
    |---|---|
    | Heiti | DynamicsCrmLinkedService |
    | lýsing | Tengdar þjónustur til að tengjast við CRM-tilvik til að sækja gögn eininga |
    | Tengjast með keyrslutíma samþættingar | AutoResolvelntegrationRuntime |
    | Uppsetningargerð | Nettenging |
    | Uri þjónustu | `https://<organization-name>.crm[x].dynamics.com` |
    | Sannvottunargerð | Office365 |
    | Notandanafn | |
    | Aðgangsorð eða Azure-lyklageymsla | Aðgangsorð |
    | Aðgangsorð | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Búðu þig undir að keyra Data Factory sniðmátin

Þessi hluti lýsir uppsetningunni sem er nauðsynleg áður en þú keyrir sniðmát póstfang aðila og rafrænt heimilisfang aðila Data Factory.

### <a name="setup-to-run-the-party-postal-address-template"></a>Uppsetning til að keyra póstfangssniðmát aðila

1. Skráðu þig inn á þátttökuforrit viðskiptavina og farðu á **Stillingar** \> **Sérstillingar**. Síðan, á **Almennt** flipann, stilltu tímabeltisstillingu fyrir kerfisstjórareikninginn. Tímabelti verður að vera í samræmdum alhliða tíma (UTC) til að uppfæra „gild frá“ og „gild til“ dagsetningar póstfanga úr Finance and Operations forritum.

    ![Tímabeltisstilling fyrir kerfisstjórareikninginn.](media/ADF-1.png)

2. Í Data Factory, á **Stjórna** flipi, undir **Alþjóðlegar breytur**, búðu til eftirfarandi alþjóðlega færibreytu.

    | Númer | Heiti | Gerð | Gildi |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | strengur | Þessi færibreyta bætir raðnúmeri við nýstofnað póstföng sem forskeyti. Vertu viss um að gefa upp streng sem stangast ekki á við póstföng í Finance and Operations öppum og öppum fyrir þátttöku viðskiptavina. Til dæmis, notaðu **ADF-PAD-**. |

    ![PostalAddressIdPrefix alþjóðleg færibreyta búin til á flipanum Stjórna.](media/ADF-2.png)

3. Þegar þú hefur lokið skaltu velja **Birta allt**.

    ![Birta allt hnappinn.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Uppsetning til að keyra sniðmát fyrir rafræn heimilisfang aðila

1. Í Data Factory, á **Stjórna** flipi, undir **Alþjóðlegar breytur**, búðu til eftirfarandi alþjóðlegu færibreytur.

    | Númer | Heiti | Gerð | Gildi |
    |---|---|---|---|
    | 1 | IsFOSource | ból | Þessi færibreyta ákvarðar hvaða aðalkerfisföngum er skipt út ef árekstrar koma upp. Ef gildið er **satt**, munu aðalheimilisföngin í Finance and Operations forritum koma í stað aðalheimilisfönganna í viðskiptavinaþátttökuforritum. Ef gildið er **rangt**, munu aðalheimilisföngin í forritum fyrir þátttöku viðskiptavina koma í stað aðalheimilisfönganna í Finance and Operations forritum. |
    | 2 | ElectronicAddressIdPrefix | strengur | Þessi færibreyta bætir raðnúmeri við nýstofnuð rafræn heimilisföng sem forskeyti. Vertu viss um að gefa upp streng sem stangast ekki á við rafræn heimilisföng í Finance and Operations öppum og öppum fyrir þátttöku viðskiptavina. Til dæmis, notaðu **ADF-EAD-**. |

    ![IsFOSource og ElectronicAddressIdPrefix alþjóðlegar færibreytur búnar til á flipanum Stjórna.](media/ADF-4.png)

2. Þegar þú hefur lokið skaltu velja **Birta allt**.

## <a name="run-the-templates"></a>Keyra sniðmát

1. Hættu eftirfarandi **Partí**, **·**, **samband**, og **Seljandi** tvískrifa kort sem nota fjármála- og rekstrarforrit:

    + CDS aðilar (msdyn_parties) 
    + Viðskiptavinir V3 (lyklar)
    + Viðskiptavinir V3 (tengiliðir)
    + CDS Tengiliðir V2 (tengiliðir)
    + CDS Tengiliðir V2 (tengiliðir)
    + Lánardrottinn V2 (msdyn_vendors)
    + Tengiliðir V2 (msdyn_contactforparties)
    + Staðsetningar póstfanga CDS-aðila (msdyn_partypostaladdresses)
    + CDS-póstfangsferill V2 (msdyn_postaladdresses)
    + Staðsetningar CDS-póstfanga (msdyn_postaladdresscollections)
    + Tengiliðir aðila V3(msdyn_partyelectronicaddresses)

2. Gakktu úr skugga um að kortin séu fjarlægð af **msdy_dualwriteruntimeconfig** borð inn Dataverse.
3. Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab) úr AppSource.
4. Í Finance and Operations appinu skaltu keyra **Upphafleg samstilling** fyrir eftirfarandi töflur ef þær innihalda gögn:

    + Ávörp
    + Persónubundnar manngerðir
    + Kveðjuorð
    + Titlar tengiliðar
    + Hlutverk ákvarðanatöku
    + Stig viðskiptavildar

5. Í forritinu fyrir þátttöku viðskiptavina skaltu slökkva á eftirfarandi viðbótarskrefum:

    + Reikningsuppfærsla

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings

    + Uppfærsla tengiliðs

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar

    + msdyn_party Update

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party

    + msdyn_vendor Update

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor

    + Heimilisfang viðskiptavinar

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Búa til heimilisfang viðskiptavinar

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Uppfærsla á heimilisfangi viðskiptavinarins

        + Virk útgáfa

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Eyða heimilisfangi viðskiptavinarins

    + msdyn_partypóstfang

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Búa til msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Búa til msdyn_partypostaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Uppfærsla á msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Uppfærsla á msdyn_partypostaladdress

    + msdyn_póstfang

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Búa til msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Búa til msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Búa til msdyn_postaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Uppfærsla á msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Uppfærsla á msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Búa til msdyn_partyelectronicaddress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Uppfærsla á msdyn_partyelectronicaddress

        + Virk útgáfa

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Eyða msdyn_partyelectronicaddress

6. Í forriti viðskiptavinar skal slökkva á eftirfarandi verkflæðum:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

7. Í gagnaverksmiðjunni skaltu keyra sniðmátið með því að velja **Kveiktu núna** eins og sýnt er á eftirfarandi mynd. Þetta ferli gæti tekið nokkrar klukkustundir að ljúka, allt eftir gagnamagninu.

    ![Keyrir sniðmátið.](media/data-factory-trigger.png)

    > [!NOTE]
    > Ef þú ert með sérstillingar fyrir **Reikningur**, **samband**, og **Seljandi**, þú verður að breyta sniðmátinu.

8. Flytja inn nýja **Partí** skrár í Finance and Operations appið.

    1. Sækja **FONewParty.csv** skrá frá Azure Blob geymslu. Leiðin er **partybootstrapping/output/FONewParty.csv**.
    2. Umbreyttu **FONewParty.csv** skrá í Excel skrá og flytja Excel skrána inn í Finance and Operations appið. Að öðrum kosti, ef CSV innflutningurinn virkar fyrir þig, geturðu flutt inn .csv skrána beint. Þetta skref gæti tekið nokkrar klukkustundir að ljúka, allt eftir gagnamagninu. Frekari upplýsingar er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../data-import-export-job.md).

    ![Að flytja inn Dataverse Veisluskrár.](media/data-factory-import-party.png)

9. Í gagnaverksmiðjunni skaltu keyra sniðmát fyrir póstfang aðila og rafræn heimilisfang aðila, hvert á eftir öðru.

    + Póstfangssniðmát aðila uppfærir allar póstfangsfærslur í forritinu fyrir þátttöku viðskiptavina og tengir þær við samsvarandi **Reikningur**, **samband**, og **Seljandi** skrár. Það býr einnig til þrjár .csv skrár: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv og ImportFONewPostalAddress.csv.
    + Sniðmát fyrir rafræn heimilisfang aðila setur öll rafföng í samskiptaforriti viðskiptavina upp og tengir þau við samsvarandi **Reikningur**, **samband**, og **Seljandi** skrár. Það býr einnig til eina .csv skrá: ImportFONewElectronicAddress.csv.

    ![Að keyra sniðmát fyrir póstfang aðila og rafræn heimilisfang aðila.](media/ADF-7.png)

10. Til að uppfæra Finance and Operations appið með þessum gögnum verður þú að umbreyta .csv skránum í Excel vinnubók og [flytja það inn í Finance and Operations appið](/data-entities/data-import-export-job). Að öðrum kosti, ef CSV innflutningurinn virkar fyrir þig, geturðu flutt inn .csv skrárnar beint. Þetta skref gæti tekið nokkrar klukkustundir að ljúka, allt eftir hljóðstyrknum.

    ![Vel heppnaður innflutningur.](media/ADF-8.png)

11. Í forritinu fyrir þátttöku viðskiptavina, virkjaðu eftirfarandi viðbætur:

    + Reikningsuppfærsla

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings

    + Uppfærsla tengiliðs

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar

    + msdyn_party Update

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party

    + msdyn_vendor Update

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor

    + msdyn_partypóstfang

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Búa til msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Búa til msdyn_partypostaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Uppfærsla á msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Uppfærsla á msdyn_partypostaladdress

    + msdyn_póstfang

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Búa til msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Búa til msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Búa til msdyn_postaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Uppfærsla á msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Uppfærsla á msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Búa til msdyn_partyelectronicaddress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Uppfærsla á msdyn_partyelectronicaddress

        + Virk útgáfa

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Eyða msdyn_partyelectronicaddress

12. Í forritinu fyrir þátttöku viðskiptavina skaltu virkja eftirfarandi verkflæði ef þú hefur áður gert þau óvirkjuð:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

13. Keyra á **Partí** skráatengd kort eins og lýst er í [Veislu- og alheimsfangabók](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Útskýring á Data Factory sniðmátunum

Þessi hluti tekur þig í gegnum skrefin í hverju Data Factory sniðmáti.

### <a name="steps-in-the-party-template"></a>Skref í Party sniðmátinu

1. Skref 1 til 6 auðkenna fyrirtækin sem eru virkjuð fyrir tvískrift og búa til síuákvæði fyrir þau.
2. Skref 7-1 til 7-9 sækja gögn bæði úr Finance and Operations appinu og viðskiptavinaforritinu og setja þau gögn í uppfærslu.
3. Skref 8 til 9 bera saman flokksnúmerið fyrir **Reikningur**, **samband**, og **Seljandi** færslur á milli Finance and Operations appsins og viðskiptavinaþátttökuappsins. Öllum færslum sem hafa ekki aðilanúmer er sleppt.
4. Skref 10 býr til tvær .csv skrár fyrir aðilaskrárnar sem þarf að búa til í viðskiptavinaþátttökuforritinu og Finance and Operations appinu.

    - **FOCDSParty.csv** – Þessi skrá inniheldur allar aðilaskrár beggja kerfa, óháð því hvort fyrirtækið er virkt fyrir tvískrifa.
    - **FONewParty.csv** – Þessi skrá inniheldur hlutmengi af skrám aðila sem Dataverse er meðvitaður um (til dæmis frásagnir af **Horfur** tegund).

5. Skref 11 býr til aðilana í forritinu fyrir þátttöku viðskiptavina.
6. Skref 12 sækir alþjóðlegt einstök auðkenni (GUID) aðila úr forritinu fyrir þátttöku viðskiptavina og sviðsetur þau þannig að hægt sé að tengja þau við **Reikningur**, **samband**, og **Seljandi** skrár í síðari skrefum.
7. Skref 13 tengir **Reikningur**, **samband**, og **Seljandi** skrár með GUID aðila.
8. Skref 14-1 til 14-3 uppfæra **Reikningur**, **samband**, og **Seljandi** skrár í þátttökuforriti viðskiptavina með GUID aðila.
9. Skref 15-1 til 15-3 undirbúa **Hafðu samband fyrir Party** skrár fyrir **Reikningur**, **samband**, og **Seljandi** skrár.
10. Skref 16-1 til 16-7 sækja tilvísunargögn eins og kveðjur og persónugerðir og tengja þau við **Hafðu samband fyrir Party** skrár.
11. Skref 17 sameinar **Hafðu samband fyrir Party** skrár fyrir **Reikningur**, **samband**, og **Seljandi** skrár.
12. Skref 18 flytur inn **Hafðu samband fyrir Party** skrár inn í forritið fyrir þátttöku viðskiptavina.

### <a name="steps-in-the-party-postal-address-template"></a>Skref í sniðmát fyrir póstfang aðila

1. Skref 1-1 til 1-10 sækja gögn bæði úr Finance and Operations appinu og viðskiptavinaþátttökuforritinu og setja þau gögn í uppfærslu.
2. Skref 2 afnormaliserar póstfangsgögnin í Finance and Operations appinu með því að sameina póstfangið og póstfang aðila.
3. Skref 3 afritar og sameinar reiknings-, tengiliða- og heimilisfangsgögn frá viðskiptavinaforritinu.
4. Skref 4 býr til .csv skrár fyrir Finance and Operations appið til að búa til ný heimilisfangsgögn sem eru byggð á reikningi, tengiliðum og heimilisfangi söluaðila.
5. Skref 5-1 býr til .csv skrár fyrir þátttökuforrit viðskiptavinarins til að búa til öll heimilisfangsgögn, byggð á bæði Finance and Operations appinu og viðskiptavinaþátttökuforritinu.
6. Skref 5-2 breytir .csv skránum í Finance and Operations innflutningssnið fyrir handvirkan innflutning.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Skref 6 flytur inn gögn um söfnun póstfanga inn í forritið fyrir þátttöku viðskiptavina.
8. Skref 7 sækir söfnunargögn um póstfang úr þátttökuforriti viðskiptavina.
9. Skref 8 býr til heimilisfang viðskiptavinar og tengir söfnunarauðkenni póstfangs.
10. Skref 9-1 til 9-2 tengja auðkenni aðila og póstfangasafns við póstföng og póstföng aðila.
11. Skref 10-1 til 10-3 flytja heimilisföng viðskiptavina, póstföng og póstföng aðila inn í forritið fyrir þátttöku viðskiptavina.

### <a name="steps-in-the-party-electronic-address-template"></a>Skref í sniðmát fyrir rafræn heimilisfang aðila

1. Skref 1-1 til 1-5 sækja gögn bæði úr Finance and Operations appinu og viðskiptavinaforritinu og setja þau gögn í uppfærslu.
2. Skref 2 sameinar rafræn heimilisföng í þátttökuforriti viðskiptavina frá reiknings-, tengiliða- og söluaðilum.
3. Skref 3 sameinar aðal rafræn heimilisfangsgögn úr viðskiptavinaforritinu og Finance and Operations appinu.
4. Skref 4 býr til .csv skrár.

    - Búðu til ný rafræn heimilisfangsgögn fyrir Finance and Operations appið, byggt á heimilisfangi reiknings, tengiliða og söluaðila.
    - Búðu til ný rafræn heimilisfangsgögn fyrir þátttökuforrit viðskiptavina, byggt á rafrænu heimilisfangi, reikningi, tengiliðum og heimilisfangi söluaðila í Finance and Operations appinu.

5. Skref 5-1 flytur inn rafræn heimilisföng í þátttökuforritið fyrir viðskiptavini.
6. Skref 5-2 býr til .csv skrár til að uppfæra aðalnetföng fyrir reikninga og tengiliði í forritinu fyrir þátttöku viðskiptavina.
7. Skref 6-1 til 6-2 flyttu inn reikninga og tengiliðaaðföng í þátttökuforritið fyrir viðskiptavini.

## <a name="troubleshooting"></a>Úrræðaleit

1. Ef ferlið mistekst skaltu endurræsa gagnaverksmiðjuna. Byrjaðu á misheppnuðu virkninni.
2. Sumar skrár sem eru búnar til af gagnaverksmiðjunni er hægt að nota til að sannprófa gögn.
3. Gagnaverksmiðjan keyrir á .csv skrám. Þess vegna, ef kommur er innifalinn í einhverju svæðisgildi, gæti það truflað niðurstöðurnar. Þú verður að fjarlægja allar kommur úr reitgildum.
4. The **Eftirlit** flipinn veitir upplýsingar um öll skref og gögn sem hafa verið unnin. Veljið tiltekið skref til að kemba þau.

    ![Eftirlitsflipi.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Frekari upplýsingar um sniðmátið

Fyrir frekari upplýsingar um sniðmátið, sjá [Athugasemdir fyrir Azure Data Factory sniðmát readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
