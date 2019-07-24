---
title: Setja upp kennslu fyrir Regression Suite Automation Tool
description: Þetta efni er kennsluefni sem sýnir hvernig á að setja upp Regression Suite Automation Tool (RSAT).
author: kfend
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ab81e95c2e31adfefd4e5c4367a61baa7c251c43
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703830"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Setja upp kennslu fyrir Regression Suite Automation Tool
Þetta efnisatriði er kennsla sem hjálpar þér að fá skipulag og byrja með RSAT og verkfærin sem tengjast því að nota RSAT. 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Notaðu verkfæri þín í internetvafranum til að sækja niður og vista þessa síðu á PDF-sniði. 

## <a name="key-concepts"></a>Lykilhugtök

- Kynntu þér uppsetningu og forsendur sem þarf fyrir þau mismunandi forrit sem styðja Regression Suite Automation Tool (RSAT).
- Kynntu þér hvernig eiginleikinn verkskráning í Microsoft Dynamics 365 for Finance and Operations, ásamt Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps, gerir þér kleift að stofna, skilgreina, keyra, rannsaka og tilkynna um prófunaratriði.
- Styrktu starfandi notendur til að skrá viðskiptaverkefni með því að nota verkskráningu í Finance and Operations og breyttu síðan verkskráningunum í pakka með sjálfvirkum prófum, án þess að þurfa að skrifa frumkóða.

## <a name="before-you-begin"></a>Áður en hafist er handa

### <a name="prerequisites"></a>Forkröfur

- Krafist er umhverfis Finance and Operations sem keyrir Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0 (apríl, 2019) eða síðar fyrir þetta kennsluefni. Fyrir viðskiptavini sem eru að nota Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 er verkvangsuppfærsla 20 (PU20) eða nýrri einnig studd.
- Notandinn verður að hafa stjórnandaréttindi í umhverfi Finance and Operations.
- Þú verður að hafa aðgang að leigjanda viðskiptavinar í LCS og Azure DevOps (áður þekkt sem Microsoft Visual Studio Team Services \[VSTS\]).
- Notandinn sem er að stofna og stjórna prófunarpökkum verður að hafa Azure DevOps prófunaráætlanir eða prófunarstjóraleyfi. Eftirfarandi heimildir veita þér einnig aðgang að prófunaráætlunum:
    - Visual Studio Enterprise-leyfi
    - Visual Studio Test Professional-leyfi
    - MSDN Platforms-áskrifandaleyfi
- RSAT verður að hafa aðgang að prófunarumhverfi í gegnum vafra.
- Til að mynda og breyta prófunarbreytum verður þú að vera með Microsoft Excel uppsett.

## <a name="configure-azure-devops"></a>Skilgreina Azure DevOps

### <a name="user-eligibility"></a>Hæfni notanda

Gakktu úr skugga um að notandinn sé stofnaður í Azure DevOps og hafi áskriftarstig sem veitir aðgang að prófunaráætlunum í Azure. Leyfis fyrir prófunaráætlanir Azure DevOps er aðeins krafist ef notandinn mun stofna og stjórna prófunartilvikum (þ.e.a.s., ekki allir RSAT-notendur þurfa þetta leyfi). Upplýsingar um leyfiskröfur er að finna í [Leyfisskilyrði](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Stofna nýtt Azure DevOps-verk
RSAT notar Azure Devops fyrir prófunartilvikið og stjórnun prófunarpakkans, skýrslugerð og könnun á niðurstöðum prófanakeyrslna. 

> [!NOTE]
> Þú getur notað núverandi Azure DevOps-verk. En ef núverandi Azure DevOps-verkið er sett upp þannig að það hafi sérsniðið sniðmát muntu fá villuna „VSTS-samstillingarvillu“ þegar þú samstillir prófunartilvik frá Viðskiptaferlavinnslu (BPM) til Azure DevOps (sjá kaflann [Prófa samstillingu frá BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)). Ef eftirfarandi bestu venjur hefur verið fylgt fyrir sérsniðið sniðmát, munt þú geta samstillt prófunardæmin við Azure DevOps. (Þessar bestu venjur eru skráðar í villuboðunum.)

- Ekki eyða neinum gerðum vinnuliða eða tilbúnum reitum.
- Ekki eyða neinni stöðu í gerð vinnuliðar.
- Ekki bæta neinum skyldusvæðum við gerð vinnuliðar.

![Villuboð með lista yfir bestu starfsvenjur](./media/setup_rsa_tool_02.png)

Að öðrum kosti mælum við með því að þú stofnir nýtt Azure DevOps-verk fyrir þetta kennsluefni. Nánari upplýsingar er að finna í [Vandamál við samstillingu við BPM með sérsniðnu Azure DevOps (VSTS) ferlissniði](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Opnaðu Azure DevOps-slóðina (`https://dev.azure.com/<Azure DevOps Name>`).
2. Veldu **Stofna verk** efst í hægra horninu á síðunni Azure DevOps.

    ![Stofna verkhnapp](./media/setup_rsa_tool_03.png)

3. Fylltu út í eftirfarandi reiti og veldu síðan **Stofna**:

    - **Verknafn**
    - **Útgáfustjórnun** - Veldu **Team Foundation útgáfustjórnun**. Athugaðu að sjálfgefinn valkostur, **Git**, er ekki studdur.
    - **Ferli vinnuliða**

    ![Stofnaðu nýjan svarglugga verks](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Stofna aðgangsmerki notanda

Í þessu kennsluefni notar þú LCS Viðskiptaferlavinnslu (BPM) til að búa til prófunarsafn og samstilla prófunaratriði þín við Azure DevOps. Þú þarft aðgangsmerki notanda til að samstilla BPM við Azure DevOps.

1. Veldu notandasíðutáknið efst í hægra horni síðunnar fyrir Azure DevOps verkið og veldu síðan **Öryggi**.

    ![Öryggisskipun](./media/setup_rsa_tool_05.png)

2. Í vinstri glugganum, undir **Öryggi** velurðu **Aðgangsmerki notanda**. Veldu síðan **Nýtt tákn**.

    ![Hnappurinn Nýtt tákn á flipanum Aðgangsmerki í Notendastillingum](./media/setup_rsa_tool_06.png)

3. Fylltu út í eftirfarandi reiti og veldu síðan **Stofna**:

    - **Nafn**
    - **Gildistími (UTC)** – Veldu **Sérskilgreint** og notaðu síðan dagsetningavalið til að velja síðustu tiltæku dags.
    - **Umfang** - Veldu valkostinn **Ótakmarkaður aðgangur**.

    ![Stofnaðu nýjan svarglugga aðgangsmerkis notanda](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Skráðu niður aðgangsmerkið sem er stofnað. Þú þarft það síðar þegar þú setur upp RSAT-skilgreiningu.

    ![Aðgangsmerki notanda](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Skilgreina LCS-verk

Þú þarft Lifecycle Services (LCS)-verkefni fyrir aðalprófunarsafnið þitt. LCS Viðskiptaferlavinnsla (BPM) er notuð sem aðalsafn fyrir prófunardæmin þín. BPM er notað til að stjórna og dreifa prófunarsöfnum yfir LCS-verk. Til dæmis mun Microsoft-samstarfsaðili eða sjálfstæður smásali hugbúnaðar (ISV) sem er að byggja prófunarsöfn gefa út prófunardæmi á formi BPM-safna. Í BPM eru prófunardæmin skipulögð af viðskiptaferli. BPM skilgreinir ekki framkvæmdaröð eða -tíðni staðinna prófana. Þessum aðgerðum er stjórnað í Azure DevOps, eins og er lýst síðar í þessu efnisatriði.  

Fyrir LCS-verkefnið er hægt að nota núverandi innleiðingu viðskiptavina eða samstarfsverkefni.

### <a name="update-the-lcs-language"></a>Uppfæra LCS-tungumál

> [!NOTE]
> Svo að notendaviðmótið (UI) geti sýnt viðskiptaferli á réttan hátt verður valið tungumál LCS að vera stillt á **Enska (Bandaríkin)**.

1. Farðu í LCS-innleiðingarverk.
2. Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Tungumálaval**.

    ![Skipanir í valmyndinni Stillingar](./media/setup_rsa_tool_09.png)

3. Í reitnum **Valið tungumál** velurðu **Enska (Bandaríkin)** og síðan velurðu **Vista**.

    ![Flipinn Tungumálaval í Notendastillingum](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>Skilgreina LCS til að tengjast við Azure DevOps-verk

Ef þú stofnaðir nýtt Azure DevOps-verk áður skaltu skilgreina LCS-verkið þannig að það tengist því. Að öðrum kosti geturðu haldið áfram í næsta kafla, ef LCS-verkið þitt er þegar tengt við Azure DevOps-verkið.

1. Farðu í LCS-innleiðingarverk.
2. Veldu hnappinn **Valmynd** og veldu síðan **Verkefnisstillingar**.

    ![Skipun fyrir verkstillingar](./media/setup_rsa_tool_11.png)

3. Í vinstri glugganum skaltu velja **Visual Studio Team Services** og síðan **Setja upp Visual Studio Team Services**.

    ![Flipinn Visual Studio Team Services í verkstillingum](./media/setup_rsa_tool_12.png)

4. Í reitnum **Azure DevOps vefslóð vefsvæðis** skaltu slá inn slóðina að vefsvæði Azure DevOps. Í reitnum **Aðgangsmerki notanda** skaltu slá inn aðgangsmerki notanda sem var stofnað áður.

    > [!NOTE]
    > Þótt VSTS sé núna þekkt sem Azure DevOps skaltu nota gömlu vefslóðina til að tengja LCS við Azure DevOps-verkið. Til dæmis er Azure DevOps-vefslóðin sem er notuð í þessu kennsluatriði `https://dev.azure.com/D365FOFastTrack/`. En í eftirfarandi skýringarmynd er hún slegin inn sem `https://D365FOFastTrack.visualstudio.com/`.

    ![Skref 1 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. Veldu **Haltu áfram**.
6. Í reitnum **Visual Studio Team Services-verk** velurðu VSTS-verk á valinni vefslóð til að tengja við LCS-verkið. Reiturinn **Vinna úr sniðmáti** er sjálfgefið stilltur á **Agile**. Fyrir sérsniðið sniðmát skaltu fara yfir leiðbeiningar á bestu venjum í kaflanum [Stofna nýtt Azure DevOps-verk](#create-a-new-azure-devops-project). Veldu síðan **Halda áfram**.

    ![Skref 2 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. Farðu yfir stillingar þínar og veldu síðan **Vista**.

    ![Skref 3 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. Veldu **Heimila** til að heimila LCS að aðgang að skilgreindu svæði Azure DevOps fyrir þína hönd og til að kveikja á eiginleikum sem samþættast VSTS.

    ![Hnappurinn Heimila](./media/setup_rsa_tool_16.png)

9. Skilaboðagluggi birtist og þar stendur, „Þér verður beint yfir á ytra svæði til að heimila LCS að tengja við Visual Studio Team Services fyrir hönd notanda. Á að halda áfram?“ Velja skal **Já**.

    ![Skilaboðagluggi](./media/setup_rsa_tool_17.png)

10. Veljið **Samþykkja**.

    ![Heimila aðgang](./media/setup_rsa_tool_18.png)

11. Ef þú ert hefur heimild sem notandi ættir notandaviðmótið að skila þér aftur á síðuna LCS-verkefnastillingar.

    ![Heimilaður notandi](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Stofna nýtt BPM-safn

1. Farðu í LCS-innleiðingarverk.
2. Veldu hnappinn **Valmynd** og veldu síðan **Viðskiptaferlavinnsla**.

    ![Skipun Viðskiptaferlavinnslu](./media/setup_rsa_tool_20.png)

3. Veldu **Nýtt safn**.

    ![Hnappurinn Nýtt safn](./media/setup_rsa_tool_21.png)

4. Í reitnum **Heiti safns** slærðu inn heiti og velur síðan **Stofna**. Fyrir þetta kennsluefni skaltu nefna BPM-safnið **RSAT**.

    ![Stofnaðu nýjan svarglugga safns](./media/setup_rsa_tool_22.png)

5. Opnaðu nýtt **RSAT** BPM-safn.
6. Veldu ferlið **Sýnisviðskiptaferli** og síðan velurðu til hægri **Breyta ham**.

    ![Hnappurinn Breyta ham](./media/setup_rsa_tool_23.png)

7. Breyttu gildi bæði reitarins **Heiti** og reitarins **Lýsing** í **Stofna afurð**. Veldu síðan **Vista**.

    ![Reitirnir Heiti og Lýsing](./media/setup_rsa_tool_24.png)

## <a name="finance-and-operations-environment"></a>Umhverfi Finance and Operations

### <a name="version-requirement"></a>Þörf skv. útgáfu

Krafist er prófunar- eða sandkassaumhverfis Finance and Operations test sem keyrir útgáfu 10. Fyrir viðskiptavini sem eru að nota útgáfu 7.3 er verkvangsuppfærsla 20 eða nýrri einnig studd.

> [!NOTE]
> RSAT verður að hafa aðgang að prófunarumhverfi Finance and Operations í gegnum vafra.

### <a name="user-criteria"></a>Notandaskilyrði

Notandinn verður að hafa stjórnandaréttindi á þessu umhverfi.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Stilltu hjálparstillingar til að tengjast LCS

Þetta skref er nauðsynlegt til að tengjast LCS þannig að hægt sé að vista verkskráningu í viðeigandi BPM-safn í LCS í gegnum biðlara Finance and Operations.

1. Opnaðu biðlara Finance and Operations.
2. Farðu í **Kerfisstjórnun \> Uppsetning \> Kerfisfæribreytur**.
3. Á flipanum **Hjálp**, í reitnum **Hjálparskilgreiningar Lifecycle Services** velurðu viðkomandi LCS-verk (**RSAT** fyrir þetta kennsluefni).

    ![Reiturinn Hjálparskilgreiningar Lifecycle Services á flipanum Hjálp](./media/setup_rsa_tool_25.png)

    BPM-söfn eru fyllt út undir viðeigandi LCS-verki.

4. Veljið **Vista**.
5. Þú gætir þurft að endurræsa vafrann til að sjá uppfært hjálparefni.

    ![Tilkynning um að endurræsingu á vafranum](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Verkskráning

> [!NOTE]
> Gakktu úr skugga um að allar verkskráningar þínar hefjist aðalyfirlitinu í Finance and Operations. Haltu stökum skráningum stuttum og leggðu áherslu á eitt viðskiptaverk, eins og að stofna sölupöntun.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Stofnaðu verkskráningu og vistaðu hana í BPM-safnið

Stofnaðu samsvarandi verkskráningu sem hægt er að festa við hið einfaldaða viðskiptaferli sem var stofnað í nýja BPM-safninu.

1. Opnaðu biðlara Finance and Operations.
2. Í aðalyfirlitinu skaltu velja hnappinn **Stillingar** (gírtáknið) og síðan **Verkskráningu**.

    ![Skipanir í valmyndinni Stillingar](./media/setup_rsa_tool_27.png)

3. Veldu **Stofna skráningu**.

    ![Hnappurinn Stofna skráningu](./media/setup_rsa_tool_28.png)

4. Fylltu út reitina **Heiti skráningar** og **Lýsing skráningar** og veldu síðan **Ræsa**.

    ![Reitirnir Heiti skráningar og Lýsing skráningar.](./media/setup_rsa_tool_29.png)

5. Skráðu skrefin til að stofna afurð. Þegar því er lokið skaltu velja **Hættu** til að stöðva skráningu.

    ![Skref til að stofna afurð](./media/setup_rsa_tool_30.png)

6. Veldu **Vista í Lifecycle Services**.

    ![Vista valkosti](./media/setup_rsa_tool_31.png)

    Upplýsingar um söfn er hlaðið úr LCS.

    ![Framvinduvísir](./media/setup_rsa_tool_32.png)

7. Veldu BPM-safn til að tengja við verkskráninguna. Fyrir þetta kennsluefni skaltu velja BPM-safnið **RSAT** sem var stofnað áður og síðan viðskiptaferlið **Stofna afurð** undir því. Veljið síðan **Í lagi**.

    ![Tengja verkskráningu við BPM-safn og viðskiptaferli](./media/setup_rsa_tool_33.png)

    Skilaboðin „Vistað í Lifecycle Services“ birtast.

    ![Skilaboð um árangursríka vistun í LCS](./media/setup_rsa_tool_34.png)

8. Ef þú vilt vista verkskráningu á staðnum og hlaða henni síðan inn í BPM í gegnum LCS skaltu fylgja þessum skrefum:

    1. Þegar skáningu er lokið skaltu velja **Vista á þessa tölvu**.

        ![Vista valkosti](./media/setup_rsa_tool_35.png)

    2. Í tilkynningastiku vafrans skaltu velja **Vista** eða **Vista sem** til að vista skrána staðbundið á tölvuna.

        ![Tilkynningastika](./media/setup_rsa_tool_36.png)

    3. Farðu í BPM-safnið **RSAT** og veldu viðskiptaferlið sem á að vista verkskráninguna gegn.
    4. Á flipanum **Yfirlit** velurðu **Hlaða upp**.

        ![Hnappurinn Hlaða upp](./media/setup_rsa_tool_37.png)

    5. Veldu **Fletta** og veldu .axtr skrána sem þú vistaðir áður. Veldu síðan **Hlaða upp**.

        ![Veldu .axtr skrá til að hlaða upp](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Prófaðu samstillingu úr BPM við Azure DevOps

Núna þegar verkskráning er tengd viðskiptaferlinu verður þú að sannreyna að hægt sé að samstilla viðskiptaferlið og tengda verkskráningu við Azure DevOps sem eiginleika og prófunardæmi (í þessari röð) með því að nota VSTS-samstillingu í LCS.

> [!NOTE]
> Samsvarandi gerð vinnuliðar sem er stofnaður í Azure DevOps verður breytileg eftir því ferlissniði sem þú valdir við skilgreiningu á LCS-verkinu með Azure DevOps, eins og lýst er í kaflanum [Stofna nýtt Azure DevOps-verk](#create-a-new-azure-devops-project).

1. Farðu í BPM-safnið og opnaðu **RSAT**-safnið sem var áður stofnað.
2. Veldu úrfellingarhnappinn (**...**) og veldu **VSTS-samstillingu**.

    ![VSTS-samstillingarskipun í úrfellingarvalmyndinni](./media/setup_rsa_tool_39.png)

    Eftir að VSTS-samstillingu er lokið birtist flipinn **Þarfir** vinstra megin og inniheldur samsvarandi Azure DevOps-vinnulið.

    > [!NOTE]
    > Vinnuliðurinn sem er stofnaður í Azure DevOps mun hafa heiti BPM-safnsins sem titilforskeyti.

    ![Flipinn Þarfir](./media/setup_rsa_tool_40.png)

3. Endurhlaðið síðuna.
4. Veldu úrfellingarhnappinn (**...**). Þú munt sjá viðbótarvalkost, **Samstilla prófunartilvik**. Veldu þennan valkost.

    ![Dæmi um samstillingarskipun í úrfellingarvalmyndinni](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Ef valkosturinn **Samstilla prófunartilvik** er ekki tiltækur eftir að endurhleðslu síðunnar skaltu fara á heimasíðuna fyrir BPM og velja **Samstilla prófunartilvik** fyrir allt safnið. Þannig þvingar þú í raun samstillingu á allt safnið.
    > 
    > ![Valið Samstillt prófunardæmi fyrir allt safnið](./media/setup_rsa_tool_42.png)

    Þegar samstillinu prófunardæma er lokið er nýtt prófunardæmi stofnað á flipanum **Þarfir**.

    ![Nýtt prófunardæmi á flipanum Þarfir](./media/setup_rsa_tool_43.png)

5. Farðu í Azure DevOps-verkið og veldu **Spjöld \> Vinnuliðir**.

    ![Vinnuliðaskipun undir Spjöldum](./media/setup_rsa_tool_44.png)

6. Staðfestu að vinnuliðurinn og prófunardæmin sem þú voru stofnuð með BPM-samstillingu séu til.

    ![Vinnuliður og prófunardæmi](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>Setja upp og skilgreina RSAT

Hægt er að setja upp RSAT á allar tölvur sem keyra Windows 10 og geta tengst umhverfi Finance and Operations í gegnum vafra (Internet Explorer eða Google Chrome).

> [!NOTE]
> Við mælum með því að þú fjarlægir fyrri útgáfuna áður en þú setur upp nýja útgáfu af verkfærinu.

### <a name="install-an-authentication-certificate"></a>Settu upp sannvottunarvottorð

Til að virkja sannvottun verðurðu að mynda og setja upp vottorð á sömu tölvu og RSAT keyrir á.

#### <a name="generate-a-certificate"></a>Mynda skírteini

1. Til að mynda vottorðaskrá skaltu opna Microsoft Windows PowerShell-glugga sem stjórnandi og keyra eftirfarandi skipun.

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Opnaðu vottorðsstjóra með því að slá inn **certlm.msc** í svargluggann **Keyra** og staðfesta að vottorðið **D365 Sjálfvirkt prófunarvottorð** sé myndað undir **Persónulegt \> Vottorð**.

    > [!NOTE]
    > Passaðu að slá inn **certlm.msc**, ekki **certmgr.msc**, vegna þess að vottorðin eru geymd á tölvunni þinni.

    ![D365 Sjálfvirkt vottorð prófunarvottorðs](./media/setup_rsa_tool_46.png)

3. Hægri-smelltu á vottorðið og veldu síðan **Afrita**.
4. Farðu í **Trusted Root Certification Authorities \> Vottorð**.

    ![Vottorðamappa undir möppunni Trusted Root Certification Authorities](./media/setup_rsa_tool_47.png)

5. Í valmyndinni **Aðgerð** velurðu **Líma** til að afrita vottorðið á staðsetninguna **Trusted Root Certification Authorities**.

    ![Líma-skipun í aðgerðavalmyndinni](./media/setup_rsa_tool_48.png)

6. Til að fá fingrafar af uppsettu vottorði, en án bila eða sérstafa, skaltu opna gluggann Windows PowerShell sem stjórnandi og keyra eftirfarandi skipanir.

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Vistaðu fingrafarið því þú þarft það síðar þegar þú uppfærir .wif-skrárnar fyrir Application Object Server (AOS) og setur upp RSAT-stillingar.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>Skilgreina AOS-tölvuna til að treysta tengingunni

> [!NOTE]
> Ef umhverf Finance and Operations er Lag 2+ verður fingrafar vottorðs að vera uppfært í wif.config skránni fyrir **allar** AOS-tölvur fyrir umhverfið.

1. Stofnaðu Remote Desktop Protocol (RDP)-tengingu við AOS-tölvuna. Skráningarupplýsingar eru tiltækar á umhverfisupplýsingasíðunni í LCS.
2. Opnaðu Microsoft Internet Information Services (IIS) og finndu **AOSService** á listanum yfir vefsvæði.

    ![AOSService á lista yfir vefsvæði](./media/setup_rsa_tool_49.png)

3. Hægrismelltu á **Kannaðu** að opna möppuna **\<Drif\>: \\AosService\\WebRoot**. Finndu skrána **wif.config**.

    ![Skráin Wif.config í möppunni WebRoot](./media/setup_rsa_tool_50.png)

4. Uppfærðu skrána **wif.config** með því að bæta við nýrri heimildarfærslu fyrir vottorðið og heiti heimildar, eins og sýnt er í eftirfarandi dæmi.

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Ef fleiri notendur eru að nota sama forrit Finance and Operations, þarf hver notandi að búa til aðskilið fingrafar og bæta verður hverju af því fingrafari við í kaflanum **\<lyklar\>**.

5. Ef fleiri en ein AOS-tölva er til staðar skaltu endurtaka skref 3 til 4 fyrir hverja viðbótartölvu.

    > [!NOTE]
    > Ólíkt eldri umhverfum á lagi 2 er nýju umhverfi beitt á lagi 2 umhverfi með tveimur AOS-tilvikum.

6. Hlaupa **iisreset** á öllum AOS-tölvum.

    > [!NOTE]
    > Ef þú hefur ekki stjórnandaréttindi til að keyra **iisreset** á tölvu á lagi 1 skaltu síðunni Umhverfisupplýsingar í LCS velja Viðhalda > Endurræsa þjónustu.

#### <a name="tier-2-environment"></a>Umhverfi lags 2+

Ef notast er við umhverfi Finance and Operations á lagi 2+ (Sandbox: stöðluð samþykktarprófun eða nýrra) skaltu staðfesta eða stilla eftirfarandi stýriskráarstillingar á tölvunni þar sem RSAT er sett upp. Þetta skref er nauðsynlegt vegna þess að það hjálpar þér að koma í veg fyrir villur í sannprófun eða RSAT-tengingu.

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>Setja upp RSAT

1. Farðu á <https://www.microsoft.com/download/details.aspx?id=57357> og veldu **Sækja**.
2. Veldu allar skrárnar og veldu síðan **Næst**.

    ![Val á öllum skrám](./media/setup_rsa_tool_51.png)

3. Tvísmelltu á .msi-pakkann til að keyra uppsetningarforritið. Þegar uppsetningu er lokið skaltu síðan velja **Ljúka**.

    ![RSAT Installer-skrá](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Settu upp Selenium og vafradrif

Í eldri útgáfum af RSAT þurfti að setja upp Selenium og vafradrif. Það þarf ekki lengur að setja upp þessi drif vegna þess að þau eru sjálfkrafa sett upp.

1. Í fyrsta skipti sem þú opnar RSAT færðu kvaðiningum um að sækja sjálfkrafa og setja Selenium upp. Nánari upplýsingar er að finna í kaflanum [Skilgreina RSAT](#configure-rsat).
2. Áður en þú getur keyrt prófunardæmi færðu kvaðningu um að sækja sjálfvirkt og setja upp vafradrifið sem samsvarar sjálfgefna vafranum sem er valinn í RSAT-stillingu. Nánari upplýsingar er að finna í kaflanum [Sækja og keyra prófunardæmi](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Hafist handa með RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Stofna prófunaráætlun og prófunarpakka

1. Farðu í Azure DevOps-verkið og veldu **Prófunaráætlanir**.

    ![Skipunin Prófunaráætlanir](./media/setup_rsa_tool_53.png)

2. Veldu **Ný prófunaráætlun**.

    ![Hnappurinn Ný prófunaráætlun](./media/setup_rsa_tool_54.png)

3. Fylltu út reitinn **Heiti** og veldu síðan **Stofna**. Fyrir þetta kennsluefni skaltu nefna prófunaráætlunina **RSAT-prófunaráætlun**.

    ![Svarglugginn Ný prófunaráætlun](./media/setup_rsa_tool_55.png)

4. Veldu plústáknið (**+**) og veldu síðan **Fast safn** til að stofna fast safn undir nýrri prófunaráætlun. Nefndu nýja prófunarsafnið **T01 - Gera á lager**.

    > [!NOTE]
    > Einnig er hægt að stofna safn byggt á fyrirspurnum, ef þú vilt að nýju prófunardæmin úr BPM verði sjálfkrafa dregin inn í RSAT-prófunarpakka.

    ![Stofna fast safn](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Hengdu prófunardæmi við prófunarpakka

1. Veldu **Bæta við núverandi** hægra megin til að bæta núverandi prófunardæmum við prófunarpakkann.

    ![Bæta fyrirliggjandi hnappi við](./media/setup_rsa_tool_57.png)

2. Á síðunni **Bæta prófunardæmum við safn** velurðu **Keyra fyrirspurn** og síðan velurðu prófunardæmi til að bæta við prófunarpakkann. Fyrir þetta kennsluefni skaltu velja prófunardæmið **Stofna nýja vöru**. Veldu síðan **Bæta við prófunardæmum** í neðra hægra horninu á síðunni (þessi hnappur er ekki sýndur í eftirfarandi mynd).

    ![Hnappurinn Keyra fyrirspurn](./media/setup_rsa_tool_58.png)

    Prófunardæminu er bætt við prófunarpakkann **T01-Gera í lager**.

    ![Prófunardæmi bætt við prófunarpakkann](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Stilla RSAT

1. Opnaðu RSAT.

    ![RSAT-tákn](./media/setup_rsa_tool_60.png)

2. Þú færð viðvörunarskilaboð þar sem stendur „Regression Suite Automation Tool krefst Selenium, viltu sækja það sjálfvirkt og setja upp núna?“ Velja skal **Já**.

    ![Viðvörunarboð](./media/setup_rsa_tool_61.png)

3. Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horninu og fylltu síðan út eftirfarandi reiti í valmyndinni sem birtist:

    - **Azure DevOps-slóð** – Sláðu inn vefslóð Azure DevOps-verksins, eins og `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Aðgangsmerki** - Sláðu inn aðgangsmerkið sem leyfir verkfærinu að tengjast Azure DevOps. Notaðu aðgangsmerki notanda sem þú bjóst til fyrr í þessari kennsluefni. Nánari upplýsingar er að finna í [Sannvotta aðgang með aðgangsmerkjum notenda](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Heiti verkefnis** - Veldu heiti fyrir Azure DevOps-verkið.
    - **Prófunaráætlun** - Veldu Azure DevOps-prófunaráætlunina sem inniheldur prófunardæmin. Nánari upplýsingar er að finna í [Stofna prófunaráætlanir og prófunarpakka](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Þegar þú hefur valið prófunaráætlun skaltu velja **Prófa tengingu** til að prófa tengingu þína við Azure DevOps.
    - **Hýsilheiti** – Skráðu hýsilheiti prófunarumhverfis Finance and Operations, eins og **\<myaos\>.cloudax.dynamics.com**. Hafðu ekki forskeytin **https://** eða **http://** með.
    - **SOAP-hýsilheiti** – Skráðu SOAP-hýsilheiti prófunarumhverfis Finance and Operations. Yfirleitt er heiti SOAP-hýsils það sama og hýsilheitið en með viðskeytið **soap**. Hér er dæmi: **\<myaos\>soap.cloudax.dynamics.com**. Hafðu ekki forskeytin **https://** eða **http://** með.

        > [!NOTE]
        > Til að finna hýsilheiti og heiti SOAP-hýsils skaltu opna IIS Manager, hægri-smella á **Vefsvæði \> AOSService** og velja síðan **Breyta bindingum**. Gildin í dálknum **Heiti hýsils** veita þér hýsilheitið og heiti SOAP-hýsils (heiti SOAP-hýsils er með viðskeytið **soap** í vefslóðinni).

        ![Hýsilheiti og heiti SOAP-hýsils í dálkinum Heiti hýsils](./media/setup_rsa_tool_63.png)

    - **Notandaheiti stjórnanda** – Skráðu netfang stjórnanda í prófunarumhverfi Finance and Operations.
    - **Fingrafar** - Sláðu inn fingrafar auðkenningarvottorðsins, eins og lýst er hér að framan í þessu kennsluefni.
    - **Vinnuskráarsafn** – Tilgreindu staðsetningu möppu til að geyma sjálfvirkniskrár prófunar, eins og Excel-prófunargagnaskrár. Til dæmis, sláðu inn eða veldu **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Ef nafnið á möppunni er með bilum mun framkvæmdin mistakast þar sem ekki verður hægt að finna möppuna. Þetta vandamál er þekkt og ætti að vera leiðrétt í nýjustu útgáfunni af verkfærinu.

    - **Sjálfgefinn vafri** – Veldu annaðhvort **Internet Explorer** eða **Google Chrome**. Gakktu úr skugga um að viðeigandi vafradrif hafi verið sett upp.
    - **Tímamörk prófunar** – Tilgreindu tímamörk í mínútum fyrir prófanir. Þegar tímalokin renna út er öllum virkum gluggum lokað og prófanir í bið takast ekki.
    - **Tímalok prófunaraðgerða** – Þessi reitur stýrir tímalokum í mínútum fyrir biðlarabeiðnir í umhverfi Finance and Operation. Yfirleitt ætti sjálfgefið gildi (2 mínútur) að vera nóg. Hinsvegar þegar um er að ræða hægari umhverfi gætirðu viljað hækka gildið ef villur sem tengjast tímalokum eiga sér stað.
    - **Heiti fyrirtækis** – Skráðu heiti fyrirtækis sem á að nota sem sjálfgefið fyrirtæki í Finance and Operations þegar Excel-færibreytuskrár eru stofnaðar. Þú getur breytt fyrirtækinu seinna með því að breyta Excel-færibreytuskránni.

    ![Svargluggi stillinga](./media/setup_rsa_tool_62.png)

4. Veldu **Nota** til að nota og vista stillingarnar.

    Til að vista núverandi stillingar í skilgreiningaskrá á tölvunni skaltu velja **Vista sem**. Til að endurheimta stillingarnar úr skilgreiningaskrá á tölvunni skaltu velja **Opna**.

5. Veldu **Loka** til að loka svarglugganum.

### <a name="load-and-run-test-cases"></a>Sækja og keyra prófunardæmi

1. Veldu **Sækja** til að sækja prófunaráætlunina **RSAT-prófunaráætlun** úr Azure DevOps-verkinu.

    ![Hnappurinn Sækja](./media/setup_rsa_tool_64.png)

2. Veldu prófunardæmið **Stofna nýja vöru** úr prófunarpakkanum og veldu síðan **Nýtt \> Mynda prófunarkeyrslu- og færibreytuskrár**.

    ![Skipunin Mynda prófunarkeyrslu og færibreytuskrár í nýju valmyndinni](./media/setup_rsa_tool_65.png)

    Excel-færibreytuskráin er stofnuð í staðbundnu möppunni sem þú tilgreindir í RSAT-skilgreiningunni (til dæmis, **C:\\Temp\\RegressionTool**).

    ![Excel-færibreytuskrá stofnuð](./media/setup_rsa_tool_66.png)

3. Ef þú vilt vista breytuskrár skaltu velja **Hlaða upp**. Sjálfvirkniskrám prófunar allra valda prófana er hlaðið upp á Azure DevOps fyrir seinni tíma notkun. (Þessar skrár innihalda Excel-færibreytuskrár prófana.)

    Á þennan hátt geturðu valið **Sækja** til að sækja færibreytuskrár (og sjálfvirkniskrár) úr prófunardæminu beint af Azure DevOps. Þú þarft ekki að endurnýja færibreytuskrárnar. Þessi nálgun verður mikilvæg seinna þegar þú vilt halda breytingum í færibreytuskránni og vilt ekki að skrifað verði yfir þær.

4. Til að staðfesta að sjálfvirkniskrár og færibreytuskrár séu vistaðar á Azure DevOps skaltu fara í Azure DevOps-verkið, velja **Spjald \> Vinnuliður** og síðan prófunardæmið **Stofna nýja vöru**. Á flipanum **Viðhengi** ættirðu að sjá fjórar skrár:

    - **.cs** – C\# sjálfvirkniskrá
    - **.dll** – Þýdd sjálfvirkniskrá sem samsetning
    - **.xlsx** – Excel-færibreytuskrá
    - **.xml** – Skráningarskrá

    ![Skrár á flipanum Viðhengi](./media/setup_rsa_tool_67.png)

5. Veldu prófunardæmið sem á að keyra og veldu síðan **Keyra**.

    > [!NOTE]
    > Áður en þú keyrir prófunardæmi og ef þú ert að nota Internet Explorer sem vafra, skaltu passa að skjáborðsupplausn þín sé stillt á **100%** í **Windows skjástillingar \> Kvarði og útlit**. Ef þú getur ekki breytt þessari stillingu á sýndarvél (VM) skaltu breyta henni á biðlaranum (fartölvu) sem þú ert að reyna að komast í VM af. Upplausnarstillingarnar erfast síðan með stillingum VM-skjásins.

    ![Skjáborðsupplausn stillt á 100%](./media/setup_rsa_tool_68.png)

6. Ef vafradrifin eru ekki uppsett í kerfinu færðu viðvörunarskilaboð sem segja: „Þessi aðgerð þarfnast drifs fyrir \<heiti vafra\>. Viltu sækja hann sjálfvirkt og setja upp núna?“ Velja skal **Já**.

    ![Viðvörunarboð fyrir Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Viðvörunarboð fyrir Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Ef þú er að nota Chrome sem vafra og færð villuboð sem segir að setan hafi ekki verið stofnuð vegna þess að útgáfan Chrome sé ekki rétt skaltu sækja nýjasta Chrome-drifið frá <http://chromedriver.chromium.org/downloads> í möppuna **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Almennt\\Ytra\\Selenium**.

    ![Villuboð fyrir Chrome](./media/setup_rsa_tool_71.png)

    Prófunardæmið er keyrt og reiturinn **Niðurstaða** er uppfærður.

    ![Framvinduvísir](./media/setup_rsa_tool_72.png)

    Ef þú hefur fylgt þessu kennsluefni eins og það er skrifað, þá mun prófunardæmið **Stofna nýja vöru** ekki takast, vegna þess að það verkskráningin fyrir stofnun vöru vistaði vöruheitið sem harðkóðað gildi. Ef þú endurkeyrir sama prófunardæmið ættirðu að fá villuskilaboð vegna þess að varan er þegar til.

    ![Niðurstöðureitur stilltur á Stóðst ekki](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Skoða prófunarniðurstöður

1. Tvísmelltu á prófunardæmið sem tókst ekki.

    Þú fékkst villuboð.

    ![Villuboð](./media/setup_rsa_tool_73.png)

2. Veldu **Upplýsingar** til að skoða öll villuboðin.

    ![Öll villuboðin](./media/setup_rsa_tool_74.png)

3. Til að skoða nákvæma útgáfu af villuskilaboðum í Azure DevOps skaltu velja **Opna í Azure DevOps**. Í Azure DevOps geturðu skoðað stöðu prófunardæmisins og upplýsingar villuboða.

    ![Upplýsingar villuboða í Azure DevOps](./media/setup_rsa_tool_75.png)

4. Til að skoða niðurstöðurnar beint í Azure DevOps-verkinu skaltu fara í **Prófunaráætlanir \> Prófunaráætlanir \> Keyrslur**. Tvísmelltu á prófunarkeyrsluna sem þú vilt sjá meiri upplýsingar um.

    ![Listi yfir prófanir í Azure DevOps](./media/setup_rsa_tool_76.png)

5. Flipinn **Keyra samantekt** gefur til kynna að prófunardæmið hafi ekki tekist en hann veitir ekki raunverulegu villuboðin. Til að skoða sundurliðuð villuboð velurðu flipann **Prófunarniðurstöður**.

    ![Flipinn Keyra samantekt](./media/setup_rsa_tool_77.png)

    Flipinn **Prófunarniðurstöður** veitir upplýsingar um prófunardæmið, ásamt útkomunni og villuboðunum.

    ![Flipinn Niðurstöður prófunar](./media/setup_rsa_tool_78.png)

6. Tvísmelltu á viðeigandi skrá til að skoða upplýsingar villuboða.

    ![Upplýsingar villuboða](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Öll villuskilaboð eru einnig tiltæk staðbundið í **C:\\Notendur\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Þú getur einnig flutt út niðurstöður prófunarkeyrslu úr prófunaráætlunarstiginu með því að velja **Flytja út**.

    ![Flytur út prófunaráætlun](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Breyta Excel-færibreytuskrá

1. Opnaðu RSAT.
2. Veldu prófdæmið og veldu síðan **Breyta** til að opna Excel-færibreytuskrána.

    Á blaðinu **EcoResProductCreate** skaltu athuga að gildið í reinum **Afurðarnúmer** er harðkóðað. Þú verður að uppfæra þennan reit í nýtt afurðarnúmer áður en prófunardæmið er keyrt aftur.

3. Til að mynda einkvæmt afurðarnúmer fyrir hverja keyrslu án þess að þurfa að enduropna Excel-færibreytuskrána og uppfæra afurðarnúmerið handvirkt í hvert skipti skaltu nota eftirfarandi Excel-formúlu.

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Í viðbót við flipann **Almennt** inniheldur Excel-færibreytuskráin gagnaflipa fyrir hverja síðu Finance and Operations, sem prófið heimsækir.

    ![Reiturinn Afurðarnúmer](./media/setup_rsa_tool_81.png)

4. Veldu **Vista** og lokaðu síðan Excel-skjalinu.
5. Veldu **Hlaða upp** til að vista Excel-færibreytuskrá á Azure DevOps.

    ![Upphleðsla skráar tókst](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Til að keyra prófdæmi í tilteknu notendasamhengi skaltu slá inn netfang notanda í reitnum **Prófa notanda** á flipnum **Almennt** í Excel-færibreytuskránni. Í nýjustu útgáfunni af RSAT hefur útlit reitanna í Excel-færibreytuskránni verið uppfærð, en hugtakið er enn það sama.
    >
    > ![Reiturinn Prófa notanda](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Sannprófa niðurstöður

- Veldu **Keyra** til að endurkeyra prófunardæmið og sannprófa að prófunardæmið hafi staðist. Þú getur skoðað niðurstöðurnar eins og lýst er í kaflanum [Skoða prófunarniðurstöður](#view-the-test-results).

    ![Niðurstöðureitur stilltur á Stóðst](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Keðja prófunardæma

Eitt lykilatriði í RSAT er keðja prófunardæma (það er að segja, geta prófunar til að gefa gildi til annarra prófana). Prófunardæmi eru keyrð í samræmi við skilgreinda röð þeirra í Azure DevOps-prófunaráætlun. (Þessa röð er einnig hægt að uppfæra í prófunarverkfærinu sjálfu.) Ef þú vilt framsenda breytur úr einni prófun í aðra er afar mikilvægt að prófanirnar séu í réttri röð.

Í þessum kafla muntu stofna vistaða breytu í fyrsta prófunardæminu, stofna annað prófunardæmi og senda vistaða breytu úr fyrsta prófunardæminu í annað prófunardæmi. Síðan muntu keyra prófunardæmin sem keðju af prófunardæmum í RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Breyta núverandi verkskráningu til að stofna vistaða breytu

1. Opnaðu biðlara Finance and Operations.
2. Veldu hnappinn **Stillingar** (gírtáknið) og síðan **Verkskráningu**.
3. Veldu **Breyta skráningu**.

    ![Hnappurinn Breyta skráningu](./media/setup_rsa_tool_85.png)

4. Veldu **Opna úr Lifecycle Services**.

    ![Opna úr hnappnum Lifecycle Services](./media/setup_rsa_tool_86.png)

5. Veldu **Velja Lifecycle Services-safnið**.

    ![Veldu hnappinn Lifecycle Services-safnið](./media/setup_rsa_tool_87.png)

    BPM-söfn eru sótt úr LCS.

    ![Framvinduvísir](./media/setup_rsa_tool_88.png)

6. Eftir að BPM-söfn hafa verið sótt úr LCS skaltu velja **RSAT** BPM-safnið og viðskiptaferlið **Stofna nýja vöru** sem verkskráningin var tengd við. Veljið síðan **Í lagi**.

    ![Val á BPM-safn og viðskiptaferli](./media/setup_rsa_tool_89.png)

7. Heiti viðeigandi verkskráningar er slegið inn í reitinn **Heiti skráningar**. Velja **Ræsa**.

    ![Heiti verkskáningarinnar í reitnum Heiti skráningar](./media/setup_rsa_tool_90.png)

8. Farðu í **Afurðaupplýsingastjórnun \> Afurðir** og veldu **Nýtt** til að opna síðuna þar sem upphafleg verkskráning, **Stofna afurð**, var skráð.
9. Veldu **Setja inn skref**.

    > [!NOTE]
    > Nýja skrefið er sett inn á **eftir** skrefinu sem þú valdir í glugganum.

    ![Hnappurinn Setja inn skref](./media/setup_rsa_tool_91.png)

10. Hægrismelltu á reitinn **Afurðarnúmer** og veldu síðan **Verkskráning \> Afrita**.

    ![Afrita skipun](./media/setup_rsa_tool_92.png)

11. Nýju skrefi er bætt í glugganum. Skráðu niður gildið í reitnum **Afurðarnúmer** vegna þess að þú þarft það síðar.

    ![Nýju skrefi bætt við](./media/setup_rsa_tool_93.png)

12. Veldu **Breytingum lokið**.
13. Veldu **Vista í Lifecycle Services** og tengdu nýja verkskráningu við sama BPM-safnið og viðskiptaferlið sem upphafleg verkskráning var tengd við. Nánari upplýsingar er að finna í kaflanum [Stofna verkskráningu og vista hana í BPM-safnið](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Farðu í BPM-safnið og veldu **Samstilla prófunardæmi** til að yfirskrifa þá verkskráningu sem fylgir prófunardæminu í Azure DevOps, eins og lýst er í kaflanum [Prófa samstillingu úr BPM við Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).
15. Opnaðu RSAT og veldu **Sækja** til að endursækja öll prófunardæmin í prófunarpakkanum. Það verður að endurnýja sjálfvirkni- og færibreytuskrár fyrir viðeigandi prófunardæmi með því að velja prófunardæmið og velja síðan **Nýtt \> Mynda prófunarkeyrslu- og færibreytuskrár**, eins og lýst er í kaflanum [Sækja og keyra prófunardæmi](#load-and-run-test-cases).

    > [!NOTE]
    > Ef Excel-færibreytuskráin var skilin eftir opnuð mun endurnýjun ekki takast. Passaðu þess vegna að Excel-færibreytuskráin fyrir prófunardæmið sé lokuð áður en þú myndar nýja Excel-færibreytuskrá.

16. Veldu **Breyta** til að opna nýja Excel-færibreytuskrána. Þú munt sjá nýja færslu **Vistuð breyta** í línu 9. Þessi breyta, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, er vistuð í XML-skrá verkskráningarinnar og hana má nota í síðari prófanir.

    ![Vistuð breytufærsla](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Stofna nýtt prófunardæmi

1. Farðu í **RSAT** BPM-safnð.
2. Veldu ferlið **Sýnisstuðningsviðskiptaferli** og síðan velurðu til hægri **Breyta ham**.
3. Breyttu gildi bæði reitarins **Heiti** og reitarins **Lýsing** í **Losa afurð**. Veldu síðan **Vista**.

    ![Heiti og lýsingu breytt í Losa afurð](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Stofna nýja verkskráningu sem er með staðfestingaraðgerð

- Stofnaðu verkskráningu til að losa afurðina sem var stofnuð áður til lögaðila í Bandaríkjunum. Nánari upplýsingar er að finna í kaflanum [Stofna verkskráningu og vista hana í BPM-safnið](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Fyrir keðjuð prófunardæmi mælum við alltaf með að þú finnir eða síir fyrir skrána sem þú þarfnast með því að *rita gildið handvirkt inn í reitinn*. Þannig getur verkfærið ákvarðað skrána sem nota verður aðgerðin við í síðara prófunardæminu.

    ![Ný verkskráning sem er með staðfestingaraðgerð](./media/setup_rsa_tool_96.png)

    Þegar afurðin er fundin með því að nota flýtiafmörkun, en áður en þú velur **Losa afurðir**, staðfestirðu gildi reitsins **Afurðarnúmer** til að ganga úr skugga um að afurðakennið sé það afurðakenni sem var búið til áður, eins og skýringarmyndin á undan sýnir. Til að staðfesta gildi skaltu hægrismella á reitinn **Afurðarnúmer** og velja síðan **Verkskráning \> Staðfesta \> Núverandi gildi**.

    ![Staðfesting á núvarndi gildi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Vistaðu verkskráninguna í BPM

1. Þegar verkskráningunni er lokið skaltu velja **Vista í Lifecycle Services**.

    ![Vista valkosti](./media/setup_rsa_tool_98.png)

2. Upplýsingar um söfn er hlaðið úr LCS.

    ![Framvinduvísir](./media/setup_rsa_tool_99.png)

3. Veldu BPM-safn til að tengja við verkskráninguna. Fyrir þetta kennsluefni skaltu velja BPM-safnið **RSAT** sem var stofnað áður og síðan viðskiptaferlið **Losa afurð** undir því. Veljið síðan **Í lagi**.

#### <a name="sync-bpm-to-azure-devops"></a>Samstilla BPM við Azure DevOps

1. Farðu í BPM-safnið og opnaðu **RSAT**-safnið.
2. Veldu **VSTS-samstilling** og síðan **Samstilla prófunardæmi**. Nánari upplýsingar er að finna í kaflanum [Prófa samstillingu úr BPM við Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Þegar samstillingunni er lokið, verður nýr vinnuliður og samsvarandi prófdæmi fyrir viðskiptaferlið **Losa afurð** birtist í Azure DevOps á **Spjald \> Vinnuliðir**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Bættu nýjum prófunardæmum við núverandi prófunarpakka

1. Farðu í **Prófunaráætlanir \> Prófunaráætlanir** og veldu áætlunina **RSAT-prófunaráætlun**.
2. Veldu **Bæta við fyrirliggjandi**.
3. Á síðunni **Bæta prófunardæmum við í safn** velurðu **Keyra fyrirspurn**.
4. Veldu nýja prófunardæmið sem var búið til fyrir **Losa afurð** og veldu síðan **Bæta við prófunardæmum** neðst í hægra horni síðunnar (þessi hnappur er ekki sýndur á eftirfarandi mynd).

    ![Síðan Bæta prófunardæmum við safn](./media/setup_rsa_tool_100.png)

    Núna er prófunarsafnið með tvö prófunardæmi.

    ![Tvö prófunardæmi í prófunarpakkanum](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Hlaða prófunardæmum í RSAT

1. Opnaðu RSAT og veldu **Sækja**.
2. Prófunardæmunum hefur verið hlaðið og þú færð viðvörun sem segir: „Þessi aðgerð mun skrifa yfir Excel-prófgagnaskrár, staðbundnar breytingar munu glatast. Á að halda áfram?“ Veldu **Já** til að uppfæra Excel-færibreytuskrár í staðbundna kerfinu en ekki Excel-færibreytuskrár sem var hlaðið upp í Azure DevOps.

    ![Viðvörunarboð](./media/setup_rsa_tool_102.png)

    Báðum prófunardæmunum hefur verið hlaðið, ásamt Excel-færibreytuskránni fyrir fyrsta prófunardæmið. Þar sem þú valdir **Hlaða upp** í síðustu keyrslunni eru færibreytuskrárnar dregnar úr Azure DevOps.

    ![Prófunardæmum hlaðið](./media/setup_rsa_tool_103.png)

3. Veldu aðeins annað prófunardæmið og veldu síðan **Nýtt \> Mynda prófunarkeyrslu og færibreytuskrár**.

#### <a name="edit-the-excel-parameter-file"></a>Breyta Excel-færibreytuskránni

1. Veldu aðeins annað prófdæmið og veldu síðan **Breyta** til að opna samsvarandi Excel-færibreytuskrá.
2. Afritaðu vistaða breytu **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (sjá kaflann [Breyta núverandi verkskráningu til að stofna vistaða breytu](#modify-an-existing-task-recording-to-create-a-saved-variable)) úr fyrsta prófunardæminu inn í alla reiti þar sem afurðarnúmerið er notað. Í þessu dæmi afritar þú breytu inn í reitina **Afurðarnúmer** og **Staðfesta afurðarnúmer** á blaðinu **EcoResProductListPage**.

    ![Reitirnir Afurðarnúmer og Staðfesta afurðarnúmer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Aðeins er hægt að láta breytur ganga áfram á milli prófana í sömu prófunarkeyrslu. Heiti breytanna verða að stemma nákvæmlega.

3. Veldu **Vista** og lokaðu síðan Excel-skjalinu.
4. Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni.

#### <a name="run-the-chained-test-cases"></a>Keyrðu keðjuð prófunardæmi

1. Veldu bæði prófunardæmin og veldu síðan **Keyra**.
2. Staðfestu að bæði prófunardæmin hafi staðist.

    ![Niðurstöðureiturinn stilltur á staðist fyrir bæði prófunardæmin](./media/setup_rsa_tool_105.png)
