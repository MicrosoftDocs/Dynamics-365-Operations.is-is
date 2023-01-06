---
title: Uppfæra í altæka aðila- og aðsetursbókarlíkanið
description: Í þessari grein er lýst hvernig á að uppfæra gögn tvöfaldrar skráningar í aðilalíkanið og líkan altækrar aðsetursbókar.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 7141f9c7ae4e27013bd655ce78892fc44c181315
ms.sourcegitcommit: e14648b01549bdc17998ffdef6cde273d4e78560
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/09/2022
ms.locfileid: "9242983"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Uppfæra í altæka aðila- og aðsetursbókarlíkanið

[!include [banner](../../includes/banner.md)]



[Microsoft Azure Data Factory-sniðmátin](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) hjálpa til við að uppfæra fyrirliggjandi gögn í tvöföld skráningu á líkan aðila eða altækrar aðsetursbókar: gögn í **Lykill**, **Tengiliður** og **Lánardrottinn** töflum og póstföng og rafræn vistföng.

Eftirfarandi þrjú sniðmát Data Factory eru í boði. Sniðmátið afstemmir gögnin úr bæði forritum fjármála- og reksturs og forritum viðskiptavinar.

- **[Sniðmát aðila](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Uppfæra gögn í tvöfalda skráningu Party-GAB schema/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra gögn fyrir **Aðila** og **Tengilið** sem tengist gögnum fyrir **Lykil**, **Tengilið** og **Lánardrottin**.
- **[Sniðmát póstfangs aðila](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Uppfæra gögn í tvöfalda skráningu Party-GAB schema/Uppfæra í póstfang aðila - GAB/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra póstföng sem tengjast gögnum fyrir **Lykil**, **Tengilið** og **Lánardrottin**.
- **[Sniðmát rafræns vistfangs aðila](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Uppfæra gögn í tvöfalda skráningu Party-GAB schema/Uppfæra í rafrænt vistfang aðila - GAB/arm_template.json)** – Þetta sniðmát hjálpar til við að uppfæra rafræn vistföng sem tengjast gögnum fyrir **Lykil**, **Tengilið** og **Lánardrottin**.

Í lok ferlisins eru eftirfarandi csv-skrár búnar til.

| Skráarheiti | Notkun |
|---|---|
| FONewParty.csv | Þessi skrá auðveldar að stofna nýjar **aðilafærslur** í forriti fjármála- og reksturs. |
| ImportFONewPostalAddressLocation.csv | Þessi skrá auðveldar að stofna nýjar færslur fyrir **Staðsetningu póstfangs** í forriti fjármála- og reksturs. |
| ImportFONewPartyPostalAddress.csv | Þessi skrá auðveldar að stofna nýjar færslur fyrir **Póstfang aðila** í forriti fjármála- og reksturs. |
| ImportFONewPostalAddress.csv | Þessi skrá auðveldar að stofna nýjar færslur fyrir **Póstfangs** í forriti fjármála- og reksturs. |
| ImportFONewElectronicAddress.csv | Þessi skrá auðveldar að stofna nýjar færslur fyrir **Rafrænt vistfang** í forriti fjármála- og reksturs. |

Í þessari grein er að finna leiðbeiningar um notkun Data Factory-sniðmáts og uppfærslu gagnanna. Ef engar sérstillingar eru til staðar er hægt að nota sniðmátin eins og þau eru. Ef sérstillingar eru fyrir hendi fyrir **Lykill**, **Tengiliður** og **Lánardrottinn**, þarf að breyta sniðmátinu eins og lýst er í þessari grein.

> [!IMPORTANT]
> Sérstakar leiðbeiningar eru um hvernig á að keyra sniðmát fyrir póstfang aðila og rafrænt vistfang aðila. Fyrst þarf að keyra sniðmát aðila, síðan sniðmát fyrir póstfang aðila og síðan sniðmát fyrir rafrænt vistfang aðila. Hvert sniðmát er hannað til að flytja inn í sérstakri gagnasmiðju.

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur eru nauðsynlegar til að uppfæra í líkan aðila og altækrar aðsetursbókar:

+ Þú verður að vera með [Azure-áskrift](https://portal.azure.com/).
+ Þú verður að hafa aðgang að [sniðmátunum](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Þú verður að vera núverandi viðskiptavinur tvöfaldrar skráningar.

## <a name="prepare-for-the-upgrade"></a>Uppfærsla undirbúin

Uppfærsla krefst eftirfarandi undirbúnings:

+ **Full samstilling:** Bæði umhverfi fjármála- og reksturs og umhverfi viðskiptavinar eru í fullri samstillingarstöðu fyrir töflurnar **Lykill (viðskiptavinur)**, **Tengiliður** og **Lánardrottinn**.
+ **Samþættingarlyklar:** Töflurnar **Lykil (viðskiptavinur)**, **Tengiliður** og **Lánardrottinn** í forritum viðskiptavinar nota tilbúna samþættingarlykla sem fylgja með. Ef samþættingarlyklarnir voru sérstilltir þarf að sérstilla sniðmátið.
+ **Aðilanúmer**: Allar færslur **Lykils (viðskiptavinar)**, **Tengiliðar** og **Lánardrottins** sem verða uppfærðar eru með númer aðila. Færslur án númers aðila verða hunsaðar. Ef uppfæra á þær færslur skal bæta númeri Aðila við þær áður en uppfærsluferlið er sett í gang.
+ **Stöðvun kerfis**: Í uppfærsluferlinu þarf að slökkva á nettengingu fyrir bæði umhverfi fjármála- og reksturs og umhverfi viðskiptavinar.
+ **Skyndimynd**: Takið skyndimyndir af bæði forritum fjármála- og reksturs og forritum viðskiptavinar. Hægt er að nota skyndimyndirnar til að endurheimta fyrri stöðu ef á þarf að halda.

## <a name="deployment"></a>Uppsetning

1. Sækið sniðmátið úr [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
3. Stofnið [tilfangaflokk](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Búið til [geymslureikning](/azure/storage/common/storage-account-create?tabs=azure-portal) í tilfangaflokknum sem var stofnaður.
5. Stofnið [gagnasmiðju](/azure/data-factory/quickstart-create-data-factory-portal) í tilfangaflokki sem var stofnaður.
6. Opnið gagnasmiðjuna og veljið reitinn **Stýra og fylgjast með**.
7. Í flipanum **Stjórna** skal velja **ARM-sniðmát**.
8. Veljið **Flytja inn ARM-sniðmát** til að flytja inn sniðmátið **Aðili**.
9. Flytjið sniðmátið inn í gagnasmiðjuna. Færið inn eftirfarandi gildi fyrir **Upplýsingar um verk** og **Upplýsingar um tilvik**.

    | Svæði | Gildi |
    |---|---|
    | Áskrift | Azure-áskriftin |
    | Tilfangaflokkur | Gefðu upp sömu tilfang og geymslureikningurinn er stofnaður undir. |
    | Svæði | Svæðið |
    | Heiti verksmiðju | Heiti verksmiðju |
    | FO Linked Service_service Principal Key | Lykill forritsins |
    | Strengur Azure Blob Storage_connection | Tengingarstrengurinn Azure Blob Storage. |
    | Dynamics Crm Linked Service_password | Aðgangsorðið fyrir notandareikninginn sem þú tilgreinir sem notendanafnið |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Upplýsingar (heiti léns eða leigjandakenni) um leigjanda sem forritið heyrir undir. |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Biðlarakenni forritsins. |
    | Dynamics Crm Linked Service_properties_type Properties_username | Notandanafnið sem er notað til að tengjast Dynamics 365 |

    Frekari upplýsingar er hægt að finna í eftirfarandi efni:

    - [Úthluta sniðmáti forðastjóra á handvirkan hátt fyrir hvert umhverfi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Tengdir þjónustueiginleikar](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Afrita gögn með Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Eftir uppsetningu skal staðfesta gagnasöfnin, gagnaflæðið og tengda þjónustu gagnasmiðjunnar.

    ![Gagnasafn, gagnaflæði og tengd þjónusta.](media/data-factory-validate.png)

11. Opnið **Stjórna**. Undir **Tengingar** skal velja **Tengd þjónusta**. Veljið síðan **DynamicsCrmLinkedService**. Á svarglugganum **Breyta tengdri þjónustu (Dynamics CRM)** skal færa inn eftirfarandi gildi.

    | Svæði | Gildi |
    |---|---|
    | Nafn | DynamicsCrmLinkedService |
    | lýsing | Tengdar þjónustur til að tengjast við CRM-tilvik til að sækja gögn eininga |
    | Tengjast með keyrslutíma samþættingar | AutoResolvelntegrationRuntime |
    | Uppsetningargerð | Nettenging |
    | Uri þjónustu | `https://<organization-name>.crm[x].dynamics.com` |
    | Sannvottunargerð | Office365 |
    | Notandanafn | |
    | Aðgangsorð eða Azure-lyklageymsla | Aðgangsorð |
    | Aðgangsorð | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Búðu þig undir að keyra sniðmát Data Factory

Þessi hluti lýsir uppsetningu sem er nauðsynleg áður sniðmát Data Factory fyrir póstfang aðila og rafrænt vistfang aðila eru keyrð.

### <a name="setup-to-run-the-party-postal-address-template"></a>Uppsetning til að keyra sniðmát fyrir póstfang aðila

1. Skráðu þig inn í viðskiptavinaforrit og farðu í **Stillingar** \> **Sérstillingar**. Síðan í flipanum **Almennt** skal skilgreina stillingu tímabeltis fyrir reikning kerfisstjóra. Tímabeltið verður að vera í UTC til að uppfæra „gildir frá“ og „gildir til“ dagsetningar póstfanga úr forritum fjármála- og reksturs.

    ![Tímabeltisstilling fyrir kerfisstjórnarreikninginn.](media/ADF-1.png)

2. Í Data Factory, í flipanum **Stjórna**, undir **Altækar færibreytur**, skal búa til eftirfarandi altæka færibreytu.

    | Númer | Nafn | Gerð | Gildi |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | strengur | Þessi færibreyta bætir raðnúmeri við nýlega stofnuð póstföng sem forskeyti. Gættu þess að bjóða upp á streng sem stangast ekki á við póstföng í forritum fjármála- og reksturs og viðskiptavina. Notaðu t.d. **ADF-PAD-**. |

    ![Altæk PostalAddressIdPrefix-færibreyta stofnuð fyrir flipann Stjórna.](media/ADF-2.png)

3. Þegar því er lokið skal velja **Birta allt**.

    ![Hnappurinn „Birta allt“.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Uppsetning til að keyra sniðmát fyrir rafrænt vistfang aðila

1. Í Data Factory, í flipanum **Stjórna**, undir **Altækar færibreytur**, skal búa til eftirfarandi altækar færibreytur.

    | Númer | Nafn | Gerð | Gildi |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Þessi færibreyta ákvarðar hvaða aðalaðsetrum kerfisins er skipt út ef upp koma árekstrar. Ef gildið er **satt** munu aðalaðsetrin forritum fjármála- og reksturs koma í staðinn fyrir aðalaðsetrin í viðskiptavinaforritum. Ef gildið er **ósatt** munu aðalaðsetrin í viðskiptavinaforritum koma í staðinn fyrir aðalaðsetrin í forritum fjármála- og reksturs. |
    | 2 | ElectronicAddressIdPrefix | strengur | Þessi færibreyta bætir raðnúmeri við nýlega stofnuð rafræn vistföng sem forskeyti. Gættu þess að bjóða upp á streng sem stangast ekki á við rafræn vistföng í forritum fjármála- og reksturs og viðskiptavina. Notaðu t.d. **ADF-EAD-**. |

    ![Altækar færibreytur IsFOSource og ElectronicAddressIdPrefix búnar til í flipanum „Stjórna“.](media/ADF-4.png)

2. Þegar því er lokið skal velja **Birta allt**.

## <a name="run-the-templates"></a>Keyra sniðmátin

1. Stöðvaðu eftirfarandi varpanir tvöfaldrar skráningar á **Aðila**, **Lykli**, **Tengilið** og **Lánardrottni** sem nota forrit fjármála- og reksturs:

    + CDS-aðilar (msdyn_parties) 
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

2. Gangið úr skugga um að varpanir séu fjarlægðar úr **msdy_dualwriteruntimeconfig**-töflunni í Dataverse.
3. Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab) úr AppSource.
4. Í forriti fjármála- og reksturs skal keyra **Upphafleg samstilling** fyrir eftirfarandi töflur ef þær innihalda gögn:

    + Ávörp
    + Persónubundnar manngerðir
    + Kveðjuorð
    + Titlar tengiliðar
    + Hlutverk ákvarðanatöku
    + Stig viðskiptavildar

5. Í forriti viðskiptavinar skal slökkva á eftirfarandi skrefum viðbótar:

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

    + Customeraddress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Stofnun customeraddress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Uppfærsla customeraddress

        + Eyða

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Eyðing customeraddress

    + msdyn_partypostaladdress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Stofnun msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Stofnun msdyn_partypostaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Uppfærsla msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Uppfærsla msdyn_partypostaladdress

    + msdyn_postaladdress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Stofnun msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Stofnun msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Stofnun msdyn_postaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Uppfærsla msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Update of msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Stofnun msdyn_partyelectronicaddress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Uppfærsla msdyn_partyelectronicaddress

        + Eyða

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Eyðing msdyn_partyelectronicaddress

6. Í forriti viðskiptavinar skal slökkva á eftirfarandi verkflæðum:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

7. Í gagnasmiðjunni skal keyra sniðmátið með því að velja **Ræsa núna** eins og sýnt er á eftirfarandi mynd. Þetta ferli gæti tekið nokkrar klukkustundir að ljúka allt eftir því hvert gagnamagnið er.

    ![Keyrir sniðmátið](media/data-factory-trigger.png)

    > [!NOTE]
    > Ef sérstillingar eru fyrir hendi fyrir **Lykill**, **Tengiliður** og **Lánardrottinn**, þá þarf að breyta sniðmátinu.

8. Flytja inn nýjar færslur fyrir **Aðili** í fjármála- og reksturs-forritið.

    1. Sækið **FONewParty.csv**-skrána úr Azure Blob geymslu. Slóðin er **partybootstrapping/output/FONewParty.csv**.
    2. Umbreytið **FONewParty.csv** skránni í Excel-skrá og flytjið Excel-skrána inn í fjármála- og reksturs-forritið. Ef CSV-innflutningurinn virkar fyrir þig, þá geturðu flutt .csv-skrána beint inn. Þetta skref gæti tekið nokkrar klukkustundir að keyra, en það fer allt eftir gagnamagninu. Frekari upplýsingar er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../data-import-export-job.md).

    ![Innflutningur Dataverse-aðilafærslna.](media/data-factory-import-party.png)

9. Í gagnasmiðjunni skal keyra sniðmát fyrir rafrænt vistfang aðila og síðan sniðmát fyrir póstfang aðila á eftir hinu.

    + Sniðmát fyrir póstfang aðila uppfærir allar færslur póstfangs í viðskiptavinaforriti og tengir þær við samsvarandi færslur fyrir **Lykil**, **Tengilið** og **Lánardrottin**. Það býr einnig til þrjár csv-skrár: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv og ImportFONewPostalAddress.csv.
    + Sniðmát fyrir rafrænt vistfang aðila uppfærir öll rafræn vistföng í viðskiptavinaforriti og tengir þau við samsvarandi færslur fyrir **Lykil**, **Tengilið** og **Lánardrottin**. Þetta býr einnig til eina .csv-skrá: ImportFONewElectronicAddress.csv.

    ![Keyra sniðmát póstfangs og rafrænna vistfanga aðila.](media/ADF-7.png)

10. Til að uppfæra forrit fjármála- og reksturs með þessum gögnum þarf að umbreyta csv-skránum í Excel-vinnubók og [flytja hana inn í forrit fjármála- og reksturs](../data-import-export-job.md). Ef csv-innflutningurinn virkar fyrir þig, þá geturðu flutt csv-skrárnar beint inn. Þetta gæti tekið nokkrar klukkustundir að ljúka þessu skrefi en það fer allt eftir magninu.

    ![Innflutningi lokið.](media/ADF-8.png)

11. Í forriti viðskiptavinar skal kveikja á eftirfarandi skrefum viðbótar:

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

    + msdyn_partypostaladdress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Stofnun msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Stofnun msdyn_partypostaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Uppfærsla msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Uppfærsla msdyn_partypostaladdress

    + msdyn_postaladdress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Stofnun msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Stofnun msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Stofnun msdyn_postaladdress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Uppfærsla msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Update of msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Búa til

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Stofnun msdyn_partyelectronicaddress

        + Update

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Uppfærsla msdyn_partyelectronicaddress

        + Eyða

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Eyðing msdyn_partyelectronicaddress

12. Í forritum viðskiptavinar skal virkja eftirfarandi verkflæði ef slökkt var á þeim:

    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna í reikningstöflu
    + Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu
    + Uppfæra lánardrottna í reikningstöflu
    + Uppfæra lánardrottna í lánardrottnatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu
    + Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu

13. Keyrið varpanir tengdar færslu í **Aðili** eins og lýst er í [Aðili og altæk aðsetursbók](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Skýringar á sniðmátum Data Factory

Í þessum hluta er farið í gegnum skrefin í hverju sniðmáti Data Factory.

### <a name="steps-in-the-party-template"></a>Skref í sniðmáti fyrir aðila

1. Skref 1 til 6 bera kennsl á fyrirtækin þar sem tvöföld skráning er virk og býr til síuákvæði fyrir þau.
2. Skref 7-1 til 7-9 sækja gögn bæði úr forriti fjármála- og reksturs og viðskiptavinaforrit og undirbúa þessi gögn fyrir uppfærslu.
3. Skref 8 til 9 bera saman aðilanúmerið fyrir færslur **Lykils**, **Tengiliðar** og **Lánardrottins** milli forrita fjármála- og reksturs og viðskiptavinar. Öllum færslum sem eru ekki með aðilanúmer er sleppt.
4. Skref 10 býr til tvær csv-skrár fyrir aðilafærslurnar sem þarf að stofna í viðskiptavinaforritinu og forriti fjármála- og reksturs .

    - **FOCDSParty.csv** – Þessi skrá inniheldur allar aðilafærslur úr báðum kerfum burtséð frá því hvort tvöföld skráning sé virk í fyrirtækinu.
    - **FONewParty.csv** – Þessi skrá inniheldur undirsafn af aðilafærslum sem Dataverse veit um (til dæmis lyklum af gerðinni **Viðfang**).

5. Skref 11 býr til aðila í forriti viðskiptavinarins.
6. Skref 12 sækir altæk einkvæmt kennimerki (GUID) aðilanna úr viðskiptavinaforritinu og undirbýr þau þannig að hægt sé að tengja þau við færslur fyrir **Lykil**, **Tengilið** og **Lánardrottin** í næstu skrefum.
7. Skref 13 tengir færslur **Lykils**, **Tengiliðar** og **Lánardrottins** við GUID aðila.
8. Skref 14-1 til 14-3 uppfæra færslurnar **Lykill**, **Tengiliður** og **Lánardrottinn** í viðskiptavinaforritinu með GUID aðila.
9. Skref 15-1 til 15-3 undirbýr færslurnar **Tengiliður fyrir aðila** fyrir færslurnar **Lykill**, **Tengiliður** og **Lánardrottinn**.
10. Skref 16-1 til 16-7 sækja tilvísunargögn eins og kveðjur og persónubundnar manngerðir og tengir þau við **Tengiliður fyrir aðila** færslurnar.
11. Skref 17 sameinar færslurnar **Tengiliður fyrir aðila** fyrir færslurnar **Lykill**, **Tengiliður** og **Lánardrottinn**.
12. Skref 18 flytur inn færslurnar **Tengiliður fyrir aðila** í viðskiptavinaforritið.

### <a name="steps-in-the-party-postal-address-template"></a>Skref í sniðmátið Póstfang aðilans

1. Skref 1-1 til 1-10 sækja gögn bæði úr forriti fjármála- og reksturs og viðskiptavinaforriti og undirbýr gögnin fyrir uppfærslu.
2. Skref 2 afstaðlar gögn póstfangs í forriti fjármála- og reksturs með því að sameina póstfangið og póstfang aðila.
3. Skref 3 fjarlægir tvítekningar og sameinar aðsetursgögn lykils, tengiliðar og lánardrottins úr viðskiptavinaforritinu.
4. Skref 4 býr til csv-skrár fyrir forrit fjármála- og reksturs til að búa til ný aðsetursgögn sem byggja á aðsetrum lykils, tengiliðar og lánardrottins.
5. Skref 5-1 býr til csv-skrár fyrir viðskiptavinaforritið til að búa til öll aðsetursgögn sem byggja á bæði forriti fjármála- og reksturs og viðskiptavinaforriti.
6. Skref 5-2 umbreytir csv-skránum í innflutningssnið fjármála- og reksturs fyrir handvirkan innflutning.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Skref 6 flytur inn söfnunargögn póstfangs í viðskiptavinaforritið.
8. Skref 7 sækir söfnunargögn póstfangs úr viðskiptavinaforritinu.
9. Skref 8 býr til aðsetursgögn viðskiptavinar og tengir við söfnunarkenni póstfangs.
10. Skref 9-1 til 9-2 tengja söfnunarkenni aðila og póstafangs við póstföng og póstföng aðila.
11. Skref 10-1 til 10-3 flytja inn aðsetur viðskiptavina, póstföng og póstföng aðila í viðskiptavinaforritið.

### <a name="steps-in-the-party-electronic-address-template"></a>Skref í sniðmáti rafræns vistfangs aðila

1. Skref 1-1 til 1-5 sækja gögn bæði úr forriti fjármála- og reksturs og viðskiptavinaforrit og undirbúa þessi gögn fyrir uppfærslu.
2. Skref 2 sameinar rafræn vistföng í viðskiptavinaforritið úr lykla-, tengiliðar- og lánardrottnaeiningum.
3. Skref 3 sameinar gögn rafræns aðalvistfangs úr viðskiptavinaforritinu og forriti fjármála- og reksturs.
4. Skref 4 býr til .csv skrár.

    - Búðu til ný gögn rafræns vistfangs fyrir forrit fjármála- og reksturs sem byggja á aðsetrum lykils, tengiliðar og lánardrottins.
    - Búðu til ný gögn rafræns vistfangs fyrir viðskiptavinaforritið sem byggja á rafrænu vistfangi, aðsetrum lykils, tengiliðar og lánardrottins í forriti fjármála- og reksturs.

5. Skref 5-1 flytur inn rafræn heimilisföng í forrit viðskiptavinar.
6. Skref 5-2 býr til csv-skrár til að uppfæra aðalaðsetur fyrir lykla og tengiliði í viðskiptavinaforritinu.
7. Skref 6-1 til 6-2 flytur inn aðalaðsetur lykla og tengiliða í viðskiptavinaforritið.

## <a name="troubleshooting"></a>Úrræðaleit

1. Ef ferlið mistekst skal endurkeyra gagnasmiðjuna. Byrja á misheppnuðu aðgerðinni.
2. Sumar skrár sem gagnasmiðjan býr til er hægt að nota fyrir gagnaprófun.
3. Gagnasmiðjan keyrir á .csv skrám. Ef komma er þar af leiðandi innifalin í einhverju reitargildi gæti það truflað niðurstöðurnar. Fjarlægja verður allar kommur úr gildum reita.
4. Flipinn **Eftirlit** veitir upplýsingar um öll skref og afgreidd gögn. Veljið tiltekið skref til að kemba þau.

    ![Eftirlitsflipi.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Frekari upplýsingar um sniðmátið

Þú getur fengið viðbótarupplýsingar um sniðmátið í [Upplýsingaskrá með athugasemdum við sniðmát Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

